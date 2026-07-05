# AV Fleet Scaling — Forced Bill of Materials
## Wave 0 Grounding | Track: Autonomous Vehicles (Engineer View)
**Date:** 2026-07-05
**Horizon:** 6–9 months of non-discretionary spend

---

## Executive Frame

The question is not "when does full autonomy arrive?" The question is: **what does a fleet operator have to buy in the next 6–9 months to keep trucks rolling, robotaxis scaling, and training pipelines fed?** That spend is happening now and is contractually/operationally locked regardless of market sentiment about timelines.

The key operators are: Waymo (robotaxi, ~3,000 vehicles, targeting 1M rides/week), Zoox (custom robotaxi), Aurora Innovation (autonomous trucking, commercially launched on Fort Worth–Houston/El Paso routes), Wayve (UK/EU, end-to-end AI driving model), and embedded automaker AV programs (GM Cruise, Hyundai, Volkswagen CARIAD). Secondary forcing mechanism: Chinese robotaxi players (Baidu Apollo, Pony.ai, WeRide, DiDi) are scaling fast domestically and constitute an equally large demand signal for the same hardware nodes.

**Critical cross-track finding:** AV, humanoid/legged robotics, and world-model labs are converging on the same physical input nodes. LiDAR, edge AI compute (particularly NVIDIA platforms), sensor cleaning, and GPU training clusters are all simultaneously demanded by AV programs, robot manipulator programs, and the world-model foundation model labs building behind them. This demand reinforcement is a key investment signal.

---

## Section 1: Per-Vehicle Forced Nodes

### Node 1 — LiDAR

**What it is:** Solid-state or spinning time-of-flight sensor array providing 3D point clouds at 10–20 Hz. AV programs use 4–5 units per vehicle for 360° coverage.

**Why forced ≤9 months:**
- Waymo 6th-gen Ojai/Zeekr platform uses 4 LiDARs per vehicle. Fleet is scaling from ~3,000 to a stated target of 3,500+ in 2026, with Hyundai reportedly in talks to supply 50,000 IONIQ 5 units. Each vehicle is a locked LiDAR order.
- Aurora is deploying its 2nd-gen commercial hardware kit in Q2 2026 with its proprietary FirstLight LiDAR (now 1,000m range), manufactured by Fabrinet. "Hundreds of trucks" being outfitted in 2026.
- Chinese fleet operators (Baidu, Pony.ai, WeRide) are scaling domestically. Hesai (Chinese, dominant global merchant LiDAR supplier) is **doubling production capacity to 4 million units/year in 2026** from 2 million in 2025. They delivered 1.6M units in 2025 including ~200K+ to robotics.

**Confidence:** HIGH

**Robotics/World-Model Overlap:** YES — STRONG. Hesai's 1.6M 2025 units included ~200K to robotics. NVIDIA selected Hesai as the LiDAR partner for its DRIVE Hyperion 10 reference platform (targets AV + robot deployments simultaneously). World-model labs use LiDAR-derived point clouds as ground truth for spatial world models.

**China/Captive Risk:** HIGH RISK. Hesai is Chinese-domiciled, listed in the US (Nasdaq: HSAI). Two other major suppliers (Innoviz — Israeli, Luminar — US) are smaller in volume. Hesai's share of the global merchant market is dominant, particularly at the price points needed for fleet economics. US/EU customers face supply chain concentration risk and potential sanctions exposure.

---

### Node 2 — Radar (Imaging/4D)

**What it is:** Millimeter-wave radar for velocity measurement and all-weather detection. 6th-gen Waymo uses 6 radar units per vehicle. 4D imaging radar (adds elevation angle) is the new standard vs. traditional 3-beam radar.

**Why forced ≤9 months:**
- Waymo's Zeekr/Ojai platform has 6 radars per vehicle; fleet ramp requires proportional radar procurement.
- Aurora's FirstLight suite includes "imaging radar" as one of three core sensor modalities (alongside LiDAR and cameras). Their 2nd-gen hardware kit launches Q2 2026.
- 4D imaging radar is being adopted by all Tier-1 OEM programs for both ADAS and AV — ZF and Horizon Robotics partnership announced in Nov 2025 specifically for AV radar.

**Confidence:** HIGH

**Robotics/World-Model Overlap:** PARTIAL. Robotics programs (particularly outdoor mobile robots, delivery robots, and legged robots in adverse weather) are beginning to adopt radar, but the overlap is narrower than LiDAR or compute. Warehouse robots generally do not use radar.

**China/Captive Risk:** MEDIUM. Key players include Continental, ZF, Bosch (all European), and Texas Instruments (chipset). Chinese player Huawei/BAIC is developing automotive radar for domestic programs. ZF + Horizon Robotics partnership is a watch item for captive Chinese integration.

---

### Node 3 — Cameras (High-Resolution Automotive)

**What it is:** Calibrated, high-dynamic-range CMOS imagers with automotive qualification (AEC-Q100). Waymo's 6th-gen uses 13 cameras per vehicle (down from 29), but at 17-megapixel resolution described as "a generation ahead of automotive cameras." High pixel count per vehicle remains high.

**Why forced ≤9 months:**
- Every new vehicle off the Zeekr, Hyundai, or Toyota production line needs a full camera suite installed and calibrated. Per-vehicle camera count has decreased but camera quality (and cost) per unit has increased substantially.
- Zoox custom vehicle is camera-dense (proprietary BOM not public, but known to be multi-camera).
- Aurora includes cameras in all commercial hardware kits being deployed in 2026.

**Confidence:** HIGH

**Robotics/World-Model Overlap:** YES — VERY STRONG. This is the single highest-overlap node. Every humanoid/mobile robot uses cameras. Every world-model lab ingests primarily video data. The shift to high-resolution, low-latency egocentric cameras for robot learning is identical to AV camera requirements. Sony (dominant sensor die supplier), ON Semiconductor (supplier of CMOS automotive imagers to Waymo, rumored), and OMNIVISION are simultaneously serving AV, robotics, and surveillance camera markets.

**China/Captive Risk:** MEDIUM-HIGH. Camera CMOS die production is concentrated at Sony (Japan) and OMNIVISION (Chinese-owned since 2016, fabbed at SMIC and TSMC). The module assembly is heavily China-concentrated.

---

### Node 4 — Automotive AI Compute (SoC/Edge Platform)

**What it is:** The central vehicle AI compute platform — responsible for real-time sensor fusion, perception, planning, and actuation. Key platforms are NVIDIA DRIVE Thor (Blackwell-based), Qualcomm Ride, and custom ASICs (Waymo has in-house custom chips, Tesla has HW4/HW5).

**Why forced ≤9 months:**
- NVIDIA DRIVE Hyperion 10 (featuring dual DRIVE AGX Thor SoCs, delivering ~2,000 FP4 TOPS and ~1,000 INT8 TOPS) is the reference platform for L4 deployment. Multiple OEMs and Chinese AV operators are designing programs around it.
- Aurora's Gen 2 commercial kit (Fabrinet-made, Q2 2026) uses a current-gen compute platform. Their Gen 3 kit (AUMOVIO + NVIDIA) uses a bespoke "Super Thor" (dual Thor SoC). Gen 3 production begins H2 2027, but component qualification, tooling orders, and NRE are forced spend **right now** (Q3–Q4 2026 window).
- Waymo uses custom internally designed compute chips (confirmed as of 6th-gen). Not addressable by NVIDIA for Waymo directly, but the broader OEM ecosystem is NVIDIA-dependent.

**Confidence:** HIGH (NVIDIA Drive ecosystem + third-party OEMs); MEDIUM (Waymo custom — captive)

**Robotics/World-Model Overlap:** YES — CRITICAL OVERLAP. NVIDIA Thor and Orin are the same chipsets used in NVIDIA Jetson (robotics edge platform) and the mobile compute nodes for humanoid robots. The Thor SoC is literally described by NVIDIA as a "physical AI" compute platform spanning AV and robotics. This is the single most structurally important cross-track node.

**China/Captive Risk:** MEDIUM. NVIDIA is the dominant supplier; the chip is fabbed at TSMC (Taiwan). Chinese AV players using DRIVE Hyperion add to demand. Domestic Chinese alternatives (Horizon Robotics J6P, Black Sesame A2000) are capturing domestic Chinese market share, reducing Chinese AV customers' dependence on NVIDIA for local deployments — but do not displace NVIDIA in US/EU/global markets.

---

### Node 5 — Sensor Cleaning Systems

**What it is:** Per-sensor fluid jets, mini-wipers, heated housings, and automated cleaning cycles that keep camera, LiDAR, and radar pods clear in rain, snow, dust, and debris. Waymo described designing their cleaning system "from scratch." Zeekr Ojai/RT vehicles have individual wiper blades on each sensor pod.

**Why forced ≤9 months:**
- Waymo is expanding into cold-weather cities (Detroit confirmed, Denver likely) in 2026. These cities have snow, ice, and road salt — environments that immediately disable uncleaned sensors. Cleaning systems are a regulatory and operational prerequisite for those launches.
- The Zeekr RT and Ojai van both have documented automated cleaning systems as standard equipment — this is baked into the vehicle BOM, not optional.
- Fleet expansion into new cities (any precipitation environment) forces sensor cleaning procurement as part of the platform spec.

**Confidence:** HIGH

**Robotics/World-Model Overlap:** PARTIAL. Outdoor mobile robots (delivery, agriculture, inspection) face the same cleaning challenge, but the industrial robotics and world-model-lab segments do not. This is an AV-specific and outdoor-robotics node, not a broad overlap.

**China/Captive Risk:** LOW. Sensor cleaning is a mechanical/fluidic subsystem; suppliers include Kautex Textron (fluid systems) and a range of automotive fluid system manufacturers. No single captive or Chinese dependency.

---

### Node 6 — HD Mapping / Localization Infrastructure

**What it is:** The offline pipeline that builds and maintains high-definition maps (lane geometry, semantics, infrastructure position to centimeter accuracy) that AV systems use for prior localization. Includes survey vehicles, mapping compute, and continuous map update pipelines.

**Why forced ≤9 months:**
- Every new city expansion requires HD map coverage before commercial service can launch. Waymo is launching 9+ new US cities in 2026 plus London and Tokyo (announced). Each launch requires months of mapping runs ahead of commercial deployment.
- Aurora's new Fort Worth–El Paso route required full HD mapping of that corridor. Each new route is a forced mapping campaign.
- Map freshness is a continuous requirement, not a one-time cost. Construction zones, lane changes, and road works require constant map updates — a persistent operational cost with dedicated survey vehicles and processing infrastructure.

**Confidence:** HIGH (forced by city expansion), MEDIUM (cost structure may shift as map-light approaches mature)

**Robotics/World-Model Overlap:** PARTIAL. Some outdoor mobile robots (sidewalk delivery, inspection drones) use HD maps. World-model labs consume HD map data as ground truth. But the operational mapping vehicle fleet requirement is primarily AV-specific.

**China/Captive Risk:** LOW-MEDIUM. Major HD map providers for AV include Here (private, consortium-owned), TomTom, Mobileye's REM (crowdsourced), and proprietary in-house systems. Chinese domestic players use Navinfo and Baidu Maps. Primarily non-Chinese supply chain for Western AV operators.

---

### Node 7 — Vehicle Connectivity / Telematics Hardware

**What it is:** Multi-network cellular modems (4G/5G), vehicle-side antennas, and onboard networking gear that enable real-time telemetry upload, OTA software updates, remote ops command relay, and safety monitoring.

**Why forced ≤9 months:**
- Teleoperation/remote-ops requires continuous bidirectional connectivity with sufficiently low latency (sub-100ms glass-to-glass targets) and bandwidth (multi-camera stream upload).
- OTA software update capability is a regulatory and operational requirement — AV software stacks are updated continuously, and fleet-wide pushes are how calibration and model updates are delivered.
- Waymo's Light Reading article confirms 5G as an active infrastructure layer, though positioned as "background" (telemetry/update, not real-time driving control on the 5G path).

**Confidence:** MEDIUM-HIGH (connectivity is clearly a fleet requirement; the specific per-vehicle hardware is not publicly itemized)

**Robotics/World-Model Overlap:** YES — PARTIAL. Mobile robots and teleoperated robots share cellular connectivity requirements. But the bandwidth/latency requirements for AV are higher than most robot teleoperation use cases.

**China/Captive Risk:** MEDIUM. Cellular modem chipsets are Qualcomm (dominant, US) or MediaTek (Taiwan). Cradlepoint (Ericsson-owned) is a common vehicle router supplier for North American fleets. No Chinese captive risk in the US/EU AV segment.

---

## Section 2: Data Pipeline — Forced Hardware Demand

### Node 8 — Real-World Data Collection Fleet (Mapping + Training)

**What it is:** Purpose-built sensor-laden data collection vehicles (distinct from revenue robotaxis) that drive continuously to generate raw training data. Usually camera + LiDAR heavy, with high-bandwidth onboard storage.

**Why forced ≤9 months:**
- Training a new city requires real-world data *before* the HD map and before the model is adapted to local conditions (different road markings, signage conventions, pedestrian behavior patterns). Data collection vehicles must precede deployment by months.
- The world-model training paradigm (Waymo's GAIA, Google DeepMind's world models, Wayve's PRISM-2) requires diverse real-world driving scenarios at scale. These are not replaceable by simulation alone — real data closes the sim-to-real gap for the "long tail" (rare events, adversarial pedestrian behavior, novel weather).
- Waymo delivered 4 million autonomous miles per week in its commercial fleet alone. Data collection on top of this is additional forced spend.

**Confidence:** HIGH

**Robotics/World-Model Overlap:** YES — STRONG. Real-world embodied data (video from moving platforms) is exactly what world-model foundation model labs need. NVIDIA Cosmos was trained on "20 million hours of real-world data spanning driving scenarios and robotics." AV data collection vehicles are a primary source of that data. This creates a direct AV-to-world-model data pipeline dependency.

**China/Captive Risk:** LOW (the vehicles are generic instrumented platforms; the sensors on them carry the same LiDAR/camera supply chain risks as above).

---

### Node 9 — GPU Training Compute (Data Center)

**What it is:** H100/H200/B200 GPU clusters (typically NVIDIA) used to train perception models, world models, and planner policies on the data collected by the fleet.

**Why forced ≤9 months:**
- Waymo's model refresh cycle is continuous. The shift to 6th-gen Waymo Driver and expanding to 9+ new cities requires retraining or fine-tuning on local data at scale.
- Aurora's 2nd-gen hardware kit (Q2 2026 launch) includes a more powerful compute platform — the software trained on it must be trained on GPUs at scale.
- World-model-based AV training (Waymo GAIA, Wayve PRISM-2, Tesla Dojo equivalent) is memory- and compute-intensive. Scaling from 500K rides/week to 1M rides/week generates proportionally more training data.
- The consensus framework: real fleet data → world model fine-tuning → synthetic "dreamed" scenarios → downstream perception/planner training. Every step requires GPU compute.

**Confidence:** HIGH

**Robotics/World-Model Overlap:** YES — CRITICAL OVERLAP. This is the single node with the broadest and most structurally deep cross-track demand. GPU training clusters are demanded simultaneously by: (1) AV training programs, (2) humanoid robot training programs (GR00T N1, RT-2, π0), (3) world-model foundation model labs (Cosmos, Genie 2, etc.), and (4) general LLM labs. The H100/H200/B200 supply is a shared constraint across all tracks.

**China/Captive Risk:** LOW-MEDIUM for US/EU. NVIDIA supplies the dominant share of training GPUs; TSMC fabricates the silicon. Huawei Ascend and domestic Chinese AI chips (Cambricon, Biren) are alternatives for Chinese players, but not available in Western markets.

---

### Node 10 — Teleoperation / Remote-Ops Infrastructure

**What it is:** Operations centers with staffed human teleoperators who monitor AV fleet vehicles in real time, intervene in edge cases, and generate labeled "demonstration" data. Includes operator workstations, latency-optimized video decode hardware, and secure connectivity infrastructure.

**Why forced ≤9 months:**
- Regulatory requirement in many jurisdictions: a human teleoperator must be reachable for any driverless commercial vehicle. This is not discretionary for commercial deployment.
- Waymo's remote ops model requires round-the-clock coverage across time zones as fleets expand to new cities.
- Teleoperation data is the highest-quality training signal: a human resolving an edge case generates a labeled demonstration that directly feeds the next model iteration.
- Vay Technology (Las Vegas remote-driving fleet) reported nearly 2,000 trips/month and is scaling to 100+ vehicles in 2025. Kodiak Robotics uses Vay tech to supplement Aurora's autonomous ops.

**Confidence:** HIGH (regulatory requirement makes this non-discretionary)

**Robotics/World-Model Overlap:** YES — STRONG. Humanoid robot deployment is moving toward the same model: teleoperator generates labeled demonstrations, robot learns from them. The teleoperation hardware and software stack (workstation, low-latency video pipeline, annotation tooling) is shared architecture. Companies like DriveU and Guident serve both AV and robot remote-ops markets.

**China/Captive Risk:** LOW. Teleoperation centers are primarily staffed ops infrastructure in the deployment country.

---

### Node 11 — Onboard Edge Storage (High-Bandwidth Data Logging)

**What it is:** NVMe SSD arrays or enterprise storage in the vehicle that buffer sensor data (multi-camera 4K, LiDAR point clouds, radar returns) before it is either uploaded or transferred via physical media at depot. Required because uplink bandwidth is insufficient for raw sensor stream upload in real time.

**Why forced ≤9 months:**
- At 13 cameras + 4 LiDARs + 6 radars + audio, a Waymo 6th-gen vehicle generates hundreds of gigabytes per hour. Storage must buffer this for selective upload or depot transfer.
- Fleet scale increase directly proportional to edge storage procurement. 3,000+ vehicles at ~500GB–1TB/vehicle-day is a multi-petabyte daily capture program.

**Confidence:** HIGH (technically inescapable given sensor density)

**Robotics/World-Model Overlap:** YES. High-bandwidth edge storage for humanoid robots is a growing requirement as they become sensor-dense. But the scale per unit in robotics is currently lower than AV.

**China/Captive Risk:** LOW-MEDIUM. Samsung, SK Hynix, Western Digital, and Micron supply automotive-grade NAND. Manufacturing concentration in Korea and Japan. No single Chinese captive dependency in enterprise SSD supply.

---

## Section 3: Discretionary / >9-Month Nodes — KILL or DEFER

### KILL-1 — Vehicle-to-Everything (C-V2X) Infrastructure

**Assessment:** C-V2X (cellular vehicle-to-infrastructure communication) is frequently cited as an AV enabler, but no current commercial AV operator — Waymo, Aurora, or Zoox — discloses V2X hardware as part of their deployed BOM. The FCC only recently began C-V2X spectrum testing; municipal infrastructure deployment is years behind. No commercial fleet is procuring V2X hardware as a fleet requirement in the next 9 months.

**Verdict:** KILL for 6–9 month forced-spend analysis. Discretionary, timeline >3 years for commercial relevance.

### KILL-2 — Aurora Gen 3 "Super Thor" Compute / AUMOVIO Production Facility

**Assessment:** Aurora's Gen 3 hardware kit is explicitly timed for H2 2027 production start (AUMOVIO facility construction completes Q1 2027). The kit targets "tens of thousands of trucks" — a meaningful scale — but the spend horizon is outside the 6–9 month window. Component qualification and NRE are happening now, but the capital spend on actual production inventory and tooling is a 2027 event. **Do not include in the 6–9 month forced node list.**

**Verdict:** KILL for near-term analysis. Flag as a 2027 inflection to track.

### DEFER — High-Fidelity Simulation Platform Expansion

**Assessment:** AV simulation (NVIDIA DRIVE Sim, CARLA, Waymo's internal Sim) is a real spend item, but its forced-spend nature is contested. The current world-model paradigm reduces the need for hand-crafted simulators: Cosmos and similar platforms can synthesize novel scenarios from real data. Sim remains useful for rare-event coverage, but the incremental hardware forced by simulation is primarily GPU compute (which appears under Node 9 above, not as a separate simulation-specific node). Simulation *software* spend is discretionary; the underlying GPU compute spend is already captured.

**Verdict:** DEFER as a standalone node. GPU compute (Node 9) subsumes the hardware component.

---

## Section 4: Cross-Track Overlap Summary

The following nodes have confirmed demand from at least two of: AV programs, mobile/humanoid robotics, world-model foundation model labs.

| Node | AV | Robotics | World-Model Lab |
|---|---|---|---|
| LiDAR | Core | Growing (outdoor) | Ground-truth 3D |
| Cameras (high-res) | Core | Core | Primary modality |
| Automotive/Edge AI Compute (Thor/Orin) | Core | Core (Jetson) | Edge inference |
| GPU Training Compute (H100/H200/B200) | Core | Core | Core |
| Teleoperation Hardware/Stack | Core | Growing fast | Demonstration data |
| Real-World Data Collection | Core | Core | Training corpus |

The strongest single cross-track signal is **NVIDIA's physical AI compute platform** (Thor/Orin), which is literally the same silicon node serving AV, robotics, and world-model inference simultaneously. LiDAR (Hesai/NVIDIA Hyperion 10) is the second strongest signal due to Hesai's confirmed robotics shipments and NVIDIA's formal partnership.

---

## Coverage Gaps

1. **Waymo's proprietary LiDAR supplier identity (6th-gen):** Waymo states their LiDAR uses "custom-designed chips and optical components built in California." The specific chipset supplier and optical assembly partner are not publicly confirmed. This matters because it determines whether Waymo is captive (good for the supply chain) or a source of demand for a merchant supplier.

2. **Per-vehicle BOM cost and component-level supplier detail for Zoox:** Zoox's custom vehicle (bidirectional, purpose-built) has a fully proprietary BOM that Amazon has not disclosed. We do not know who supplies Zoox's LiDAR, radar, or compute.

3. **Wayve's hardware stack:** Wayve (UK, backed by SoftBank, NVIDIA, Microsoft) takes an end-to-end AI model approach and deploys on partner vehicles. Their specific sensor and compute BOM is not public, and their forced hardware spend in 2025–2026 as they expand into new EU markets is not quantifiable from public sources.

4. **Quantitative radar supplier breakdown:** We identified Aurora (FirstLight imaging radar, proprietary), and noted ZF + Horizon Robotics partnership, but the specific radar chipset suppliers (Indie Semiconductor, NXP, TI, Uhnder) and their AV customer relationships are not confirmed in available sources.

5. **Edge storage (onboard) supplier specifics:** The per-vehicle storage architecture (vendor, capacity, form factor) for Waymo 6th-gen and other platforms is not public. This node is technically forced but the investable supplier is unclear.

6. **Chinese AV fleet hardware demand quantum:** Chinese operators (Baidu Apollo, Pony.ai, WeRide, DiDi, AutoX) collectively represent a large and fast-growing demand signal for LiDAR and edge compute, but their fleet sizes, procurement volumes, and BOM specs are disclosed inconsistently. This may be the largest single coverage gap for total demand quantification.

7. **Connectivity hardware specifics:** The specific 5G modem/router hardware in deployed AV fleets (Qualcomm X65 modem? Cradlepoint vehicle router?) is not confirmed in public disclosures. Connectivity is clearly forced but the investable component is unclear.

---

## Sources

- [Waymo 6th-gen launch, fully autonomous ops, 1M rides/week target](https://electrek.co/2026/02/12/waymo-begins-fully-autonomous-ops-with-6th-gen-driver-targets-1m-weekly-rides/)
- [Aurora Innovation shareholder letter Q1 2026 / 8-K](https://www.sec.gov/Archives/edgar/data/0001828108/000182810826000050/aurora26q1shareholderlet.htm)
- [Hesai selected as NVIDIA DRIVE Hyperion 10 LiDAR partner, doubling capacity to 4M units in 2026](https://www.prnewswire.com/news-releases/hesai-selected-by-nvidia-as-lidar-partner-for-nvidia-drive-hyperion-10-to-enable-level-4-fleet-deployment-302653579.html)
- [Zeekr RT sensor cleaning system, tiny wipers detail](https://techcrunch.com/2025/01/07/zeekr-rt-the-robotaxi-built-for-waymo-has-the-tiniest-wipers/)
- [Waymo vs. Zoox fleet comparison and sensor BOM overview](https://automotive-transportation.news-articles.net/content/2026/04/26/waymo-vs-zoox-two-distinct-paths-to-autonomous-fleets.html)
- [Waymo 2025 Year in Review — 15M rides, 4M miles/week](https://www.thedriverlessdigest.com/p/waymos-2025-year-in-review-the-year)
- [NVIDIA Cosmos world foundation model, 20M hours real-world data, AV+robotics overlap](https://www.thundercompute.com/blog/ai-gpu-rental-market-trends)
- [Teleoperation for AV: methodology and best practices](https://adamohq.com/blog/remote-operation-for-autonomous-vehicles-at-low-latency)
- [Autonomous & Self-Driving Vehicle News Nov 2025 — ZF/Horizon Robotics partnership](https://www.autoconnectedcar.com/2025/11/autonomous-self-driving-vehicle-news-waymo-deeproute-ai-aurora-uber-nvidia-borgwarner-holon-glid-technologies-hyundai-motor-group-zf-horizon-robotics/)
- [World Models Race 2026 overview](https://introl.com/blog/world-models-race-agi-2026)
