# World Model Lab Supply Chain — Wave 0: Engineer Grounding Memo
**Date:** 2026-07-05
**Scope:** Forced capital expenditures in the next 6–9 months across world-model labs
**Labs in scope:** World Labs (Fei-Fei Li), AMI Labs (Yann LeCun), Physical Intelligence (pi), Runway, Luma, Decart, Odyssey, Nvidia Cosmos program
**Principle:** Follow FORCED capital spend — what they MUST buy regardless of whether world models ultimately work

---

## 1. The Funding Context (brief, not the point)

As of mid-2026, confirmed raises relevant to forced near-term spend:
- **AMI Labs:** $1.03B seed (Mar 2026) — Europe's largest seed ever. Compute + talent are explicitly the two stated cost centers.
- **World Labs:** $1.0B round (Feb 2026) at $5.4B valuation. Nvidia and AMD both invested, suggesting hardware procurement pipeline is already being socialized.
- **Physical Intelligence (π):** $600M at $5.6B (Nov 2025).
- **Luma:** $900M Series C (Nov 2025) at ~$4B.
- **Runway:** $315M Series E (Feb 2026) for explicit pretraining pivot to world models.
- **Decart:** $100M (Aug 2025) + $300M Series B led by Radical Ventures.
- **Odyssey:** in-market.

Collectively, ~$4B+ newly deployed into labs that have committed to training world foundation models in 2026. These labs must show training progress to maintain valuation credibility. That means forced spend.

---

## 2. Bill of Materials — Forced Spend Nodes

### Node 1: H100/H200/B200 GPU Clusters (training compute)
**(a) What it is:** Large-scale GPU cluster contracts — either cloud reservations (CoreWeave, Lambda, AWS, Azure, Oracle) or on-prem procurement. Typical foundation-scale pretraining run requires 512–4,000+ 80GB SXM GPUs running for 60–180 days continuous.

**(b) Why forced/non-discretionary in ≤9 months:** Every lab has announced a pretraining program. Pretraining is the single non-deferrable gate: without it there is no product, no next funding round, no credibility. AMI Labs has explicitly stated compute is one of two main cost centers. World Labs and Runway have pivoted explicitly to pretraining world models. The physics of these jobs: a $50–200M training run requires reserving cluster capacity months in advance (demand is supply-constrained). Contracts must be signed now to get compute in the 6–9 month window. Slipping this slips the entire roadmap.

**(c) Confidence:** HIGH

**(d) Share of spend:** Dominant. Estimated 55–75% of total non-talent opex for the first 18 months. A single frontier training run costs $50–200M in compute. Labs with $300M–$1B raises can fund 2–5 runs if disciplined, but every dollar goes through the GPU channel.

**Vendor concentration:** Nvidia (H100 SXM, H200, B200 Blackwell) is 90%+ of supply. AMD MI300X is available but the software stack ecosystem is immature for novel architecture research — most labs default Nvidia. Blackwell (B200/GB200) is ramp-constrained in H1 2026 but available on committed contracts.

---

### Node 2: HBM Memory (HBM3e / HBM4)
**(a) What it is:** High-bandwidth memory stacked on GPU dies. H200 has 141GB HBM3e at 4.8 TB/s. B200 is ~192GB HBM3e. Rubin-class will require HBM4.

**(b) Why forced:** World models are distinctly memory-hungry relative to language models. Video/multimodal context windows are long; JEPA-style architectures process high-dimensional spatiotemporal representations that do not compress to short sequences. The 14B-parameter Cosmos-Predict model alone requires two 80GB H100s at full precision. For active training at batch scale, HBM capacity directly determines whether a training run is feasible at all. Labs cannot substitute away from this — it is baked into the accelerator.

**(c) Confidence:** HIGH (this is just: "you buy a GPU, you bought the HBM in it")

**(d) Share of spend:** Not separately purchased — embedded in GPU cost. Roughly 25–35% of the per-GPU BOM cost is HBM (SK Hynix ~85% HBM3e share, Micron ramping). Flagged here because HBM supply constraints are the proximate bottleneck on Nvidia GPU availability, not GPU die yield.

**Supply risk note:** HBM4 mass production from SK Hynix targeted late 2025, actual volume ramp into 2026. Any yield slip means Nvidia falls back to HBM3e configs on Rubin, delaying next-gen cluster availability for labs.

---

### Node 3: High-Speed Networking Fabric (InfiniBand / RoCE / NVLink)
**(a) What it is:** Within-cluster interconnect — NVLink for intra-node GPU-to-GPU (NVLink 4/5 at 900 GB/s aggregate per GPU), InfiniBand NDR (400 Gb/s) or HDR for inter-node. All-reduce operations during training backprop require terabits/sec aggregate bandwidth.

**(b) Why forced:** Multi-node training at 512–4,000 GPU scale requires InfiniBand or equivalent. Without it, all-reduce becomes the wall — GPUs sit idle waiting for gradient sync. There is no software workaround to physics: you cannot gradient-average faster than the wire. World models are particularly sensitive because batch sizes are large (video frames are 10–100x the data of text tokens) and gradient tensors are correspondingly huge. This is not deferrable: you cannot start training without the fabric in place.

**(c) Confidence:** HIGH

**(d) Share of spend:** Roughly 8–15% of cluster BOM. On a 1,000-GPU H100 cluster, the InfiniBand fabric alone (NDR switches + cables) runs $5–15M. If labs own their own hardware vs. renting cloud (where fabric is bundled), this is a separate procurement. For cloud-rented clusters, this is embedded.

**Mega-cap flag:** Nvidia owns Mellanox/InfiniBand. Broadcom supplies Ethernet/RoCE switching ASICs. Both large caps. Smaller optical cabling vendors supply the physical fiber.

---

### Node 4: Optical Transceivers and Fiber (400G/800G/1.6T)
**(a) What it is:** Pluggable optical modules (QSFP-DD, OSFP) that convert electrical signals to light across rack-scale or multi-rack inter-switch distances. At frontier AI cluster scale (800G links per GPU port emerging in 2026), transceiver spend is a meaningful line item.

**(b) Why forced:** The shift to Blackwell-class clusters requires 800G transceivers (OSFP form factor) — 800G shipments grew 100% YoY in 2025 and are the mainstream choice for new deployments. 1.6T transceivers are entering production for Nvidia and hyperscaler applications. Labs renting cloud don't buy these directly, but labs building on-prem clusters (Physical Intelligence's robot simulation infrastructure, Decart's chip-agnostic custom cluster) do. For the broader datacenter buildout that must absorb this demand, transceiver supply is a real constraint.

**(c) Confidence:** MEDIUM (direct lab spend depends on own-vs-rent decision; most smaller labs will rent)

**(d) Share of spend:** 3–8% of owned cluster BOM. The broader market is $16B+ in 2025. Spend concentrates in Coherent, Lumentum, II-VI / Coherent (post-merger), InPhi/Marvell. Nvidia has signed multi-year agreements with Lumentum and Coherent, signaling supply chain lock.

---

### Node 5: Data Center Power Infrastructure (PDUs, UPS, HVDC, generators)
**(a) What it is:** Power delivery from utility substation to rack — transformers, switchgear, PDUs (power distribution units), UPS systems, backup generators, and emerging 800V HVDC bus architecture. An H100 DGX node draws 10.2 kW; racks run 40–50 kW in liquid-cooled configs.

**(b) Why forced:** You cannot run a training cluster without power. For labs building dedicated compute (Physical Intelligence runs its own robot simulation clusters; Decart has built bespoke hardware infrastructure for sub-35ms latency world models), power delivery infrastructure is a capital line item. Even cloud-rented labs are indirectly forcing this spend on the CSPs they contract with.

**(c) Confidence:** HIGH for owned infrastructure; MEDIUM as direct lab spend (most labs are cloud-rented in the first year post-raise)

**(d) Share of spend:** 5–10% of datacenter CAPEX. Nvidia's 800V HVDC architecture is gaining traction (Navitas GaN/SiC PSUs at 98% efficiency). This is primarily spend at hyperscalers and co-lo operators, not directly at the labs — but it is forced downstream.

---

### Node 6: Liquid Cooling Systems (CDUs, cold plates, coolant distribution)
**(a) What it is:** Coolant distribution units (CDUs), direct liquid cooling (DLC) cold plates for GPU modules, rear-door heat exchangers, or full immersion tanks. Required for 40–50 kW/rack densities.

**(b) Why forced:** Air cooling is physically inadequate at H100/B200 rack densities. A 10-kW DGX node cannot be air-cooled in a standard datacenter without purpose-built hot-aisle containment. Labs with any on-prem infrastructure must deploy liquid cooling or rent space in liquid-cooling-capable co-lo. This is not a choice: the laws of thermodynamics force it.

**(c) Confidence:** HIGH (physics-enforced)

**(d) Share of spend:** 4–8% of datacenter CAPEX for labs with owned infrastructure. Primarily a cost for hyperscalers/co-lo operators. Vendors: Vertiv, Schneider Electric, nVent, CoolIT, Asetek for CDUs; Lenovo/HPE/Supermicro for DLC-ready server chassis.

---

### Node 7: High-Throughput Parallel Storage (petabyte-scale NVMe / all-flash)
**(a) What it is:** Parallel distributed file systems (VAST Data, WekaIO, IBM Spectrum Scale / GPFS, Lustre) backed by NVMe SSDs or high-density HDDs, delivering sustained read bandwidth of 1–10+ TB/s to the training cluster.

**(b) Why forced:** World model training datasets are categorically larger than LLM text datasets. A 70M-video corpus (comparable to Panda-70M) at even compressed 720p is petabytes. Internet-scraped video for Runway/Luma pretraining is 100s of petabytes raw before curation. Physics-based simulation outputs (Nvidia Cosmos, Isaac Sim) generate terabytes per day of rollout data. If the storage tier cannot feed the GPUs fast enough, GPUs sit idle waiting for data — effectively burning money. Storage throughput must match cluster aggregate memory bandwidth.

**(c) Confidence:** HIGH

**(d) Share of spend:** 5–12% of total infrastructure CAPEX. An all-flash VAST/Weka system at petabyte scale runs $1–5M for a well-equipped lab cluster. On-prem decisions force this. Cloud-rented compute can use object storage (S3/GCS) but incurs egress costs and latency penalties for hot training loops — leading most serious labs to hybrid or dedicated storage tier.

---

### Node 8: Video-Centric Pretraining Data (internet video licenses / crawl infrastructure)
**(a) What it is:** Licensed video content (film/TV libraries, stock footage, YouTube partner agreements), web crawl infrastructure for video ingestion, and data curation pipelines. Labs like Runway, Luma, World Labs (spatial video focus) must continuously ingest, deduplicate, caption, and filter petabytes of video.

**(b) Why forced:** Pretraining world models on video is the training paradigm. There is no world model without world data. Internet video is the primary training signal for the non-robotics labs (Runway, Luma, Decart). Building the pretraining dataset takes months of pipeline work and ongoing licensing negotiations. The curation infrastructure (GPU-accelerated filtering, optical flow estimation, CLIP scoring) is itself compute-heavy — typically 5–15% of total training compute goes to data pre-processing.

**(c) Confidence:** HIGH for video-first labs (Runway, Luma, Decart); MEDIUM for robotics-first labs (Physical Intelligence) which rely more on teleoperation/sim data

**(d) Share of spend:** 3–10% of total operational spend. Hard to quantify publicly; licensing arrangements are opaque. This is a real, material, and underappreciated line item.

---

### Node 9: Real-World Physical Data Capture Hardware (robotics/manipulation labs only)
**(a) What it is:** Teleoperation rigs (VR headsets + haptic controllers + robot arms for demonstration capture), multi-camera arrays (8–16 calibrated RGB cameras per workspace station), depth cameras (Intel RealSense, Luxonis OAK), and LiDAR scanners (Velodyne, Ouster, Livox) for 3D scene reconstruction.

**(b) Why forced:** Physical Intelligence and any lab building robot foundation models (π0, π0.5) cannot train without real manipulation demonstrations. Synthetic data substitutes partially (see Node 10 analysis) but does NOT close the sim-to-real gap for dexterous manipulation tasks. The evidence: optimal training mixes ~60–80% synthetic with 20–40% real demonstrations. The real portion is non-substitutable. Collection throughput is 10–40 demonstrations per hour per rig — to collect 50,000 demos requires 5,000–12,500 rig-hours. For a 6-month horizon, that means maintaining a fleet of 10–30 teleoperation stations running nearly continuously.

**(c) Confidence:** HIGH for robotics labs (Physical Intelligence, any humanoid-adjacent lab); LOW for video-generative world model labs (Runway, Luma, Decart — these are NOT hardware buyers)

**(d) Share of spend:** For robotics-focused labs, 8–15% of operational spend. Per teleoperation station: ~$5,000–$25,000 in hardware (robot arm + camera array + VR rig). At 30 stations, $150K–$750K hardware; ongoing cost is labor (teleoperators), not hardware. The labor is the true cost driver, not the sensors.

---

### Node 10: 3D Scene Capture and Reconstruction Infrastructure
**(a) What it is:** Ground-truth 3D data for spatial world models (World Labs focus). This means: aerial photogrammetry rigs (drones + high-res oblique cameras), ground-level 3DGS reconstruction pipelines, LiDAR-equipped vehicles for urban scene scanning, and GPU-accelerated reconstruction compute (3DGS training is GPU-intensive).

**(b) Why forced:** World Labs is explicitly building spatial intelligence — AI that understands and generates 3D scenes. Their core product requires 3D ground-truth training data, not 2D video alone. 3D Gaussian Splatting is the current state-of-the-art method for converting multi-view imagery to differentiable 3D representations. The reconstruction pipeline itself requires GPU compute (each 3DGS scene fit takes minutes to hours on 1–4 GPUs). Scale: a city-scale dataset of thousands of scenes requires a systematic capture and reconstruction operation.

**(c) Confidence:** MEDIUM-HIGH for World Labs specifically; LOW for labs without explicit spatial/3D focus

**(d) Share of spend:** 5–15% of World Labs' early operational budget, covering capture logistics, data storage, and reconstruction compute. Hardware cost per capture rig: $20K–$100K (drone + camera system), plus crew and logistics. This is real but not a massive absolute dollar number — total 3D capture fleet cost is $2–10M for a serious program. The primary cost is the reconstruction compute (GPU-hours), which folds into Node 1.

---

## 3. KILL List — Discretionary or Deferrable Items

### KILL 1: Dedicated LiDAR Sensor Procurement for Video-Generative Labs
**Why kill:** Runway, Luma, and Decart are training on internet video. They have no use for LiDAR. LiDAR is essential only for:
- Labs building physical robot navigation (not Runway/Luma/Decart/Odyssey)
- High-precision 3D reconstruction programs (World Labs, possibly Physical Intelligence for scene understanding)
The market narrative around "world models will need sensors" is partially correct but dramatically over-applied. The majority of world model labs (by count and by funding in this cohort) are NOT buying LiDAR.

**Verdict:** KILL as a universal world-model supply chain thesis. Narrow to robotics-specific labs.

### KILL 2: Custom Silicon / ASIC Development for Most Labs
**Why kill:** Decart has partnered with Etched (the Sohu transformer ASIC) and claims chip-agnostic optimization — but even Decart is not designing its own silicon. The time horizon for a custom AI accelerator from architecture to production is 18–36 months minimum, with tape-out cost of $50–200M. No lab in this cohort has the funding or timeline to spin custom silicon in a 6–9 month window. Even Decart's Sohu partnership is a chip it buys/uses, not designs.
**Verdict:** KILL for the 6–9 month window. This is a 24–36 month thesis at best, relevant only to the largest players (Nvidia itself, Google TPU, Amazon Trainium).

### KILL 3 (soft kill): Autonomous Mobile Data-Collection Robot Fleets
**Why deferrable:** Some analysts suggest world model labs will need fleets of autonomous cars/drones continuously scanning the world. This is premature for 6–9 months:
- Existing public datasets (Waymo Open, nuScenes, Mapillary, internet video) provide sufficient bootstrapping signal for the first generation of pretraining runs
- Building a proprietary autonomous collection fleet requires regulatory approvals, hardware integration, and operational scale that takes 12–24 months minimum to stand up
- The current generation of world models does NOT require proprietary real-world collection fleets; they rely on existing internet/partner video data + simulation

**Verdict:** Partially kill for near-term. Flag as a Phase 2 thesis (12–24 months out for the best-funded labs).

---

## 4. The Synthetic Data Substitution Effect

This is the most important engineering nuance that most supply-chain analyses miss.

**The actual synthetic/real split as of 2025–2026:**
- Optimal training mixes: 60–80% synthetic, 20–40% real demonstrations
- Nvidia Cosmos/GR00T-Dreams is the canonical example: a small seed of real human demonstrations is expanded into a large synthetic trajectory library using the world model itself as a data engine (bootstrapping)
- The "sim-to-real gap" is real and closing but not closed — real data is still required, especially for dexterous manipulation

**Quantitative effect on hardware demand:**
- For video-generative labs (Runway, Luma, Decart): synthetic data generated by the model itself feeds back into training. This REDUCES the need for external data ingestion infrastructure but INCREASES training compute demand (because generating synthetic data costs GPU cycles). Net effect: more GPU compute required, less data-collection hardware required.
- For robotics labs (Physical Intelligence): synthetic simulation can replace perhaps 60–70% of teleoperation demonstrations. A lab that without sim would need 100,000 real demonstrations might need only 20,000–40,000 real demos. This reduces the teleoperation rig fleet requirement by roughly 2–3x but does NOT eliminate it.

**Bottom line:** Synthetic data substitution SHIFTS spend from data-collection hardware to GPU compute. It amplifies the GPU bottleneck, not relieves it.

---

## 5. Spend Concentration Summary

| Category | Forced? | Confidence | Mega-cap vs. Small | Rough % of lab CAPEX |
|---|---|---|---|---|
| GPU/accelerator clusters (H100/H200/B200) | FORCED | HIGH | 90%+ Nvidia (mega-cap) | 55–75% |
| HBM memory (embedded in GPU) | FORCED | HIGH | SK Hynix, Micron (large cap) | Embedded in GPU |
| Networking fabric (IB/NVLink) | FORCED | HIGH | Nvidia Mellanox (mega-cap) | 8–15% |
| Optical transceivers (800G/1.6T) | FORCED (owned infra) | MED | Coherent, Lumentum (mid-cap) | 3–8% owned |
| Datacenter power (HVDC, PDU, UPS) | FORCED (owned infra) | HIGH | Vertiv, Schneider (mid-large cap) | 5–10% owned |
| Liquid cooling (CDUs, cold plates) | FORCED (owned infra) | HIGH | Vertiv, CoolIT, Asetek (mid-small) | 4–8% owned |
| Parallel storage (VAST/Weka/NVMe) | FORCED | HIGH | VAST Data, WekaIO (small-mid) | 5–12% |
| Video data licensing/crawl | FORCED (video labs) | HIGH | Diffuse (content owners) | 3–10% |
| Teleoperation rigs (robotics labs only) | FORCED | HIGH for π/humanoid | Small vendors + custom | 8–15% robotics |
| 3D capture hardware (World Labs only) | FORCED | MED-HIGH for WL | Small/niche drone/sensor | 5–15% spatial labs |

**Key takeaway:** Spend is overwhelmingly concentrated in GPU compute (Nvidia) and the HBM supply chain (SK Hynix, Micron). Everything else is a rounding error in aggregate, though there are specific niche vendor opportunities in storage (VAST/Weka), cooling (Vertiv), and optics (Coherent, Lumentum).

---

## 6. Engineering Red Flags — What Could Disrupt This Spend Pattern

1. **Cloud-vs-own decision:** Most post-Series-A labs will rent cloud GPUs for the first 1–2 pretraining runs, then evaluate on-prem. This means MOST of the non-compute supply chain spend (cooling, power, networking, storage) is being absorbed by AWS/Azure/CoreWeave/Oracle, not the labs directly. The labs' direct forced spend is primarily the cloud contract.

2. **Training efficiency improvements:** JEPA architectures (LeCun's AMI) claim to be more compute-efficient than autoregressive models. If true, this reduces GPU cluster size requirements — but this is speculative and labs will over-provision regardless until the efficiency claims are validated.

3. **Cluster availability:** H200 and B200 availability on CoreWeave/Lambda is currently 4–12 weeks lead time for large reservations. Labs that didn't sign contracts by Q1 2026 face compute delays. This creates a real forcing function: labs MUST sign GPU contracts now or slip their roadmap.

4. **Real-world data moats forming:** Physical Intelligence and the humanoid robot companies are each building proprietary demonstration datasets. Early entrants (π, 1X, Figure) have a meaningful head start. The cost to close this gap for later entrants is multiplicative (not additive) in teleoperator labor and equipment.

---

## Coverage Gaps

The following items could not be confirmed from available public sources and represent uncertainties:

1. **Specific GPU contract sizes and counterparties for AMI Labs and World Labs.** Neither has disclosed their compute procurement. Inferred from funding size and comparable labs.
2. **Precise synthetic-to-real ratios for video-generative world models (Runway, Luma).** The 60–80% synthetic guidance comes from robotics literature; video-generative labs have not published their data mix.
3. **World Labs' 3D capture program specifics.** World Labs has not disclosed its data collection methodology; the spatial-intelligence inference is based on their stated mission and the nature of the problem.
4. **Decart's bespoke hardware stack details.** Decart has published that it achieves 100x efficiency via hardware optimization and uses Sohu (Etched) chips, but cluster size and capex are not disclosed.
5. **Odyssey's funding and technical program.** Odyssey is generating significant interest but published financials and technical architecture are minimal.
6. **Power infrastructure ownership model for smaller labs.** Whether labs rent colocation vs. build their own power/cooling infrastructure determines whether they directly incur this spend or if it flows through the cloud/colo operators.
7. **Luma's training transition specifics.** Luma raised $900M (Nov 2025) and has strong video generation products, but its world model pretraining program is less publicly documented than Runway or AMI.
8. **Data licensing deal structures.** Video licensing for pretraining is opaque; no lab has disclosed what they pay for licensed video content vs. crawled/scraped data.

---

*Sources consulted: TechCrunch, Crunchbase, HPCWire, Futurum Group, latent.space (AI News), Together AI GPU pricing, WhiteFiber GPU infrastructure guide, Spheron/NVIDIA Cosmos documentation, NVIDIA newsroom, Introl Blog (optics/infrastructure), TrendForce AI infrastructure report, DataX Power blog on Physical AI training data, truelabel.ai synthetic data guide, NVIDIA developer blog (GR00T-Dreams / Cosmos), voxel51 Visual AI 2026 landscape.*
