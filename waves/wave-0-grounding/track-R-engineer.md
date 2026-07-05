# Track R — Engineering Grounding: Humanoid Robot Bill of Materials
## Wave 0 | Author: robotics hardware engineer lens | Date: 2026-07-05

---

## Purpose

Follow FORCED capital spend. ~$55B raised YTD 2026 in robotics. Even companies that fail still spend their cash on hardware first. This memo answers: what must a builder of humanoid/advanced mobile robots physically purchase in the next 6–9 months regardless of ultimate commercial outcome? This is an engineer's BOM, not a market forecast.

Reference platform: full-size bipedal humanoid with dexterous hands, targeting warehouse/factory deployment. BOM baseline: BofA estimate ~$35K/unit (China-sourced) to ~$43K/unit (US small-batch Tesla). Tesla internal target: sub-$20K at mass production. Approximately 28–44 actuators per robot.

---

## 1. ACTUATORS — The Non-Negotiable Core

### 1a. Rotary Actuators (Hip, Knee, Shoulder, Elbow)
- **What it is:** Integrated joint module = frameless torque motor + harmonic or planetary reducer + encoder + torque sensor + local controller PCB. The robot's "muscle." 14–28 rotary joints per robot depending on configuration.
- **Why forced in ≤9 months:** You cannot assemble, test, or iterate on a robot chassis without these. Lead times on custom actuator modules (especially harmonic reducers inside them) run 12–20 weeks. Companies building pilot fleets of 50–500 units must place orders now to have hardware by end of 2026. No actuator = no robot.
- **Confidence:** HIGH
- **Content-$ per robot:** $16,000–$40,000 total actuator stack at current low volumes (40–50% of full BOM). Each high-torque lower-limb actuator: $500–$2,000 unit cost at pilot volumes.
- **China/captive risk:** EXTREME. Green Harmonic holds >60% domestic China share and >35% global share in harmonic reducers; has passed Tesla supply chain verification. Chinese suppliers dominate the planetary roller screw market. Tesla/Figure are building captive actuator lines but are 2–3 years from self-sufficiency on reducers. Most Western builders are China-sourced for gearboxes with no near-term alternative.

### 1b. Harmonic / Strain-Wave Reducers (inside rotary actuators)
- **What it is:** Precision zero-backlash gearbox. The single highest-value sub-component inside the actuator: ~36% of actuator BOM. Each robot needs 14–28. Most expensive single-component category per robot.
- **Why forced in ≤9 months:** Long qualification cycles (3–6 months per supplier). Cannot substitute on the fly — robot kinematics, stiffness, and control loops are tuned to specific reducer specs. If you switch reducer suppliers mid-design you restart motor + controller tuning.
- **Confidence:** HIGH
- **Content-$ per robot:** $5,000–$14,000 embedded in actuator cost above. At pilot volumes, individual harmonic drive: $200–$800 each.
- **China/captive risk:** HIGH. Green Harmonic (Shenzhen) dominant. Nabtesco (Japan) and Harmonic Drive AG (Germany/Japan) are alternatives but at higher cost and longer lead times. No US-domestic volume supplier.

### 1c. Planetary Roller Screws (Linear Actuators — Knee/Ankle Extension, Spine)
- **What it is:** High-efficiency mechanism converting motor rotation to linear motion for load-bearing joints. Superior to ball screws in life and load. Used in 6–14 linear actuator joints per robot.
- **Why forced in ≤9 months:** Lower-limb locomotion requires these for knee/ankle extension forces. No roller screw = bipedal walking impossible at the torque levels required.
- **Confidence:** HIGH
- **Content-$ per robot:** $1,500–$4,000 total embedded in linear actuator assemblies.
- **China/captive risk:** HIGH. Chinese suppliers (e.g., Lian Bao, Ruili) dominate volume production. Bosch Rexroth and SKF produce them but at 2–3x cost and in limited humanoid-appropriate sizes.

---

## 2. MOTORS

### 2a. Frameless Torque Motors (BLDC)
- **What it is:** Rotor + stator only, no housing/shaft/bearing. Maximizes torque density and minimizes volume. Motor accounts for ~13.5% of individual actuator BOM. Each robot uses 28–44.
- **Why forced in ≤9 months:** Every actuator requires one. These are custom-wound to specific robot joint torque/speed specs — not off-the-shelf. Winding changes require a new procurement cycle.
- **Confidence:** HIGH
- **Content-$ per robot:** $2,500–$6,000 total motor content across all joints.
- **China/captive risk:** MEDIUM-HIGH. Large-volume BLDC production heavily in China (e.g., T-Motor, Maxon has Swiss capacity). Some volume production in Taiwan and Korea. Less concentrated than harmonic drives.

### 2b. Micro Motors for Dexterous Hands
- **What it is:** Sub-16mm diameter brushless DC or coreless motors driving finger joints. Each dexterous hand has 11–15 DOF; 2 hands = 22–30 micro motors minimum.
- **Why forced in ≤9 months:** Without dexterous hands, robots cannot perform manipulation tasks — the stated commercial use case. Hand is current industry "Mount Everest." All builders racing to demonstrate grasping capability by end of 2026.
- **Confidence:** HIGH
- **Content-$ per robot:** ~$3,000–$8,000 per hand pair at current volumes. Whole dexterous hand assembly: ¥tens of thousands RMB each.
- **China/captive risk:** HIGH. Faulhaber (Germany) and Maxon (Switzerland) are reference-quality suppliers; volume Chinese equivalents (e.g., ZHAOWEI) growing rapidly but QC uncertainty. Micro motor production heavily China-concentrated.

---

## 3. SENSING

### 3a. 6-Axis Force/Torque (FT) Sensors — Wrists and Ankles
- **What it is:** Measures full 3D force + 3D torque vector simultaneously. Wrist FT enables grasp force control; ankle FT feeds balance/terrain adaptation controllers. Typically 4 per robot (2 wrists + 2 ankles), sometimes 6.
- **Why forced in ≤9 months:** Safety-critical for deployment in human environments — without wrist FT, robot cannot modulate grasp force and will crush objects/people. Ankle FT is required for stable bipedal locomotion on uneven surfaces. No shortcuts here.
- **Confidence:** HIGH
- **Content-$ per robot:** FT + joint torque sensors together: ~15% of full BOM = ~$5,000–$6,500. Individual 6-axis FT sensor: $500–$2,000 at current volumes (prices dropping from >$3,000 as humanoid volumes scale — 36kr reports "hundreds of yuan level" target for China-made units).
- **China/captive risk:** MEDIUM. ATI Industrial Automation (USA), Robotiq (Canada), Sunrise Instruments (China) are primary suppliers. Bosch MEMS FT IC not in production until 2028–2031. China rapidly scaling lower-cost FT sensor supply.

### 3b. Joint Torque Sensors / Encoders
- **What it is:** Per-joint torque measurement (strain gauge or inductive) + position encoder (magnetic absolute, incremental). 28 joints = 28 sensor channels minimum.
- **Why forced in ≤9 months:** Required for impedance/torque control — the safety-critical "feel" of the robot. Hard to retrofit after actuator is assembled; must be spec'd at actuator design time.
- **Confidence:** HIGH
- **Content-$ per robot:** Embedded in the ~15% sensor BOM share above.
- **China/captive risk:** MEDIUM. Multiple encoder suppliers (RLS, Broadcom AVAGO, Tamagawa Seiki). Inductive encoders increasingly China-produced.

### 3c. IMUs (Inertial Measurement Units)
- **What it is:** 6-DOF accelerometer + gyro, often 9-DOF with magnetometer. Humanoids run 2–5 IMUs for body orientation, pelvis, and head. State estimation backbone for all locomotion.
- **Why forced in ≤9 months:** Balance control is impossible without reliable IMU. Every robot needs them on day one of chassis testing.
- **Confidence:** HIGH
- **Content-$ per robot:** Low — $50–$300 total IMU spend. High-performance tactical-grade IMUs (e.g., Analog Devices ADIS series) run $200–$500 each but most robots use consumer-grade MEMS ($10–$50). Not a major cost node.
- **China/captive risk:** LOW-MEDIUM. Bosch Sensortec, ST Micro, InvenSense (TDK), Analog Devices all supply. Well-diversified.

### 3d. Depth Cameras / Stereo Vision
- **What it is:** Intel RealSense-class or proprietary stereo + structured light for hands and navigation. Typically 2–4 cameras per robot (head, chest, wrists). One depth camera in BofA baseline BOM.
- **Why forced in ≤9 months:** Required for object detection and dexterous grasping. Robots operating in unstructured environments need perception on day 1 of pilot deployment.
- **Confidence:** HIGH
- **Content-$ per robot:** $500–$2,000 total camera/vision stack depending on count and spec. Individual depth camera: $100–$500.
- **China/captive risk:** MEDIUM. Intel RealSense (USA), Microsoft Azure Kinect (discontinued). Chinese alternatives (Orbbec, AUSB) gaining ground. Sony IMX series sensors dominate the underlying image sensor.

### 3e. LiDAR (Navigation)
- **What it is:** Typically one solid-state or spinning LiDAR for navigation/SLAM. BofA baseline includes one per robot.
- **Why forced in ≤9 months:** Not universal — some builders (Figure, Tesla) are camera-only (pure vision navigation). Agility Digit uses LIVOX LiDAR.
- **Confidence:** MEDIUM — depends on architecture choice. Vision-only builders skip this.
- **Content-$ per robot:** $200–$1,500 depending on type (solid-state MEMS vs spinning).
- **China/captive risk:** HIGH IF used. Hesai, Robosense, and Livox (DJI) dominate. QUANERGY and Luminar are US alternatives at higher cost. The mid-range solid-state segment is ~80% China-sourced.

### 3f. Tactile Skin / Array Sensors
- **What it is:** Distributed pressure/contact sensing across fingertips, palms, potentially forearms. Capacitive, optical (GelSight-style), or piezoresistive arrays.
- **Why forced in ≤9 months:** PARTIALLY FORCED. Fingertip tactile needed for dexterous manipulation tasks (assembly, handling deformable objects). But full-body tactile skin is NOT required for pilot deployments — only hand/fingertip coverage matters near-term.
- **Confidence:** MEDIUM (fingertip tactile HIGH; body skin LOW for ≤9 months)
- **Content-$ per robot:** Currently >$10,000 for full systems; fingertip-only likely $2,000–$5,000. Prices falling rapidly but remain a major cost item.
- **China/captive risk:** LOW-MEDIUM for current commercial units. Most tactile sensor suppliers are small specialty firms (SynTouch USA, Weiss Robotics Germany, startup ecosystem). China catching up quickly.

---

## 4. EDGE COMPUTE / ONBOARD AI

### 4a. Main Compute (SoC / GPU Module)
- **What it is:** Onboard inference platform for perception, planning, and motor control. NVIDIA Jetson Thor is the emerging de facto standard; some builders (Tesla) use custom silicon (FSD derivative). ADI announced Jetson Thor adoption in August 2025. Jetson Thor: ARM CPU + next-gen GPU + NVLink for multi-camera pipelines.
- **Why forced in ≤9 months:** Every robot needs an inference brain. Without onboard AI compute, robot cannot process camera feeds or run learned manipulation policies in real time. Jetson Thor orders placed now for H2 2026 delivery.
- **Confidence:** HIGH
- **Content-$ per robot:** $500–$2,000 for Jetson-class module. Tesla custom SoC: captive, cost not disclosed.
- **China/captive risk:** MEDIUM-HIGH. NVIDIA Jetson is US-designed but TSMC-fabricated. Export control risk if US-China tensions escalate. Tesla captive. Some Chinese builders (Unitree, UBTECH) using Rockchip or Qualcomm alternatives.

### 4b. Motor Driver / Real-Time Control Electronics
- **What it is:** Per-joint or per-limb servo driver boards (FPGA + power electronics). Runs at 1–4 kHz control loops. Often custom-designed by the robot maker.
- **Why forced in ≤9 months:** Control electronics are the most customized part of the electronic stack. PCB layout, firmware, and qualification take 4–6 months. Boards must be ordered at PCB fab 8–12 weeks before robot assembly starts.
- **Confidence:** HIGH
- **Content-$ per robot:** $1,000–$3,000 total (distributed across 4–6 limb controller boards).
- **China/captive risk:** MEDIUM. PCB fabrication heavily in China (JLCPCB, etc.). Power electronics (GaN FETs, gate drivers) from Texas Instruments, STMicro, Infineon — globally diversified fabs but assembly China-concentrated.

---

## 5. POWER / BATTERY

### 5a. Battery Pack (Li-ion or LiFePO4)
- **What it is:** High-density rechargeable pack, typically 400–1,000 Wh, packaged in torso/pelvis. Must support 30–90 min continuous operation. Hot-swap architecture becoming standard (UBTech Walker S2 achieved autonomous swap in 2025).
- **Why forced in ≤9 months:** No power = no robot. Hot-swap is now a competitive requirement for 24-hour factory operation. Custom pack form factor requires cell procurement + BMS + mechanical design — 3–6 month lead from cell order to validated pack.
- **Confidence:** HIGH
- **Content-$ per robot:** $1,500–$4,000 at current cell prices (~$100–$120/kWh for 18650 or prismatic LFP). High-performance cylindrical cells (21700) preferred for energy density.
- **China/captive risk:** EXTREME. CATL and BYD dominate cell supply globally. 18650/21700 cylindrical cells: >70% China production. No near-term alternative at scale.

### 5b. Battery Management System (BMS)
- **What it is:** Electronics monitoring cell voltage, temperature, state-of-charge, and protection. Usually custom or semi-custom for robot form factor.
- **Why forced in ≤9 months:** Embedded in battery pack development timeline above.
- **Confidence:** HIGH
- **Content-$ per robot:** $200–$600 BMS electronics.
- **China/captive risk:** MEDIUM. Texas Instruments, Analog Devices for BMS ICs. Assembly in China.

---

## 6. STRUCTURAL / MECHANICAL

### 6a. High-Strength Lightweight Structure (Carbon Fiber / Aluminum Alloy)
- **What it is:** Robot chassis, limb links, spine, pelvis — structural members. Carbon fiber reinforced polymer (CFRP) for arms; aerospace aluminum (6061/7075) or titanium for load-bearing joints.
- **Why forced in ≤9 months:** You need a chassis before any electronics goes in. CFRP layup is 6–14 week lead time; CNC aluminum is shorter. Robot link geometry is often revised between hardware versions, requiring new tooling.
- **Confidence:** HIGH
- **Content-$ per robot:** $1,500–$4,000 structural materials + machining.
- **China/captive risk:** MEDIUM. CFRP materials from Hexcel (USA), Toray (Japan). Chinese CFRP growing. CNC machining: global but heavily China-sourced for cost.

### 6b. Cable Harnesses / Tendon Routing
- **What it is:** Spectra/Dyneema cable tendons for hand actuation (remote motor + tendon-driven fingers), plus electrical wiring harnesses throughout the body.
- **Why forced in ≤9 months:** Tendons are design-specific; routing through the hand and arm requires custom fabrication. High-failure-rate component in early prototypes — redundant supply essential.
- **Confidence:** HIGH
- **Content-$ per robot:** $300–$800.
- **China/captive risk:** LOW. Commodity materials but assembly is custom.

---

## 7. DATA INFRASTRUCTURE (Training & Teleoperation)

### 7a. Teleoperation Rigs (Physical)
- **What it is:** Exoskeleton-style upper body rig or bimanual hand controllers worn by a human operator to puppeteer the robot in real time, recording state + action pairs for imitation learning. Examples: wrist-mounted controllers, full arm exoskeletons, VR glove+controller combos. Used to collect 500–5,000 demonstration episodes per manipulation skill.
- **Why forced in ≤9 months:** Simulation alone cannot close the sim-to-real gap for dexterous manipulation on real objects. Every serious manipulation lab (Physical Intelligence, Skild, Apptronik, Figure) is running active teleoperation data collection programs. A fleet of 10–50 teleoperation rigs per company is necessary to generate enough real-world data for policy training. ICRA 2026 "Beyond Teleoperation" workshop confirms this remains the dominant real-world data collection method.
- **Confidence:** HIGH — teleoperation hardware demand is REAL and current.
- **Content per rig:** $5,000–$30,000 per teleop rig. A 20-rig fleet = $100K–$600K. Not per-robot but per-lab.
- **China/captive risk:** LOW-MEDIUM. Mostly proprietary or assembled from off-the-shelf components.

### 7b. GPU Compute Infrastructure (Training Cluster)
- **What it is:** Dense GPU servers (NVIDIA H100/H200/B200) for training world models, visuomotor policies, and generative sim data. NVIDIA GR00T and Isaac Sim run on Blackwell-class GPUs. Companies like Axe Compute deploying B300 clusters for robot training.
- **Why forced in ≤9 months:** You cannot train competitive manipulation policies without GPU compute. This is the direct connection between robot builders and NVIDIA's hyperscale infrastructure business. Capital-rich robot startups (Figure at $39B valuation, Apptronik at $5B) are procuring or contracting GPU time immediately after funding rounds.
- **Confidence:** HIGH
- **Content per company (not per robot):** $5M–$100M+ annually in compute spend for a well-funded robot lab. This is lab-level capex, not per-unit.
- **China/captive risk:** LOW (NVIDIA dominates training). Export controls restrict H100/H200 to China.

### 7c. Simulation Platform (Software + Synthetic Data Generation)
- **What it is:** NVIDIA Isaac Sim / Omniverse, custom simulators (MuJoCo-based), Agibot's Genie Sim 3.0. Generates synthetic training data at scale. At CES 2026, Agibot released >10,000 hours of open-source synthetic data covering 200+ tasks.
- **Why forced in ≤9 months:** Required complement to real teleoperation data, particularly for locomotion and whole-body control. However, for dexterous manipulation the sim-to-real gap means simulation is supplementary, not a replacement for physical data collection rigs.
- **Confidence:** HIGH for GPU infrastructure; MEDIUM for specific sim platform spend (many open-source options).
- **Content per company:** Infrastructure cost embedded in GPU compute above.
- **China/captive risk:** LOW. NVIDIA Omniverse US-controlled. Open source alternatives global.

---

## 8. NODES ASSESSED AS DISCRETIONARY / DEFERRABLE (KILL LIST)

### KILL 1: Full-Body Tactile Skin
- **Reason to defer:** Fingertip tactile is forced; whole-body skin is not needed for warehouse/factory deployment in ≤9 months. Current commercial deployments (Amazon/BMW pilots) do not require full-body tactile. Technology not mature and costs >$10K/robot for full coverage. No production-ready supplier at scale.
- **Verdict:** DEFER. Flag for 2027–2028 when manipulation use cases expand beyond structured tasks.

### KILL 2: High-End LiDAR (for vision-first builders)
- **Reason to defer:** Tesla, Figure, and Skild are camera-only or camera-primary navigation architectures. LiDAR adds $200–$1,500 per robot but is not needed if your navigation policy runs on cameras. Agility uses it; others skip it. For a camera-first architecture, this is optional.
- **Verdict:** ARCHITECTURE-DEPENDENT. Kill for camera-first builders; retain only for Agility-style SLAM-heavy designs.

### KILL 3: Full Autonomy Edge Inference Stack (Custom Silicon)
- **Reason to defer:** Custom neuromorphic or ASIC edge AI chips for robot inference are 2028+ products. Jetson Thor is sufficient for current generation. Custom silicon NRE costs are $50M+ and timelines are 3+ years. No builder outside Tesla should be spending on this now.
- **Verdict:** DEFER for all non-Tesla builders. Use Jetson Thor.

---

## 9. FORCED CAPITAL SPEND SUMMARY MAP

| Priority | Node | Forced? | $/Robot | Key Risk |
|---|---|---|---|---|
| 1 | Rotary actuators (full module) | FORCED | $16K–$40K | China reducer supply |
| 2 | Harmonic/strain-wave reducers | FORCED (inside actuators) | $5K–$14K | Green Harmonic monopoly |
| 3 | Dexterous hand assembly | FORCED | $3K–$8K/pair | Design not converged; high cost |
| 4 | Force/torque sensors (wrist+ankle) | FORCED | $2K–$6.5K | FT sensor supply scaling |
| 5 | Battery pack + BMS | FORCED | $1.7K–$4.6K | CATL/BYD cell dominance |
| 6 | Edge compute (Jetson Thor) | FORCED | $500–$2K | TSMC fab; export control |
| 7 | Structural chassis (CFRP/Al) | FORCED | $1.5K–$4K | Tooling lead times |
| 8 | Planetary roller screws | FORCED | $1.5K–$4K | China dominated |
| 9 | Depth cameras / stereo vision | FORCED | $500–$2K | Intel exit from RealSense |
| 10 | Joint torque sensors + encoders | FORCED | embedded in FT | Multiple suppliers |
| 11 | IMUs | FORCED | $50–$300 | Well-diversified |
| 12 | Motor drivers / servo electronics | FORCED | $1K–$3K | PCB fab China-concentrated |
| 13 | Teleoperation rigs (lab-level) | FORCED (lab capex) | $100K–$600K/lab | Proprietary; small suppliers |
| 14 | GPU training compute (cloud/on-prem) | FORCED (lab capex) | $5M–$100M+/yr | NVIDIA near-monopoly |
| 15 | LiDAR | ARCHITECTURE-DEPENDENT | $200–$1.5K | China-dominated (Hesai/Livox) |
| 16 | Full-body tactile skin | DEFER past 9 mo | >$10K if deployed | No volume supplier |
| 17 | Custom edge AI ASIC | DEFER 2028+ | $50M+ NRE | Only Tesla justified |

---

## 10. HIGHEST-VALUE / HARDEST-TO-SUBSTITUTE NODES

In order of substitution difficulty and investment relevance:

1. **Harmonic / strain-wave reducers** — Green Harmonic has near-monopoly; 3–6 month qualification per supplier; robot kinematics locked to reducer choice. Hardest to substitute.
2. **Planetary roller screws** — Long lifespans required; precision tolerance; Chinese volume producers have 2–3 year head start.
3. **6-Axis FT sensors** — MEMS-scale FT ICs not in production; custom mechanical designs; Bosch not in market until 2028+.
4. **Dexterous hand assembly (integrated module)** — No standard; every builder doing custom; micro-motor + reducer + tendon integration not commoditized.
5. **Battery cells** — CATL/BYD cell supply for custom-form humanoid packs; no Western alternative at volume.
6. **Onboard GPU compute (Jetson Thor)** — NVIDIA de facto standard; custom silicon 3+ years away for non-Tesla.

---

## 11. WHERE CHINA DOMINATES vs. CAPTIVE PRODUCTION

| Component | China Dominance | Captive/In-House |
|---|---|---|
| Harmonic reducers | Green Harmonic >60% China, >35% global | None at scale outside Japan/Germany |
| Roller screws | Chinese volume suppliers dominant | None |
| Battery cells | CATL/BYD >70% global | Tesla (Panasonic/4680) |
| LiDAR | Hesai, Robosense, Livox ~80% mid-range | None |
| Actuator modules | China assemblers dominant by volume | Tesla (partial), Figure (targeting) |
| Micro motors (hands) | Heavy China concentration | None |
| PCB fabrication | China assembly dominant | None |
| Edge compute | China restricted (NVIDIA export controls) | Tesla (FSD derivative) |

---

## 12. DATA SIDE: IS PHYSICAL DATA COLLECTION HARDWARE DEMAND REAL?

**Verdict: YES — physical teleoperation hardware demand is REAL and not offset by simulation for ≤9 month horizon.**

Engineering rationale:
- Simulation closes the locomotion gap adequately (randomization over terrain, gravity, friction). Locomotion policies trained in IsaacSim transfer to hardware with reasonable fine-tuning.
- **Simulation does NOT close the dexterous manipulation gap in 9 months.** Contact dynamics, deformable objects, and novel object appearance all require real sensor data to ground the policy. The ICRA 2026 "Beyond Teleoperation" workshop explicitly flags this as an open problem.
- Current production pipeline (per field reports): sim for locomotion + exoskeleton/teleoperation for manipulation + egocentric video for scene priors.
- A 20-rig teleoperation fleet collecting 1,000 episodes/skill at 10 min/episode needs 4–8 months of active collection to cover a useful skill library. Companies must deploy these rigs now to have data ready for 2027 pilots.
- Agibot's 10,000+ hours of synthetic data at CES 2026 shows simulation is supplementary at scale — but fine-tuning on real robot data remains necessary.

**Physical data collection hardware IS a near-term forced spend item, particularly for manipulation-focused builders.**

---

## Coverage Gaps

The following areas have lower engineering confidence due to insufficient public sourcing:

1. **Tier-2/Tier-3 supplier specifics for US builders** — Figure AI, Apptronik, and Agility do not publicly disclose component-level procurement. Actuator and reducer supplier names for US builders (except Tesla/Green Harmonic link) are not confirmed in available sources.

2. **Dexterous hand micro-motor specifications and suppliers** — Cost estimates are directionally correct but specific supplier qualification status for production rigs is opaque. Which Chinese micro-motor suppliers have passed US builder audits is not public.

3. **Cable tendon durability and failure rates** — A high-failure-rate component in early iterations; field MTBF data not public. This could be a larger ongoing consumable spend than the BOM suggests.

4. **Battery form factor and chemistry choices by builder** — Only UBTech's hot-swap architecture is public in detail. Figure, Apptronik battery configurations not publicly confirmed.

5. **NVIDIA Jetson Thor pricing at OEM volume** — Module pricing at 1,000+ unit volumes not public. Likely $400–$800 at volume vs. $800–$1,500 at dev-kit pricing.

6. **Teleoperation rig fleet sizes by company** — Lab-level capex per company not disclosed. The $100K–$600K/lab range is an estimate based on rig unit costs, not disclosed fleet sizes.

7. **Export control implications for actuator sub-components** — Whether US BIS controls apply to specific harmonic reducer or roller screw imports from China is not analyzed here. A tariff/export control escalation scenario could materially change BOM costs for US builders.

8. **Soft robot / pneumatic alternatives** — A minority of labs (e.g., some of Agility's earlier designs) use hydraulic or pneumatic actuation. This BOM assumes electric actuation as the dominant architecture, which is accurate for >90% of 2025–2026 builds but not universal.

---

*Sources: BofA Global Research (Humanoid Robots 101, April 2025), Interact Analysis 2025, 36kr English (harmonic reducer market share, motor counts), Yole Group Humanoid Robots 2026, IDTechEx Humanoid Robots 2025–2035, Bloomberg (Chinese shipments 2025), Carnegie Endowment (Embodied AI China 2025), NVIDIA ADI Jetson Thor press release (August 2025), ICRA 2026 Beyond Teleoperation Workshop, Agibot CES 2026 Genie Sim 3.0, DIGITIMES Humanoid Robotics 2025.*
