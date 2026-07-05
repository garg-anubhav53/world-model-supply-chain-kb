# Track R — Robotics/Physical-AI Supply Chain Grounding
**Wave 0 | Date: 2026-07-05 | Analyst: Supply-Chain Bot**

> Purpose: Map where forced capex from humanoid/advanced-robot builders (Figure, Apptronik, Neura, Skild, Boston Dynamics, Agility, Unitree) lands across the component and data-infrastructure stack. Identify chokepoints, leakage (China-dominated, captive/vertical-integration, private-only), and which nodes have accessible US/international public equity exposure.

---

## Macro Framing

**China's structural grip:** Chinese suppliers hold ~63–70% of the humanoid supply chain by component category and have a ~3× cost advantage on a fully "de-Chinaed" BOM. The Tesla Optimus BOM rises from ~$46K to ~$131K if China is removed. China's April 2025 rare-earth export controls have already disrupted production at multiple builders (Ford halted a plant; Elon Musk publicly cited Optimus constraint). This is the single largest systemic risk to Western public equity accessibility.

**BOM concentration:** Actuators + transmission represent ~50% of BOM; dexterous hands ~31% (overlapping category). All other sensing, compute, and power are the remainder.

**Volume ramp signal (demand):** Tesla targeting 5,000 Optimus 2025 → 100,000 by 2026; Agility ~10,000 units/yr plant; BYD 1,500 → 20,000; Agibot 5,000 (2025). Goldman Sachs notes costs fell 40% YoY (vs. 15–20% projected), accelerating adoption.

---

## Node-by-Node Supply Chain Map

---

### 1. Actuators & Brushless DC / Torque Motors

**Description:** The dominant cost node (~50% of BOM). Each humanoid has 20–40 actuator joints. Requires frameless torque motors combined with gear reduction.

**Vendor categories & named vendors:**
- *European automotive incumbents:*
  - **Schaeffler** (SDAX: SHA) — signed 3 humanoid actuator partnerships in 5 months (Neura, Humanoid UK, Leju). Developing integrated joint modules (motor + reducer + encoder + controller in one housing, debuted CES 2026).
  - **Bosch** (private GmbH for robotics division) — partnership with Neura covering motor production; broader industrial motors portfolio.
- *Japanese precision motion:*
  - **Nidec** (TSE: 6594) — FLEXWAVE strain-wave reducer + frameless motors; explicit humanoid positioning.
  - **Yaskawa** (TSE: 6506) — servo drives and motors; industrial-robot heritage now extending to humanoid supply.
  - **Panasonic** (TSE: 6752) — servo motor supplier.
- *US/European component makers:*
  - **Timken** (NYSE: TKR) — TwinSpin and DriveSpin actuators (2nd-largest Timken segment).
  - **Nidec Motion & Drives** (also NYSE via ADR) — multiple product lines.
- *Chinese challengers:*
  - Estun Automation, Inovance Technology, Greatoo, Leader Drive (Leaderdrive) — all SZSE/SSE listed; dominating volume supply for domestic builders and gaining Tesla Optimus slots.

**Chokepoint:** Moderate-to-high. High-precision frameless torque motors suitable for humanoid joints are manufactured by a small number of qualified vendors. The critical capability is achieving the torque density + precision + thermal performance in package. Schaeffler's integrated joint module approach is creating a new type of chokepoint (fully integrated joint = single-vendor lock-in).

**Captive/vertical-integration risk:** HIGH. Tesla is designing custom actuators in-house (Optimus Gen 3). Figure AI, Boston Dynamics (Hyundai), and Agility are all doing varying degrees of in-house motor/actuator design. Custom in-house designs reduce merchant market TAM.

**China leakage:** HIGH. Chinese suppliers (Leaderdrive, Shuanghuan, Inovance, Estun) are winning Optimus, Unitree, Agibot slots. Their share of harmonic reducer market went from ~15% (2022) to ~38% (Q1 2024).

**Accessibility for US public equity:** PARTIAL. Schaeffler (German, listed), Nidec (Japanese, listed), Timken (US, NYSE) are genuine beneficiaries. But Chinese suppliers are capturing the volume ramp; captive designs reduce merchant TAM further.

---

### 2. Harmonic & Strain-Wave Reducers

**Description:** High-precision zero-backlash gear reduction used in robot wrist, elbow, shoulder joints. Each humanoid requires 20–40 units.

**Vendor categories & named vendors:**
- *Global incumbents:*
  - **Harmonic Drive Systems** (TSE: 6324) — original creator, ~85% strain-wave share in 2023, now rapidly losing to Chinese challengers.
  - **Nabtesco** (TSE: 6268) — dominant in RV/cycloidal reducers (~60% of RV market); doubling capacity by 2026; acquired Spinea (Slovakia) 2023.
  - **Nidec Drive Technology** (part of Nidec TSE: 6594) — FLEXWAVE product line.
  - **Cone Drive** (private, US-based) — emphasizing "US-made" strain wave + cycloidal pairing for humanoid hips/knees/wrists. No public equity route.
  - **Wittenstein** (private, Germany) — high-precision planetary gearboxes for robot joints.
  - **Sumitomo Drive Technologies** (Sumitomo Heavy Industries, TSE: 6302) — cycloidal gear heritage.
  - **THK** (TSE: 6481) — linear motion + ball screws; also precision reducers.
- *Chinese challengers (listed on Chinese exchanges):*
  - **Leaderdrive / Leader Harmonious Drive Systems** (SZSE: 688017) — ~38% global harmonic market by Q1 2024; Tesla validated.
  - **Zhejiang Shuanghuan Driveline** (SZSE: 002472) — supplies Optimus + Unitree; 500,000-unit/yr Suzhou plant opening 2026.
  - **Ningbo Zhongda Leader** (SZSE: 002896) — named Figure AI reducer supplier.

**Chokepoint:** HIGH. Very few vendors globally can produce strain-wave gearing at humanoid precision specs. Leaderdrive's ascent creates a new quasi-monopoly at the price point builders want.

**Captive risk:** MODERATE. Some builders (Boston Dynamics, Tesla) designing custom integrated joints, but the underlying harmonic element is typically still sourced externally.

**China leakage:** VERY HIGH. Chinese suppliers have structurally displaced incumbents in less than 3 years. For US/Japan equity investors, this node is mostly leaking to China.

**Accessibility for US public equity:** POOR. Best accessible name is **Harmonic Drive Systems** (Tokyo) or **Nabtesco** (Tokyo). No US-listed pure-play. Chinese winners are on Chinese exchanges. Cone Drive is private. Accessibility is partial (via Japanese ADRs) but the volume story is in China.

---

### 3. Force-Torque (F/T) Sensors

**Description:** 6-axis wrist/ankle sensors enabling compliant control, payload monitoring, and safety. Typically 1–4 per humanoid. Currently $2,000–$8,000/unit; a MEMS-IC disruption to $10–$50 is possible but has not yet reached production.

**Vendor categories & named vendors:**
- **ATI Industrial Automation** (acquired by Novanta, NASDAQ: NOVT) — market leader in robot F/T sensors; military/surgical/industrial heritage. Parent Novanta is a US-listed mid-cap.
- **Bota Systems** (private, Swiss — ETH Zurich spinout) — SensONE 6-axis, robotics-focused, IP65, EtherCAT; widely adopted in research-grade and advanced industrial humanoids.
- **OnRobot** (private, Danish) — broader end-of-arm tooling portfolio including F/T sensors; D:Ploy platform.
- **Robotiq** (private, Canadian) — FT 300-S, popular on UR arms.
- **Kistler** (private, Swiss) — precision piezo/strain-gauge sensors, industrial standard.
- **GelSight** (private, MIT spinout) — optical gel-based tactile sensing (see Node 4 below).
- MEMS-IC F/T sensors: no production vendor identified yet (2025–2026); first merchant MEMS F/T IC would be a transformative supply-chain event comparable to the first automotive-qualified MEMS gyroscope.

**Chokepoint:** MODERATE-HIGH. ATI/Novanta dominates certified high-performance F/T. The market is fragmented at research grade, consolidated at production grade.

**Captive risk:** MODERATE. Builders are experimenting with in-house strain-gauge bridges for cost reasons. Tesla is believed to use custom ankle torque sensing in Optimus.

**China leakage:** LOW-MODERATE. Not yet China-dominated at the certified performance tier. Chinese sensor startups exist but have not yet won major humanoid production slots.

**Accessibility for US public equity:** GOOD (best single node). **Novanta (NOVT)** is the clearest US-listed pure-play with ATI F/T in its portfolio. Private players (Bota, OnRobot, Robotiq, Kistler) are not accessible.

---

### 4. Tactile / Pressure Sensors (Robot Skin)

**Description:** Distributed pressure sensing for dexterous hands and contact surfaces. Dexterous hands = ~31% of BOM; tactile skin is the enabling layer for manipulation. This is the hardest technical bottleneck in humanoid robotics.

**Vendor categories & named vendors:**
- **XELA Robotics** (private, Japan — Waseda University spinout) — uSkin magnetic-based tactile sensors; flexible; ROS/ROS2 compatible; showing at multiple 2026 exhibitions; received new strategic funding 2025–2026.
- **GelSight** (private, MIT spinout) — optical gel-based; strong on fine-texture sensing and slip detection.
- **Pressure Profile Systems (PPS)** (private, US) — tactile array sensors.
- **SynTouch** (private, US) — biomimetic tactile sensing; research-grade.
- **Meta AI** — developing foundation tactile-sensor models for humanoid robotics (internal/captive research; not a merchant product).
- **BeBop Sensors** (private, US) — fabric-based pressure sensing for gloves/grippers.
- HaptX (private, US) — haptic gloves for teleoperation (Node 12 overlap).

**Chokepoint:** HIGH. No volume-production tactile skin vendor exists at scale. This is a known supply-chain gap—humanoid builders are either sourcing research-grade (XELA, GelSight) or doing in-house development.

**Captive risk:** HIGH. Tesla, Apptronik, Figure, and others are building proprietary dexterous hand/tactile systems. This is viewed as a strategic moat differentiation.

**China leakage:** LOW. Chinese tactile sensor suppliers exist but have not won humanoid production validation yet.

**Accessibility for US public equity:** POOR. Essentially all named vendors are private. Novanta (NOVT) has minor exposure here via its broader sensor portfolio. No clean public equity access point.

---

### 5. IMUs / MEMS Inertial Sensors

**Description:** 6-axis (or 9-axis) inertial measurement units for robot pose estimation, gait stabilization, balance control. Each humanoid uses 2–8 IMUs. Typically $5–$50/unit at volume.

**Vendor categories & named vendors:**
- **TDK / InvenSense** (TDK: TSE 6762) — ICM-42688-P 6-axis IMU; SmartEdgeML on-chip ML; dominant in high-volume consumer + robotics. TDK is Tokyo-listed; InvenSense is a TDK subsidiary.
- **Bosch Sensortec** (private, subsidiary of Bosch GmbH) — BMI series; strong in mobile/IoT; expanding to industrial robotics.
- **STMicroelectronics** (NYSE: STM) — LSM6DSO series; broad industrial presence; US-listed Swiss company.
- **Analog Devices** (NASDAQ: ADI) — ADIS series (tactical/precision IMUs for demanding robotics/defense); higher-end, higher-cost tier.
- **Honeywell** (NASDAQ: HON) — navigation-grade and MEMS IMUs; primarily used in aerospace/defense robots.
- **Xsens** (acquired by mCube; previously Moog Inc. subsidiary) — motion-tracking algorithms + IMUs for humanoid/biomechanics; now part of Chinese-backed mCube (private).
- **Movella** (NASDAQ: MVLA — previously mCube/Xsens entity; ticker uncertain after multiple restructurings) — Xsens brand assets.

**Chokepoint:** LOW-MODERATE. IMU market is competitive across TDK, Bosch, ST, ADI. No single dominant vendor at the commodity tier. ADI commands a premium tier (ADIS).

**Captive risk:** LOW. IMUs are commodity inputs; no humanoid builder making own IMUs.

**China leakage:** LOW. Market is dominated by Japanese/German/US/Swiss players. Chinese entrants (GuideNav) exist in lower-precision segments.

**Accessibility for US public equity:** GOOD. **STM** (NYSE), **ADI** (NASDAQ), **TDK** (Tokyo), **Honeywell** (NYSE) all accessible. STM and ADI are the cleanest US-listed plays. Robotics is a growth vertical for both but not dominant revenue today.

---

### 6. Machine Vision & Depth Cameras

**Description:** RGB-D (color + depth) cameras for manipulation, navigation, and environment mapping. Each humanoid uses 2–6 cameras. Critical for hand-eye coordination and physical AI.

**Vendor categories & named vendors:**
- **RealSense Inc.** (private, Intel spinout — $50M from Intel Capital + MediaTek Innovation Fund, 2024) — ~60% share of AMR/humanoid robots (Reuters 2025); D585 Pro AI-native camera (ships Q1 2027); strategic NVIDIA Jetson Thor integration; customers include Unitree, Agility (Digit uses D455 in neck). No direct public equity.
- **Luxonis** (private, US) — OAK-D series with on-device AI; open-source friendly; popular for research and mid-tier deployments.
- **Stereolabs / ZED** (acquired by Ouster, NASDAQ: OUST, Feb 2026) — ZED X Nano designed specifically for humanoid manipulation; Ouster now owns ZED + Velodyne + its own lidar. Ouster is US-listed.
- **Orbbec** (private, Chinese) — low-cost RGB-D; winning price-sensitive slots.
- **Photoneo** (acquired by Zebra Technologies, NASDAQ: ZBRA, late 2024) — structured-light 3D; industrial grade.
- **Intel's RealSense division** — fully carved out; see above.

**Chokepoint:** MODERATE. RealSense's ~60% AMR/humanoid install base is a soft chokepoint but not exclusive; Luxonis and ZED/Ouster are credible alternatives.

**Captive risk:** LOW-MODERATE. Some builders (Boston Dynamics) develop proprietary perception systems but still source RGB-D sensors from vendors.

**China leakage:** LOW-MODERATE. Orbbec (Chinese) competes on price. Hesai's color lidar may displace RGB-D cameras in certain use cases.

**Accessibility for US public equity:** PARTIAL. **Ouster (OUST)** is the clearest US-listed route (owns ZED/Stereolabs + lidar). **Zebra (ZBRA)** got Photoneo but it's immaterial at Zebra scale. RealSense is private (best single name). Luxonis is private.

---

### 7. LiDAR

**Description:** 3D point-cloud sensors for navigation, mapping, and spatial awareness. Not on every humanoid today (cost/size), but increasingly used in training environments and high-end platforms. Solid-state units now at $400–$500.

**Vendor categories & named vendors:**
- **Ouster** (NASDAQ: OUST) — REV8 native color lidar (lidar + camera in one chip); Q1 2026 record revenue $49M; acquired Velodyne + Stereolabs; targeting $14B robotics market. Explicitly focused on humanoids.
- **Hesai Technology** (NASDAQ: HSAI) — Chinese; 2M+ cumulative deliveries; 4M unit/yr capacity (2026); JT Series mini-lidar surpassed 200,000 deliveries in first year; aggressively entering humanoid market; color lidar entering production end-2026. Cheapest high-quality lidar at scale.
- **Aeva Technologies** (NYSE: AEVA) — FMCW lidar; up 11% alongside Ouster in June 2026 physical-AI rally; more autonomous-vehicle heritage but pivoting to robotics.
- **Luminar Technologies** — collapsed into bankruptcy; assets acquired (no longer independent).
- **RoboSense** (HK: 2498) — Chinese; strong auto and robotics positioning; HK-listed.
- **Innoviz Technologies** (NASDAQ: INVZ) — Israeli; primarily automotive; limited humanoid exposure.
- **Velodyne** — absorbed into Ouster.

**Chokepoint:** MODERATE. Hesai dominates volume/cost; Ouster commands premium performance. The REV8 color-lidar consolidation is collapsing two sensor streams, potentially creating a new chokepoint if adopted widely.

**Captive risk:** LOW. Lidar is too specialized for most builders to produce in-house.

**China leakage:** HIGH on volume side (Hesai, RoboSense). But Hesai is NASDAQ-listed, partially accessible. OFAC/NDAA compliance risk is a live concern for US builders using Chinese lidar.

**Accessibility for US public equity:** GOOD-PARTIAL. **Ouster (OUST)** and **Hesai (HSAI)** are both NASDAQ-listed. Aeva (NYSE) is accessible but less humanoid-focused. Hesai's China-HQ creates geopolitical/delisting risk.

---

### 8. Batteries & Power Electronics

**Description:** Li-ion or solid-state battery packs for mobile power (2–4 hours typical); power management ICs; DC-DC converters; motor drivers. One of the key constraints on continuous-operation humanoids.

**Vendor categories & named vendors:**
- **LG Energy Solution** (KRX: 373220) — confirmed supplier to Boston Dynamics Atlas; 46-series cylindrical NCM cells; deployment target Hyundai US factories 2028.
- **Samsung SDI** (KRX: 006400) — unveiled humanoid-specific solid-state batteries at InterBattery 2026; targeting mass production H2 2027.
- **CATL** (SZSE: 300750) — world's largest EV battery maker; strategic investor in AgiBot; partnerships with multiple humanoid programs; major technical solutions for humanoid power.
- **EVE Energy** (SZSE: 300014) — announced humanoid robotics partnerships and technical solutions 2025.
- **Panasonic Energy** (TSE: 6752) — cylindrical cell supplier; Panasonic has servo motor exposure too.
- **Power electronics (motor drivers/inverters):**
  - **Texas Instruments** (NASDAQ: TXN) — motor driver ICs; GaN power stages.
  - **Infineon Technologies** (XETRA: IFX) — power MOSFETs, GaN, gate drivers; heavily used in robotics power stages.
  - **STMicroelectronics** (NYSE: STM) — motor control ICs + power devices; dual exposure (sensors + power).
  - **ON Semiconductor / onsemi** (NASDAQ: ON) — power semiconductors.
  - **Monolithic Power Systems** (NASDAQ: MPWR) — DC-DC converters/PMICs widely used in embedded robotic systems.

**Chokepoint:** MODERATE on cells (Samsung/LG/CATL are oligopoly at production scale). HIGH on solid-state (Samsung SDI has a first-mover slot but timeline is 2027+).

**Captive risk:** LOW on cells (battery chemistry too capital-intensive for builders). MODERATE on power electronics (some builders do custom power boards but use merchant ICs).

**China leakage:** HIGH on battery cells (CATL dominant at scale; CATL + EVE are Chinese-exchange listed). LG/Samsung are Korean-listed.

**Accessibility for US public equity:** PARTIAL-GOOD. **TXN**, **ON**, **MPWR**, **STM** are all US/EU-listed and broadly accessible. For cells: **Samsung SDI** and **LG ES** are Korean-listed (accessible via ADR or direct). CATL is Chinese-listed.

---

### 9. Edge AI Compute (Onboard Brain)

**Description:** The onboard compute module running perception, planning, and control in real time. Typically a systems-on-module (SOM) or custom compute board. This is NVIDIA's clearest single-node dominance in the humanoid stack.

**Vendor categories & named vendors:**
- **NVIDIA** (NASDAQ: NVDA) — Jetson Thor (Blackwell; 2,070 FP4 TFLOPS; 40–130W); Jetson Orin (AGX family; still widely deployed); IGX Thor (industrial/safety-critical). Adopted by: Agility (Digit Gen 5→6), Boston Dynamics Atlas, Humanoid, RLWRLD, and others. Jetson T4000 ($1,999 at 1K units) provides cost-effective upgrade path. Project GR00T + Isaac Sim ecosystem creates deep platform lock-in. NVIDIA is also the key data-center GPU for cloud training of robot policies.
- **Qualcomm** (NASDAQ: QCOM) — Dragonwing/IQ-9075 SoC (200 TOPS); Firefly AIBOX-9075; growing robotics presence but still secondary to NVIDIA in humanoid deployments.
- **AMD** (NASDAQ: AMD) — Kria SOM and Versal AI platforms; niche robotics deployments but not humanoid-dominant.
- **Rockchip** (private, Chinese) — RK3588 used in lower-cost robots; not at humanoid performance tier.
- **Horizon Robotics** (HK: 9660) — Journey series chips; deployed in Chinese humanoid programs; HK-listed.
- **Custom silicon:** Tesla is developing custom inference chips for Optimus. Google/DeepMind (Apptronik partnership) uses TPU-adjacent custom compute. Figure's compute stack is partially proprietary.

**Chokepoint:** VERY HIGH. NVIDIA Jetson Thor is the de facto humanoid compute standard. The Jetson ecosystem (Isaac Sim + GR00T + Holoscan) creates a platform moat that goes beyond hardware specs.

**Captive risk:** HIGH (for top-tier builders). Tesla custom silicon, Google TPUs for Apptronik, Figure's proprietary stack. But 80%+ of the remaining builder market will stay on Jetson Thor.

**China leakage:** LOW-MODERATE. Horizon Robotics serves the Chinese domestic market. Chinese builders using Jetson still drives NVIDIA revenue.

**Accessibility for US public equity:** EXCELLENT. **NVIDIA (NVDA)** is US-listed, large-cap, and the clearest single forced-spend beneficiary in the entire stack. Qualcomm (QCOM) is US-listed secondary.

---

### 10. Semiconductors (Broader: Motion Control ICs, Signal Chain, Microcontrollers)

**Description:** Beyond edge AI, humanoids require motion-control MCUs, encoder ICs, safety controllers, ADCs/DACs, and connectivity chips.

**Vendor categories & named vendors:**
- **Texas Instruments** (NASDAQ: TXN) — MSP430/C2000 real-time MCUs; motor driver ICs; dominant in real-time control embedded in robot joints.
- **STMicroelectronics** (NYSE: STM) — STM32 MCUs (most popular robotics real-time controller globally); motor control libraries; F/T sensor interface ICs.
- **Renesas Electronics** (TSE: 6723) — RA/RX MCUs; functional-safety (ISO 26262) MCUs; strong in precision servo drives.
- **Microchip Technology** (NASDAQ: MCHP) — PIC32/dsPIC motor-control MCUs; encoder chips.
- **Analog Devices** (NASDAQ: ADI) — encoder/resolver interfaces; precision signal chain for F/T and position sensing. AMR encoder ICs for robot joints.
- **Infineon** (XETRA: IFX) — XMC/AURIX real-time MCUs + power stages; safety-MCU heritage from automotive.
- **Lattice Semiconductor** (NASDAQ: LSCC) — small FPGAs widely used for sensor fusion and real-time IO in robotic platforms.

**Chokepoint:** LOW (broad competitive market). Chokepoints exist at niche levels (e.g., precision resolver-to-digital converters: ADI's RDC series has few competitors at the top spec tier).

**Captive risk:** LOW. Humanoid builders are not making their own MCUs.

**China leakage:** LOW-MODERATE. Chinese MCU makers (GigaDevice, Huada) compete at low end but not at functional-safety tiers needed for humanoids.

**Accessibility for US public equity:** EXCELLENT. TXN, STM, ADI, MCHP, LSCC are all US/EU-listed. STM and ADI have strong robotics-specific content.

---

### 11. Bearings & Linear Motion (Ball Screws, Linear Guides)

**Description:** High-precision bearings and ball/roller screws used in actuator joints and linear DOF. A hidden chokepoint because volume is critical and lead times are long.

**Vendor categories & named vendors:**
- **THK** (TSE: 6481) — dominant in linear guides and ball screws globally; strategic investor/partner of Agility Robotics.
- **NSK** (TSE: 6471) — bearings + ball screws; major industrial robot supplier.
- **NTN** (TSE: 6472) — bearings; expanding into humanoid component supply.
- **SKF** (NASDAQ Stockholm: SKF B) — global bearings leader; positioning for robotics.
- **Schaeffler** (SDAX: SHA) — INA/FAG bearing divisions + now humanoid actuator systems.
- **Hiwin** (TWSE: 2049) — linear guideways + ball screws; confirmed Boston Dynamics supplier (per Hiwin Chairman); Taiwan-listed.
- *Chinese challengers:* Shandong Boying Bearing, Zhejiang Tianma, others scaling for humanoid demand.

**Chokepoint:** MODERATE. Precision-grade bearings and ball screws have a concentrated high-quality supplier base. Volume ramp constraints are a real risk (THK, NSK capacity expansion underway).

**Captive risk:** LOW.

**China leakage:** MODERATE. Chinese precision bearing makers are improving but premium humanoid spec is still dominated by Japanese/German/Taiwan players.

**Accessibility for US public equity:** PARTIAL. THK (Tokyo), NSK (Tokyo), SKF (Stockholm), Schaeffler (Frankfurt), Hiwin (Taiwan) are all listed but require non-US exchange access. No major US-listed pure-play for bearings.

---

### 12. Rare-Earth Magnets (NdFeB)

**Description:** Neodymium-iron-boron permanent magnets used in all brushless DC and frameless torque motors. With 20–40 actuators per robot, magnet demand per humanoid is substantial. This is now an acute geopolitical chokepoint.

**Vendor categories & named vendors:**
- **MP Materials** (NYSE: MP) — only active rare-earth mine in North America (Mountain Pass, CA); DoD invested $400M; Pentagon acquired 15% stake June 2025; halted all rare-earth exports to China April 2025; Texas magnet plant ramping. Key US strategic play.
- **Lynas Rare Earths** (ASX: LYC) — Australian mining + Malaysia processing; key non-China source; expanding capacity.
- **USA Rare Earth** (private → commissioning Oklahoma plant 2026) — no public equity yet.
- **Energy Fuels** (NYSE American: UUUU) — uranium miner diversifying into RE processing.
- **JL Mag Rare-Earth** (SZSE: 300748) — Chinese sintered NdFeB leader; dominant production volume; Chinese-exchange listed.
- **Zhongke Sanhuan** (SZSE: 000970) — Chinese NdFeB leader.
- **Shin-Etsu Chemical** (TSE: 4063) — Japanese; significant NdFeB magnet production.
- **TDK** (TSE: 6762) — Neodymium magnet division (NEOREC series).

**Chokepoint:** EXTREME. China controls ~69% of rare-earth mining and ~90% of downstream magnet production. April 2025 export controls created immediate supply disruption across humanoid, EV, and defense sectors. This is the single most acute supply-chain chokepoint in the entire robotics stack.

**Captive risk:** N/A (no builder making magnets in-house; too capital-intensive).

**China leakage:** EXTREME. Production is ~90% China-controlled. The Western ex-China supply chain (MP Materials, Lynas, Shin-Etsu) is years behind China on volume.

**Accessibility for US public equity:** PARTIAL. **MP Materials (MP)** is US-listed and is the clearest US pure-play, but it is a mine/materials company, not a components company. **Lynas (LYC)** on ASX. **TDK** and **Shin-Etsu** (Tokyo) are partial routes.

---

### 13. Teleoperation Rigs

**Description:** Hardware systems for human operators to demonstrate robot tasks and generate high-fidelity training data. This is the critical data-collection chokepoint for training foundation robot models.

**Vendor categories & named vendors:**
- **HaptX** (private, US) — Nexus NX1 Full-Body System (72 DoF, sub-mm precision); chosen by Sanctuary AI as teleoperation partner for Phoenix humanoid; haptic feedback produces qualitatively richer demonstrations.
- **Adamo** (private, US — emerged from stealth 2025) — managed teleoperation services; sub-40ms latency software; targeting humanoid builders as a service provider.
- **Dexterity** (private, US) — robot grasping + teleoperation; prior investment from Kleiner Perkins.
- **Shadow Robot Company** (private, UK) — dexterous hands + teleoperation systems.
- **Embodied Intelligence** (rebranding of some spinouts; private ecosystem) — multiple companies building teleoperation and demonstration systems from academic spinouts.
- Internal builder systems: Figure, Tesla, Apptronik, Agility are all building in-house teleoperation rigs because it's a key differentiator in data quality. This is highly captive.

**Chokepoint:** MODERATE. No dominant merchant vendor. Quality teleoperation with haptic feedback is rare (HaptX is the clearest leader). Most of the market is fragmented or captive in-house.

**Captive risk:** VERY HIGH. Every top-tier builder treats teleoperation rig design as proprietary and strategic. The data generated is the moat, not the hardware.

**China leakage:** LOW.

**Accessibility for US public equity:** POOR. All named vendors are private. No accessible public equity route for teleoperation hardware specifically.

---

### 14. Motion Capture Systems

**Description:** Optical or inertial mocap for recording human demonstrations and validating robot motion quality. Used in training studios and gait labs.

**Vendor categories & named vendors:**
- **Vicon** (private, UK — owned by Oxford Metrics, LSE: OMG) — industry-standard optical mocap; Oxford Metrics is UK small-cap listed on AIM.
- **OptiTrack** (subsidiary of NaturalPoint, private, US) — high-fps optical mocap; widely used in robot training labs.
- **Qualisys** (private, Swedish) — optical mocap alternative.
- **Xsens** (now part of mCube/Movella ecosystem — NASDAQ: MVLA ticker uncertainty) — inertial mocap suits; widely used for full-body robot training data.
- **Rokoko** (private, Danish) — Smartsuit Pro; more affordable inertial mocap; used in smaller-scale training studios.

**Chokepoint:** LOW-MODERATE. Multiple viable systems exist. The trend is toward inertial (Xsens/Rokoko) for scale and optical (Vicon/OptiTrack) for precision research.

**Captive risk:** LOW. Mocap hardware is not something builders make in-house.

**China leakage:** LOW.

**Accessibility for US public equity:** POOR. Oxford Metrics (AIM) is accessible for UK investors. Movella/Xsens NASDAQ exposure is uncertain. OptiTrack, Qualisys, Rokoko all private.

---

### 15. Simulation & World Models (Training Data Infrastructure)

**Description:** Physics-simulation environments for generating synthetic training data at scale, and world-model platforms for policy learning. This is the force multiplier node — simulation generates millions of training episodes cheaply.

**Vendor categories & named vendors:**
- **NVIDIA** (NASDAQ: NVDA) — Isaac Sim (full robotics simulation stack built on Omniverse/USD); Isaac Lab (GPU-accelerated RL; 70× speedup via GPU parallelism); Cosmos (world-model foundation for data generation); GR00T (open robot policy models); partnered with >110 robot-brain developers including Figure, Agility, Skild, ABB, KUKA, FANUC. Simulation + cloud training + edge compute = complete vertical lock-in.
- **Mujoco / DeepMind** (Alphabet, NASDAQ: GOOGL) — MuJoCo physics engine (acquired by DeepMind, now open-source); used by most academic and many commercial robot-learning groups. Alphabet/DeepMind also partnered with Apptronik.
- **Ansys** (NASDAQ: ANSS) — high-fidelity FEA/multiphysics simulation used for mechanical design validation; some robotics simulation use. Acquired by Synopsys (deal approved 2024; SNPS+ANSS merger creating $35B+ entity, potentially complete).
- **Siemens** (XETRA: SIE) — Tecnomatix robotics simulation; factory digital-twin context for humanoid deployment validation.
- **Scale AI** (private) — labeled-data and RLHF platform; expanding into robotics data labeling; not yet a robot-native platform.
- **Physical Intelligence (Pi)** (private, US) — building foundation robot policies; direct competitor to builders but also a platform play for policy infrastructure. Raised ~$400M (2024).
- **Covariant** (private, US) — robot-brain AI; now part of Amazon (acquired 2024); captive to Amazon's robotics ambitions.
- **Skild AI** (private, US) — generalist robot brain; NVIDIA partner; using Cosmos + Isaac.

**Chokepoint:** HIGH (simulation layer). NVIDIA Isaac/Cosmos is approaching a platform monopoly for robot simulation. The open-source MuJoCo alternative is important but cannot match NVIDIA's integrated hardware-simulation-deployment stack.

**Captive risk:** HIGH. Major builders (Tesla Optimus, Boston Dynamics/Hyundai) develop proprietary simulation environments as core IP.

**China leakage:** LOW.

**Accessibility for US public equity:** GOOD. **NVIDIA (NVDA)** is the dominant accessible play. **Alphabet (GOOGL)** is partial (MuJoCo + DeepMind robotics). Ansys/Synopsys are accessible but humanoid-simulation is a small part of their revenue.

---

### 16. Data Labeling & Annotation

**Description:** Human-annotated robot demonstrations, video labeling, and reward modeling for supervised and RLHF training. Rapidly being supplemented by synthetic (simulation) data but human annotation remains essential for edge cases and safety.

**Vendor categories & named vendors:**
- **Scale AI** (private, US) — largest data-labeling platform; moving into robotics; federal government contracts; no public equity.
- **Labelbox** (private, US) — data annotation platform.
- **Appen** (ASX: APX) — Australian-listed crowdsource data labeling; under significant financial pressure.
- **Shaip** (private, US) — focused on embodied AI robot training data specifically (per 2025–2026 articles).
- **Surge AI** (acquired by Scale AI) — premium human labeling.
- **NVIDIA** (NVIDIA Canvas + NVIDIA AI Foundation models provide synthetic annotation at scale; blurs line with simulation node).
- **AgiBot** (Chinese, private → SZSE candidate) — open-sourced AGIBOT WORLD 2026 dataset.

**Chokepoint:** LOW. Data labeling is a commodity service (many providers globally). Premium robot-specific annotation has fewer players.

**Captive risk:** HIGH. Builders are building internal annotation pipelines as a strategic moat.

**China leakage:** LOW-MODERATE. Chinese builders (Agibot) are generating large open datasets; domestic Chinese annotation services are plentiful.

**Accessibility for US public equity:** POOR. Scale AI (private) is the most relevant player. Appen (ASX) is listed but declining financially. NVIDIA remains the best public-equity route for the simulation side of this node.

---

## Top 3 Nodes Where Forced Spend Most Cleanly Reaches Accessible Public Suppliers

1. **Edge AI Compute (Node 9):** NVIDIA Jetson Thor is the de facto standard for humanoid compute. Every non-Tesla, non-Google builder is spending on Jetson. No China leakage, no captive alternative at scale, public US-listed. NVDA is the clearest single forced-spend beneficiary in the entire humanoid stack.

2. **Force-Torque Sensors (Node 3):** Novanta (NOVT) owns ATI Industrial Automation, the market-leading certified F/T sensor vendor. Low China exposure, no captive threat at production-grade specs, and every production humanoid needs 2–4 units. This is a narrow but clean forced-spend funnel to a US-listed mid-cap.

3. **Semiconductors / Signal Chain (Node 10):** STMicroelectronics (STM) and Analog Devices (ADI) have broad, sticky exposure across motion-control MCUs (STM32 is near-ubiquitous), encoder/resolver interfaces, and MEMS IMUs (ADI). No single company captures the whole node, but both STM and ADI see robotics as a compounding growth vertical with minimal China-leakage risk at their product tier.

**Honorable mention:** Ouster (OUST) — owns lidar + ZED stereo camera after Stereolabs acquisition. Revenue is growing, humanoid robotics is an explicit strategy, and the REV8 color-lidar consolidation thesis is compelling. Higher risk/earlier stage than NVDA/NOVT/STM/ADI.

---

## Coverage Gaps

The following areas have insufficient data for confident mapping and should be researched in Wave 1:

1. **Dexterous hand subassemblies:** No production-grade merchant dexterous hand vendor has been identified. The 31% BOM allocation is almost entirely captive or pre-revenue private startups. Need: vendor mapping of Ability Hand (Psyonic), Shadow Robot, SEED Robotics, Wonik IPS (Korean), and Chinese entrants.

2. **Motor driver / GaN power stage specifics:** The power electronics node (TXN, Infineon, STM) was mapped at category level. Need: unit volume estimates, ASP per robot, GaN vs. SiC penetration rate, and whether any single IC vendor is disproportionately winning humanoid design wins.

3. **Pneumatic and soft-actuator suppliers:** Some builders (Soft Robotics, Piab) use pneumatic or soft-compliant actuation for hands. Not mapped here. Materiality unclear for 2026 humanoids (most are electric actuator).

4. **Structured light / 3D sensing alternatives:** Photoneo (Zebra), Zivid (private), and Mech-Mind (Chinese, private) compete in the structured-light 3D-vision space used for bin-picking and industrial manipulation. Humanoid relevance in 2026–2027 may be moderate.

5. **Communication/networking silicon:** Real-time fieldbuses (EtherCAT, TSN Ethernet, FSoE) and the silicon behind them (Beckhoff, HMS Networks, Texas Instruments EtherCAT ASICs). HMS Networks (Nasdaq First North: HMS) is a niche-listed accessible play here.

6. **Cloud training infrastructure:** GPU cloud (AWS, Azure, GCP) used for offline robot policy training is a massive forced spend that benefits NVDA (H100/H200 demand) and cloud hyperscalers. Not separately mapped here because it is well-documented in standard AI infrastructure analysis. But the robotics-specific workload (Isaac Sim on cloud, large-scale RL training) warrants its own accounting.

7. **Wiring harnesses & structural materials:** Cable management within robot bodies (Yazaki, Sumitomo Electric, TE Connectivity) and structural materials (carbon fiber, titanium alloy, CNC machining vendors). Not trivial at scale but not a strategic chokepoint for equity selection.

8. **Robot-to-cloud connectivity:** 5G/CBRS industrial connectivity chips (Qualcomm, MediaTek) and edge networking (Cisco Industrial, Sierra Wireless/Semtech) for humanoid fleets reporting back to cloud training pipelines. Partially captive to hyperscalers and telecom infrastructure.

---

*Sources: Morgan Stanley Humanoid 100 Value Chain Report; McKinsey humanoid supply-chain analysis (2025); IDTechEx Humanoid Robots 2025–2035; humanoid.guide Supply Chain Report 2026–2027; NVIDIA Jetson Thor product announcements; Ouster Q1 2026 earnings + Stereolabs acquisition; Hesai CES 2026; RealSense spinout reporting (Robot Report 2025); TDK InvenSense ICM-42688-P; MP Materials DoD investment (2025); LG Energy Solution Boston Dynamics supply confirmation; Samsung SDI InterBattery 2026; Goldman Sachs cost decline analysis; Reuters RealSense market-share data; XELA Robotics 2026 announcements; multiple market research reports (Intel Market Research, Research and Markets); ArXiv empirical depth-camera comparison (2025); labellerr.com teleoperation vendor guide (2026).*
