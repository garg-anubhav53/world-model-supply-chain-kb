# Track W — World Model Training Supply Chain
## Wave 0: Grounding Memo
**Date:** 2026-07-05
**Scope:** Forced spend nodes for world-model labs (World Labs, AMI Labs/LeCun, Physical Intelligence, Runway, Luma, Decart, Odyssey, Nvidia Cosmos) that raised billions Nov 2025–Jun 2026. Covers hardware/software bill-of-materials and maps each node to real suppliers, chokepoints, and investor-accessibility leakage.

---

## 1. GPUs / Accelerators

### Vendors
- **Nvidia** (NVDA) — H200, B200/B300, GB300, Rubin (HBM4-based, late 2026). The dominant vendor; NVIDIA alone reportedly consumes ~54% of all global HBM.
- **AMD** (AMD) — MI300X/MI325X; gaining share at select hyperscale customers but minimal traction at frontier labs.
- **Google TPUs** (captive/internal) — used in-house; not sold at arm's length.
- **AWS Trainium2, Microsoft Maia** — captive hyperscaler ASICs; no direct external access.
- **Cerebras, Graphcore, SambaNova** — private; niche; minimal world-model penetration.

### Chokepoint?
YES — TSMC CoWoS advanced packaging is the single most acute bottleneck. Every leading AI accelerator (Nvidia, AMD, Google TPU) is fabbed on TSMC 4nm/3nm and packaged via CoWoS. CoWoS capacity was reportedly booked out 2+ years as of mid-2025. TSMC has no credible alternative at volume. TSMC's Taiwan geographic concentration is a systemic geopolitical risk.

### Captive / Vertical Integration Risk
HIGH. Hyperscalers (Google, AWS, Microsoft, Meta) are aggressively building captive ASICs. For world-model labs that are NOT hyperscalers, they must buy Nvidia or rent cloud. But the acceleration spend itself lands predominantly on Nvidia (NVDA) and then bleeds through to TSMC (captive via ADR: TSM) and SK Hynix (HBM, below). AMD has secondary exposure.

### Leakage
- Hyperscaler captive ASICs: LEAKAGE (captive, no public stock access)
- TSMC CoWoS packaging: ACCESSIBLE via TSM ADR but also major leakage since TSM is >$800B market cap (mega-cap)
- Nvidia: ACCESSIBLE but mega-cap ($3T+ range), so marginal forced-spend delta is small relative to market cap

### Accessibility: POOR for asymmetric upside — the spend lands squarely on mega-caps (Nvidia, TSMC)

---

## 2. HBM / Memory

### Vendors
- **SK Hynix** (000660.KS / OTC: HXSCL) — ~62% HBM market share as of Q2 2025; exclusive early supplier for Nvidia H100/H200 HBM3E; 12-stack HBM3E ramping; HBM4 volume 2026.
- **Micron Technology** (MU) — ~21% HBM share; shipping 12-stack HBM3E; HBM4 on 2026 roadmap. Only US-listed pure-play.
- **Samsung** (005930.KS / OTC: SSNLF) — ~17% share; struggled with yield on 12-layer stacks; HBM3E qualification completed in 2025. Also massive foundry.

### Chokepoint?
YES — three-vendor oligopoly with supply sold out through 2026. HBM demand grew 130% YoY in 2025 and 70% projected in 2026. Memory vendors have reallocated capacity away from commodity DRAM/NAND to HBM, creating secondary supply tightness in consumer/auto segments. No new entrant can qualify meaningful volume before 2028+.

### Captive / Vertical Integration Risk
LOW on captive risk. Unlike chip packaging, memory is not made in-house by Nvidia or hyperscalers; they buy from SK Hynix/Micron/Samsung. SK Hynix has deepened its Nvidia partnership (supply priority agreements), partially making it quasi-captive from a supply perspective, but the equity is publicly accessible.

### Leakage
- SK Hynix: PARTIAL ACCESS (Korean exchange listing; US OTC thin; requires ADR or direct KRX brokerage)
- Samsung: PARTIAL ACCESS (same Korean exchange friction; diluted by massive conglomerate)
- Micron: GOOD ACCESS (NYSE: MU) — the most accessible US-listed HBM exposure

### Accessibility: PARTIAL to GOOD — Micron (MU) is the cleanest US-accessible HBM proxy; SK Hynix requires Korean market access

---

## 3. Networking & Optical Interconnect

### Vendors
**Switch Silicon / Fabrics:**
- **Nvidia / Mellanox** (NVDA) — dominates InfiniBand (NDR 400G, 800G); Spectrum-X for AI Ethernet; 1600G switch (Spectrum-X1600) H2 2026
- **Broadcom** (AVGO) — leads AI Ethernet; Tomahawk 6 (102.4 Tbps); CPO-enabled Tomahawk products; strong with hyperscalers
- **Arista Networks** (ANET) — cloud-native Ethernet switches; strong hyperscale fabric presence; 400G/800G leaf-spine
- **Cisco** (CSCO) — Silicon One G300 (102.4 Tbps) announced Feb 2026; re-entering AI cluster market
- **Marvell** (MRVL) — 800G custom silicon; strong 800G interconnect market position; also custom ASIC for hyperscalers

**Optical Transceivers / Modules:**
- **Coherent Corp.** (COHR) — major 400G/800G datacom module supplier; one of top-3 hyperscale module vendors
- **InnoLight** (private, China) — reportedly largest hyperscale datacom module vendor by volume; LEAKAGE (private + China-based)
- **Eoptolink** (300502.SZ) — Chinese-listed; among top-3 hyperscale module vendors; LEAKAGE (China-listed)
- **Fabrinet** (FN) — US-listed contract manufacturer for optical modules (Coherent, Nvidia, others); excellent indirect exposure
- **II-VI / now Coherent** — merged entity
- **Lumentum** (LITE) — laser/optical component supplier

**Co-Packaged Optics (CPO) — emerging:**
- Nvidia, Broadcom, Marvell, Intel all developing; 2026 is initial volume ramp year. CPO shifts value back to chip vendors and away from discrete module makers.

### Chokepoint?
YES — optical interconnect modules (especially 800G, moving to 1.6T) have entered extended lead times. Laser components and indium phosphide substrates are specifically identified as booked 2+ years. The speed transition (400G → 800G → 1.6T) creates qualification bottlenecks that compress the qualified vendor set.

### Captive / Vertical Integration Risk
MEDIUM. CPO integration (co-packaging optics into the switch ASIC) is being pushed by Nvidia and Broadcom, which would reduce the addressable market for discrete module vendors like Coherent, Fabrinet, and Lumentum over a 3–4 year horizon. This is a structural risk for optical module pure-plays.

### Leakage
- InnoLight: LEAKAGE (private + Chinese)
- Eoptolink: LEAKAGE (China-listed)
- Nvidia/Broadcom for switch silicon: accessible but mega-cap
- **Arista (ANET), Coherent (COHR), Fabrinet (FN), Marvell (MRVL)**: GOOD TO PARTIAL ACCESS — mid/large cap with meaningful AI networking exposure

### Accessibility: GOOD for networking pure-plays; optical module sub-segment has China/private leakage but US-listed alternatives exist

---

## 4. Servers / Rack Integration

### Vendors
- **Super Micro Computer** (SMCI) — high-profile AI GPU server builder; $11.7B revenue Q4 2025 (2.3x YoY); facing US government scrutiny re: alleged sanctioned GPU diversion to China
- **Foxconn / Hon Hai** (2317.TW / HNHPF OTC) — projected to become world's largest server vendor (Omdia); assembling Nvidia Vera Rubin racks to L10
- **Quanta Computer** (2382.TW) — ODM; assembling next-gen Nvidia racks; strong hyperscale relationships
- **Wiwynn** (6669.TW, subsidiary of Wistron) — liquid-cooled GB300 NVL72 racks; NVIDIA GB300 showcase at Computex 2025
- **Inventec** (2356.TW) — Taiwan ODM; AI server rack assembly
- **Pegatron / QCT** (linked Quanta) — rack-to-facility AI factory integration

### Chokepoint?
MODERATE. The ODM tier is concentrated in Taiwan (Foxconn, Quanta, Wiwynn, Inventec), creating geographic risk. Supermicro is the only meaningful US-based public assembler. Nvidia now centralizing assembly of Vera Rubin racks through Wistron/Quanta/Foxconn. Upstream chokepoint (GPUs, HBM, CoWoS) flows through this layer — the assembly tier itself is not the binding constraint.

### Captive / Vertical Integration Risk
MEDIUM. Hyperscalers (Google, Microsoft, Meta) design servers in-house using ODMs as assembly partners — this disintermediates traditional OEMs (Dell, HPE) from the AI rack market over time. Dell and HPE face secular displacement at top of pyramid.

### Leakage
- Taiwan ODMs: PARTIAL (Taiwan-listed; accessible via ADR/OTC but illiquid)
- Supermicro: GOOD (SMCI on Nasdaq) but faces regulatory overhang
- Foxconn: PARTIAL (OTC: HNHPF; thin volume)
- Hyperscaler in-house design: LEAKAGE (captive)

### Accessibility: PARTIAL — only SMCI is cleanly US-listed; Taiwan ODM stocks accessible but require non-US brokerage or thin OTC

---

## 5. Data Center Power

### Vendors
**Full-stack power (UPS, PDU, switchgear, transformers):**
- **Vertiv Holdings** (VRT) — largest pure-play; covers UPS, PDU, liquid cooling, switchgear; ~80%+ revenue from data centers; Q1 2026 revenue $2.65B (+30% YoY); backlog ~$9.5B
- **Schneider Electric** (SU.PA / SBGSF OTC) — EcoStruxure platform; UPS, modular power, liquid cooling; data center ~24% of total revenue (diluted)
- **Eaton** (ETN) — acquired Boyd for $9.5B in 2025 to add liquid cooling; UPS, switchgear, electrical distribution; broader industrial mix
- **ABB** (ABB) — power systems, switchgear, transformers
- **Delta Electronics** (2308.TW) — Taiwan-listed; UPS and power conversion
- **nVent Electric** (NVT) — thermal/liquid cooling enclosures; ~30% data center exposure; growing Nvidia partnership
- **Cummins** (CMI) — generators / backup power
- **Siemens, Legrand, Rittal** — European players; diverse exposure

**Grid/utility-scale power (the "last mile" into the campus):**
- **Eaton** (ETN) — medium-voltage switchgear
- **GE Vernova** (GEV) — power generation, grid equipment, transformers; direct beneficiary of data center power demand
- **Quanta Services** (PWR) — electrical infrastructure construction
- **Emerson Electric** (EMR) — power/HVAC controls

### Chokepoint?
YES — grid interconnection queues and substation equipment (transformers, switchgear) are now 2–4 year lead time. High-voltage transformer supply is acutely constrained: US transformer manufacturing capacity has not scaled with AI data center demand. Electric utilities and campus developers face power availability as the primary gating factor on new data center construction, not permits or real estate.

### Captive / Vertical Integration Risk
LOW. Power infrastructure cannot be vertically integrated by AI labs or hyperscalers in any meaningful way. The power layer is served by industrial/electrical specialists; no risk of Nvidia or Google making switchgear.

### Leakage
- Minimal structural leakage to China or captive (some Chinese UPS vendors exist but not dominant in high-reliability AI DC market)
- All major players are US/European-listed public companies

### Accessibility: GOOD — all major power vendors (VRT, ETN, GEV, PWR, NVT, EMR, SBGSF) are accessible on US or European exchanges

---

## 6. Data Center Cooling

### Vendors
**Direct-to-chip liquid cooling (CDU, cold plates):**
- **Vertiv** (VRT) — CDUs; partnership with ZutaCore for two-phase; 900W/GPU cooling
- **Motivair** (private) — high-density liquid cooling; Schneider partner
- **CoolIT Systems** (private) — direct-to-chip CDU; major hyperscale customer
- **Asetek** (ASTK.OL — Oslo-listed) — direct liquid cooling; smaller pure-play
- **Modine Manufacturing** (MOD) — data center thermal management; growing AI exposure
- **nVent Electric** (NVT) — Nvent Hoffman racks + liquid cooling enclosures

**Immersion / two-phase cooling:**
- **Submer** (private, Spain)
- **LiquidStack** (private)
- **GRC (Green Revolution Cooling)** (private)

**Traditional CRAC/CRAH/chiller:**
- **Johnson Controls** (JCI) — chillers
- **Emerson Electric** (EMR) — Liebert precision cooling
- **Daikin, Carrier** — large chiller supply

### Chokepoint?
MODERATE. Liquid cooling is rapidly becoming mandatory for 1000W+ GPUs (Blackwell, Rubin). Vendors who can qualify and deliver direct-to-chip systems at rack scale are supply-constrained. Most liquid cooling pure-plays are private.

### Captive / Vertical Integration Risk
LOW. Hyperscalers co-design cooling solutions with vendors but do not manufacture CDUs in-house at scale.

### Leakage
- Dominant liquid cooling specialists (CoolIT, Motivair, LiquidStack, Submer): LEAKAGE (private)
- Vertiv (VRT): GOOD ACCESS — best public proxy for both power and cooling

### Accessibility: PARTIAL — Vertiv is the best single-name exposure; pure-play liquid cooling is mostly private

---

## 7. Real-World & 3D Data Capture (Sensors, LiDAR, Scanning Rigs, Cameras)

### Vendors
**Industrial / terrestrial LiDAR:**
- **Leica Geosystems** (subsidiary of Hexagon AB, HEXA.B.ST) — BLK series, ground-truth 3D scanning; world-model scene capture
- **FARO Technologies** (FARO) — US-listed; industrial 3D scanning, Focus LiDAR scanners
- **Trimble** (TRMB) — geospatial capture; partner in NVIDIA OpenUSD ecosystem
- **Ouster** (merged with Cepton → acquired by Sense Photonics → now part of OUST) — LiDAR sensors; lower-cost; used in research pipelines

**Automotive-grade / mobile LiDAR:**
- **Velodyne / Ouster** (merged entity: OUST) — public, US-listed, small-cap; standard research-grade LiDAR
- **Hesai Technology** (HSAI) — China-listed American Depositary; dominant in affordable high-channel LiDAR; significant share of research deployments
- **Robosense** (2498.HK) — Hong Kong-listed; Chinese LiDAR; cost leader
- **Innoviz Technologies** (INVZ) — US-listed; solid-state LiDAR

**RGB cameras / depth cameras:**
- **Sony** (SONY) — image sensor dominant; ~50% of CMOS image sensor market
- **FLIR / Teledyne FLIR** (TDY) — thermal and multispectral; industrial machine vision
- **Basler, Allied Vision** (private, Germany) — industrial vision cameras
- **Intel RealSense** (captive Intel unit; Intel exited consumer RealSense but RGBD still used in research)
- **Microsoft Azure Kinect** (discontinued; successor devices fragmented)

**360-degree / photogrammetry cameras:**
- **Matterport** (acquired by CoStar Group, CSGP in 2024) — spatial data platform; indoor 3D scanning
- **Insta360, Ricoh, GoPro MAX** — consumer/prosumer 360 cameras used in scan pipelines

### Chokepoint?
MODERATE-LOW. No single chokepoint like HBM. LiDAR sensors are competitive; photogrammetry uses commodity cameras. The bottleneck for world-model data pipelines is more software/annotation labor than hardware. However, high-accuracy professional LiDAR (Leica BLK, FARO Focus) has limited competitive supply for ground-truth quality.

### Captive / Vertical Integration Risk
MODERATE. NVIDIA has built Cosmos as a synthetic data generator to *reduce* real-world data capture requirements — direct vertical integration risk to this node from NVIDIA. Labs training primarily on synthetic + internet video data may spend little on physical capture hardware.

### Leakage
- Hesai, Robosense: PARTIAL ACCESS (US-listed ADR/HK-listed; but China-domiciled = geopolitical risk, potential restrictions)
- Professional LiDAR (Leica via Hexagon): PARTIAL (Swedish exchange)
- FARO Technologies: GOOD (US-listed, small-cap)
- Sony image sensors: ACCESSIBLE (NYSE ADR: SONY) but mega-cap
- Most mid-tier camera vendors: PRIVATE (Basler, Allied Vision)

### Accessibility: PARTIAL/POOR — fragmented vendor set; China-domiciled leaders in affordable LiDAR; no clean single US-listed pure-play for world-model data capture hardware

---

## 8. Teleoperation Hardware

### Vendors
**Haptic gloves / exoskeletons:**
- **HaptX** (private) — haptic gloves; selected by Sanctuary AI for Phoenix robot data collection
- **DOGlove / HOMIE** (open-source academic) — not investable
- **Shadowrobot** (private, UK) — dexterous hands + teleop
- **Embodied Intelligence (Xi)** (private) — teleoperation for Physical Intelligence pipelines

**Leader/follower arm systems:**
- **ALOHA / ALOHA 2** (Stanford open-source hardware) — not investable; but commoditizing the space
- **UFactory** (private, Chinese manufacturer) — xArm; widely used in research; sub-$10K system
- **AgileX** (private, China) — mobile manipulation platforms

**Teleop software/services:**
- **Adamo** (private, US) — managed teleop services; sub-40ms latency
- **Cogito Tech / RoboStream** (private) — multimodal capture pipelines

### Chokepoint?
NO — the teleop hardware space is rapidly commoditizing. Chinese manufacturers produce capable leader-follower systems for under $2,000. Cost per hour of teleop data fell from $340/hr (early 2024) to $136/hr (Q4 2025). No meaningful supply chokepoint.

### Captive / Vertical Integration Risk
HIGH. Labs like Physical Intelligence and 1X/Figure/Apptronik are building or co-designing their own teleoperation rigs to match their robot morphology precisely. ALOHA-derived open-source hardware reduces reliance on commercial vendors. This node is not a defensible supplier position.

### Leakage
- ALL dominant teleop hardware vendors: LEAKAGE (private; several China-based)
- No accessible US public equity exposure to pure-play teleoperation hardware

### Accessibility: POOR — entirely private; China-based commodity manufacturers

---

## 9. Simulation / Rendering Software

### Vendors
- **Nvidia** (NVDA) — Omniverse (USD-based physical simulation); Cosmos (generative world model + synthetic data); Isaac Sim/Isaac Lab (robotics); NuRec neural rendering. Positioned as OS for physical AI. Partners: Adobe, Autodesk, Siemens, Ansys, PTC, Trimble in OpenUSD ecosystem.
- **Unity Technologies** (U) — ML-Agents; synthetic data generation; robotics simulation; widely used but struggling financially; no dominant AI lab customer base for world models
- **Epic Games / Unreal Engine** (private) — Unreal Engine 5; Nanite/Lumen rendering; used in CARLA AV simulation; photorealistic environment generation
- **Ansys** (now part of Synopsys after acquisition closes) — physics simulation; OpenUSD partner
- **Autodesk** (ADSK) — 3D content; OpenUSD; design-to-simulation workflows
- **SideFX Houdini** — procedural world generation; used in film/VFX pipelines repurposed for synthetic data
- **DeepMind / Google** (MuJoCo, captive) — open-source physics simulator; now NVIDIA Isaac interoperable
- **Microsoft** (AirSim, captive)

### Chokepoint?
NO for software. Simulation software is not supply-constrained. NVIDIA Omniverse is establishing de facto standard via OpenUSD lock-in, but labs can use competing simulators.

### Captive / Vertical Integration Risk
HIGH. Nvidia's strategy is to own the simulation stack (Omniverse/Cosmos) as a way to deepen GPU lock-in. Epic (Unreal) is private, limiting public equity access. Labs may develop proprietary simulators (Physical Intelligence, World Labs are building their own simulation pipelines).

### Leakage
- Nvidia (simulation): ACCESSIBLE but mega-cap; simulation is embedded in broader Nvidia story
- Unity (U): ACCESSIBLE but struggling, limited AI lab traction
- Autodesk (ADSK): ACCESSIBLE; indirect/partial exposure
- Ansys → Synopsys (SNPS): ACCESSIBLE post-acquisition close
- Epic/Unreal: LEAKAGE (private)
- In-house simulators: LEAKAGE (captive)

### Accessibility: POOR for pure-play simulation exposure; Nvidia captures the value but as mega-cap

---

## 10. Additional Node: Advanced Packaging (TSMC CoWoS / SoIC)

This node deserves standalone treatment given its identified status as the single tightest bottleneck.

### Vendors
- **TSMC** (TSM ADR) — monopoly on CoWoS (Chip-on-Wafer-on-Substrate) and SoIC 3D packaging for all leading AI accelerators (Nvidia, AMD, Google TPU). No credible alternative at volume until 2027+.
- **Samsung** — Foveros-equivalent in development but not at CoWoS scale for AI chips
- **Intel Foundry** — advanced packaging (Foveros) but minimal AI chip customer base
- **Amkor Technology** (AMKR) — outsourced semiconductor packaging; OSAT partner to TSMC overflow but not a substitute for CoWoS

### Chokepoint?
EXTREME — most acute single-point bottleneck in the entire AI supply chain. OCP conference data from early 2026 noted CoWoS is "no longer the #1 bottleneck" but this reflects temporary capacity additions, not a structural resolution. The constraint has shifted downstream (to memory, power, racks) but TSMC CoWoS remains highly concentrated.

### Leakage: PARTIAL — TSM ADR is accessible but mega-cap ($800B+)
### Accessibility: PARTIAL

---

## 11. Additional Node: Substrate / Advanced PCBs

- **TTM Technologies** (TTMI) — US-listed; AI server PCBs and substrates
- **Tripod Technology** (private, Taiwan) — ABF substrates
- **Ibiden / Shinko Electric** (private/Japan-listed) — ABF substrates; critical for GPU packages
- **Unimicron** (3037.TW) — Taiwan-listed; PCBs

### Chokepoint?
YES — ABF (Ajinomoto Build-up Film) substrates and advanced PCBs are supply-constrained. Lead times extended.

### Accessibility: PARTIAL — TTM (TTMI) is US-listed small-cap; Japanese/Taiwan substrate makers require foreign exchange access

---

## Coverage Gaps

The following areas were insufficiently resolved by the searches conducted and should be addressed in Wave 1:

1. **Cooling fluids / dielectric fluids for immersion cooling** — vendors like 3M (exited Novec), Engineered Fluids, Fluorez not adequately mapped
2. **Precision power conversion (VR/VRM — voltage regulator modules)** — Monolithic Power Systems (MPWR), Infineon, Texas Instruments; critical for per-GPU power delivery at 1000W+
3. **Fiber optic cable / passive cabling** — Corning (GLW) for hyperscale fiber runs; not covered
4. **DRAM (non-HBM) and NAND/SSD** — storage layer for training checkpoints and dataset caches (Samsung, Micron, Kioxia, Western Digital)
5. **Real estate / land / power rights** — Iron Mountain (IRM), Equinix (EQIX), Digital Realty (DLR) as data center REITs; the physical footprint layer
6. **Specialized AI data labeling / annotation** — Scale AI (private), Labelbox (private), Surge (private); required for world-model training data curation
7. **Network-attached storage for training clusters** — DDN, VAST Data, WekaIO (all private)
8. **Lab-specific proprietary hardware** — Physical Intelligence's internal capture rigs, Runway's multi-camera scan stages; entirely private and opaque
9. **Grid-scale energy storage / backup** — Tesla Megapack (TSLA), Fluence (FLNC); power continuity layer
10. **HVAC and mechanical contractors** — Turner Construction, EMCOR (EME); data center build-out contractors

---

## Summary Leakage Map

| Leakage Type | Nodes Affected |
|---|---|
| **Mega-cap** (accessible but no asymmetry) | GPUs (NVDA), packaging (TSM), switch silicon (AVGO, NVDA) |
| **Captive / in-house** | Hyperscaler ASICs, hyperscaler server design, in-house simulators, Nvidia Omniverse as GPU lock-in tool |
| **China-dominated / restricted** | Optical modules (InnoLight, Eoptolink), LiDAR (Hesai, Robosense), teleop arms (UFactory, AgileX) |
| **Private-only** | Teleop hardware (HaptX, CoolIT, Motivair), data labeling (Scale AI), liquid cooling (LiquidStack, Submer), NAS (VAST, DDN) |
| **Best accessible exposure** | HBM → Micron (MU); Power → Vertiv (VRT), GE Vernova (GEV), Quanta Services (PWR), nVent (NVT); Optical/networking → Arista (ANET), Fabrinet (FN), Coherent (COHR), Marvell (MRVL) |

---

*Sources: SemiAnalysis, Dell'Oro Group, Wing Venture Capital / DataGravity structural bottlenecks analysis, EnkiAI HBM supply crisis 2026, PatSnap HBM landscape 2026, TrendForce InfiniBand vs. Ethernet analysis, Spheron GPU infrastructure world models guide, Vertiv/Schneider/Eaton VaaSBlock analysis, NVIDIA Omniverse/Cosmos newsroom, Labellerr teleoperation guide, BVP world models robotics analysis.*
