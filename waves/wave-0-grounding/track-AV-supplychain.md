# AV Supply Chain — Wave 0 Grounding
**Date:** 2026-07-05  
**Scope:** Forced spend nodes for AV fleet scaling (Waymo, Aurora, Zoox, Wayve, automaker AV programs) in 2025–2026. Purpose: identify where that spend lands on accessible public suppliers and where demand overlaps robotics/world-model training tracks.

---

## 1. LiDAR

### Vendor categories and named vendors
- **Chinese public leaders (NASDAQ/HKEX listed):** Hesai Group (HSAI – Nasdaq), RoboSense (2498.HK – HKEX)
- **US/Israel public:** Ouster (OUST – NYSE, post Velodyne merger), Aeva Technologies (AEVA – NYSE), Innoviz Technologies (INVZ – Nasdaq), Luminar Technologies (LAZR – Nasdaq, acquired by Quantum Computing in restructuring)
- **Private:** Cepton (acquired by Continental), Seyond, Quanergy (bankrupt)
- **Tier-1 integrators:** Valeo (VLOF – Paris), Continental (CON – Frankfurt)

### Chokepoint / single-source?
Not a single-source chokepoint. **Dual-track consolidation** is underway: (a) Chinese volume suppliers (Hesai ~33% automotive LiDAR market share, RoboSense #2) commanding the high-volume/cost-sensitive segment; (b) Western suppliers (Innoviz for BMW/VW i4/ID.Buzz; Aeva as Nvidia DRIVE Hyperion reference and Daimler Truck exclusive) holding specific design wins. No single vendor locks the entire market, but individual platform wins create program-level lock-in.

### Captive / vertical integration risk
Waymo is building bespoke LiDAR in-house (6th-gen Driver) — significant vertical integration by the largest US robotaxi operator. Rivian's RAP1 integrates compute but still sources LiDAR externally. AutoX (China) runs fully vertical.

### China-dominated or private-only?
**China-dominated by volume** — Hesai and RoboSense together hold >50% of 2025 automotive LiDAR shipments globally. Both are listed (Hesai on Nasdaq, RoboSense on HKEX), making them accessible but carrying China-risk. Western accessible plays are smaller: Ouster (post-consolidation), Aeva (narrow TAM, Daimler/Nvidia wins), Innoviz (VW/BMW wins, cash-burn risk).

### Robotics/world-model overlap?
**Extremely strong.** Hesai robotics shipments grew +1,312% YoY in Q3 2025; RoboSense pivoted to a "robotics platform company" in early 2025. Automotive-grade qualification (–40°C to +85°C, 50G vibration) transfers directly to mobile robots, delivery robots, AGVs. This is the clearest double-signal node in the supply chain.

### Accessibility for US public equity
**Partial.** Hesai listed on Nasdaq (most accessible), RoboSense on HKEX (requires ADR/broker access), Ouster/Aeva/Innoviz small-cap with significant burn. China-concentration is a real risk for US investors given CISA/export-restriction overhang on Hesai specifically.

---

## 2. Radar (including 4D Imaging Radar)

### Vendor categories and named vendors
- **Tier-1 public:** Continental (CON), Bosch (private), ZF (private), Aptiv (APTV – NYSE), Valeo (VLOF)
- **Chipset/silicon (public):** NXP Semiconductors (NXPI – Nasdaq), Texas Instruments (TXN – Nasdaq), Infineon Technologies (IFX – Frankfurt), Analog Devices (ADI – Nasdaq), STMicroelectronics (STM – NYSE)
- **Pure-play imaging radar:** Arbe Robotics (ARBE – Nasdaq), Uhnder (private), Smartmicro (private – Germany)
- **Emerging:** Oculii (acquired by Aptiv), Zendar (private), Bitsensing

### Chokepoint / single-source?
No single-source chokepoint at the system level — multiple Tier-1 suppliers compete. However, **radar chipsets** have a narrower supply base: NXP (S32R47 imaging radar SoC, Gen-3 released May 2025), TI, and Infineon collectively dominate radar MMIC/SoC supply. The NXP S32R47 targets L2+–L4, making NXP a de facto reference silicon for 4D imaging radar.

### Captive / vertical integration risk
Aptiv acquired Oculii's software stack to differentiate its Gen-8 radar lineup (October 2025). Continental, Bosch, ZF are full-vertical for their radar module production. No AV operator is building radar silicon in-house.

### China-dominated or private-only?
Tier-1 module level is Western-dominated. Silicon level is accessible via Nasdaq/NYSE (NXP, TI, ADI, Infineon). Pure-play 4D imaging plays are mostly private (Uhnder, Smartmicro) except Arbe Robotics (ARBE – Nasdaq), which is a small-cap.

### Robotics/world-model overlap?
**Moderate.** 4D radar is increasingly used in indoor robotics, warehouse AGVs (Vayyar, Bitsensing), and obstacle detection in mobile robots. The overlap is real but less direct than LiDAR — radar is not yet the dominant robotics sensing modality.

### Accessibility for US public equity
**Good** at the semiconductor layer (NXP, TI, ADI all large-cap liquid). Arbe is accessible but illiquid micro-cap. Aptiv is the best-capitalized pure play on the full-stack radar integration thesis.

---

## 3. Cameras / Image Sensors (CMOS)

### Vendor categories and named vendors
- **Dominant image sensor suppliers:** Sony Semiconductor Solutions (6758.T – Japan, ~63.6% total CIS market), OmniVision (private – owned by Will Semi, Chinese), onsemi (ON – Nasdaq), Samsung (005930.KS)
- **Lens/module integrators:** Gentex (GNTX – Nasdaq, mirrors + cameras), Magna (MGA – NYSE, camera modules), Aptiv (APTV – NYSE)
- **Automotive-specific design wins:** OmniVision (OX08D20 for Mobileye, in production 2026; Tesla, BYD, VW, BMW, Toyota), onsemi (ADAS surround-view, DMS, North America scale-up 2025), Sony (high-res premium segment expansion)

### Chokepoint / single-source?
**Near-chokepoint for automotive CMOS.** The top 5 players (Sony, Samsung, OmniVision, STMicro, onsemi) held 83.1% of CIS market in 2025. For automotive specifically, OmniVision and onsemi are the two dominant suppliers; Sony and Samsung are challengers. Vehicle camera count rising to avg 12 by 2028 (from 8 in 2025) — steady volume tailwind.

### Captive / vertical integration risk
Waymo builds its own 17-megapixel imager for 6th-gen Driver (internal design, manufactured externally). Tesla uses onsemi/OmniVision with internal processing. Vertical integration risk is at the module/processing level, not wafer/sensor fab.

### China-dominated or private-only?
OmniVision is the dominant automotive CIS player — but it is **private** (owned by Will Semiconductor, Chinese parent, not directly investable for US public equity). This is a significant leakage node. onsemi and Sony are the accessible public alternatives.

### Robotics/world-model overlap?
**Very strong.** onsemi explicitly targets automotive ADAS + industrial machine vision + robotics as a single franchise. OmniVision extends into robotics/security. Camera sensors are universal in humanoid robot stacks, drone vision, and world-model training data collection.

### Accessibility for US public equity
**Partial.** onsemi (ON) is accessible and liquid. Sony is accessible via ADR (SONY) but automotive is <15% of Sony total revenue — limited purity. OmniVision (most automotive-dominant player) is private/Chinese-owned — **hard leakage**. Samsung accessible but diversified conglomerate.

---

## 4. Automotive AI Compute (SoC / Platform)

### Vendor categories and named vendors
- **Dominant platform:** Nvidia (NVDA – Nasdaq) — DRIVE Orin (254 TOPS, L2/L3), DRIVE Thor (2,000+ TOPS, L4); Aurora uses dual-Thor "Super Thor" config with AUMOVIO
- **Competing platforms:** Qualcomm (QCOM – Nasdaq) — Snapdragon Ride; Mobileye (MBLY – Nasdaq) — EyeQ6/EyeQ Ultra; Renesas (6723.T – Japan)
- **Chinese in-house silicon:** Horizon Robotics (9660.HK), Black Sesame Technologies (2533.HK – HKEX)
- **In-house silicon (captive):** Rivian RAP1 (1,600 TOPS dual-chip, 2026 R2), Tesla FSD chip (in-house, manufactured by Samsung/TSMC), Waymo TPU-derived compute (Google-heritage)
- **Manufacturing:** TSMC (TSM – NYSE) for Nvidia Thor and most advanced automotive SoCs

### Chokepoint / single-source?
**Strong de facto chokepoint at the software/platform layer.** Nvidia DRIVE's CUDA/DriveWorks ecosystem creates significant switching costs — described explicitly by analysts as locking in Tier-1 suppliers and OEMs. Aurora, Nuro, Bosch, and multiple Tier-1s are committed to Thor. Mobileye competes for OEM/ADAS segment but loses ground in L4 robotaxi segment. TSMC is the manufacturing chokepoint for all leading-edge automotive SoCs.

### Captive / vertical integration risk
**High and rising.** Rivian RAP1, Tesla FSD, Waymo custom compute all represent completed vertical integration. This captive leakage is significant — the largest AV operators are increasingly self-sufficient on compute.

### China-dominated or private-only?
Western-dominated at the accessible public level. Chinese alternatives (Horizon Robotics, Black Sesame) are relevant domestically but not chosen by US/EU AV operators. TSMC is the manufacturing dependency (geopolitical risk, Taiwan).

### Robotics/world-model overlap?
**Strongest overlap node.** The same Nvidia Jetson/Thor platform that runs AV inference runs humanoid robot brains (Figure, 1X use Jetson Orin) and world-model training workloads run on Nvidia H100/H200 data-center GPUs. The robotics/world-model compute demand is additive to the automotive segment and shares the same silicon roadmap.

### Accessibility for US public equity
**Excellent.** Nvidia (NVDA) is the most liquid pure-play — both AV and robotics/world-model demand flows through the same GPU/SoC architecture franchise. Mobileye (MBLY) is accessible but narrower (automotive ADAS, less robotics exposure). Qualcomm (QCOM) has automotive exposure but diversified. TSMC (TSM) is the fab-level play.

---

## 5. HD Mapping / Localization

### Vendor categories and named vendors
- **Commercial map platforms:** HERE Technologies (private – consortium owned by BMW, Mercedes, Audi, Bosch, Continental, Intel JV); TomTom (TOM2.AS – Amsterdam, accessible)
- **Crowdsourced / REM:** Mobileye RoadBook/REM (MBLY – Nasdaq) — 5cm localization accuracy using crowdsourced camera data from production vehicles
- **In-house maps (captive):** Waymo (private), Zoox (Amazon-owned), Aurora (private), Tesla (pure vision, no HD map dependency)
- **SLAM / local localization:** Luminar Iris + localization stack, Ouster SLAM, Trimble (TRMB – Nasdaq) for survey-grade ground truth

### Chokepoint / single-source?
HERE is a single-source for licensed HD map data in many EU/US markets but is **private** (not investable). Mobileye's REM creates a proprietary crowdsourced moat that is difficult to replicate quickly.

### Captive / vertical integration risk
**Very high.** Major AV operators build their own maps entirely. Tesla has zero dependency on HD maps. Waymo, Aurora, Zoox are self-sufficient. This drastically limits the addressable market for commercial map vendors for frontier AV.

### China-dominated or private-only?
Here is private (no direct US equity access). NavInfo (002405.SZ – Shenzhen-listed) is the Chinese analog. TomTom is accessible but subscale for AV.

### Robotics/world-model overlap?
**Moderate.** World-model labs use mapping/localization for robot navigation but are increasingly building neural implicit representations (NeRF, 3D Gaussian Splatting) rather than HD maps. Overlap exists at the SLAM/localization layer (sensor fusion algorithms), less at the commercial map layer.

### Accessibility for US public equity
**Poor.** HERE (private), NavInfo (Chinese/local). Mobileye (MBLY) has REM exposure but is primarily an ADAS compute play. TomTom (Amsterdam) is accessible but niche. Trimble is adjacent but not a pure AV play. This node has significant leakage.

---

## 6. Sensor Cleaning / Maintenance Systems

### Vendor categories and named vendors
- **Dedicated AV sensor cleaning:** Kautex Textron (private – Textron subsidiary) — Allegro CVS (clear-vision system), supplies Uber-Volvo and robotaxi programs
- **Multi-function actuation/valves:** Solero Technologies (private) — sensor cleaning valves, BEV thermal management
- **Washer/nozzle systems:** dlhBOWLES (private), Ficosa (private – Panasonic subsidiary)
- **Integrated fluid systems:** Valeo (VLOF – Paris) — wiper/washer and sensor cleaning, public

### Chokepoint / single-source?
Kautex Textron Allegro is the most referenced dedicated AV sensor-cleaning supplier. Not a hard chokepoint — the technology is fluid-pump/nozzle actuation, but robotaxi-specific qualification (heated nozzles for camera dome/LiDAR spinner) narrows the qualified supplier base.

### Captive / vertical integration risk
Low — no AV operator is building sensor-cleaning systems in-house; this is a Tier-2/3 component.

### China-dominated or private-only?
**Mostly private.** Kautex, Solero, Ficosa, dlhBOWLES are all private. Valeo is the only accessible public name.

### Robotics/world-model overlap?
**Weak.** Outdoor robotics (delivery bots, mowing robots) share the need for sensor maintenance in adverse conditions, but the commercial spend is small and fragmented.

### Accessibility for US public equity
**Poor.** No pure-play US public access. Valeo is partial (Paris-listed, sensor cleaning is small revenue share).

---

## 7. Connectivity / Telematics / V2X

### Vendor categories and named vendors
- **V2X chipset (post-consolidation):** Qualcomm (QCOM – Nasdaq) — acquired Autotalks (completed 2025), now dominant in C-V2X chipset; NXP Semiconductors (NXPI – Nasdaq) — acquired TTTech Auto ($625M, Jan 2025), automotive SDV software+silicon; Infineon (IFX – Frankfurt); Continental (CON) V2X modules
- **Telematics/fleet connectivity:** Verizon Connect (private division), CalAmp (CAMP – Nasdaq, very small), Aptiv (APTV) — connected services hardware; Harman International (Samsung subsidiary, private)
- **5G/cellular modem for AV:** Qualcomm Snapdragon Auto; Sierra Wireless (acquired by Semtech, SMTC – Nasdaq)

### Chokepoint / single-source?
**Near-chokepoint for C-V2X chipset after Qualcomm-Autotalks.** Qualcomm-Autotalks + Cohda Wireless (acquired by Danlaw 2024) leaves Qualcomm with dominant share in direct V2X silicon. NXP and Infineon are the remaining credible alternatives.

### Captive / vertical integration risk
Low-moderate — AV companies don't build connectivity silicon in-house; they source from the chipset tier.

### China-dominated or private-only?
Western-dominated (Qualcomm, NXP, Infineon). Huawei has a V2X offering for China market (not investable via US equity). Harman (telematics) is a Samsung subsidiary — not directly listed.

### Robotics/world-model overlap?
**Moderate.** 5G connectivity is essential for fleet teleoperation data upload (sensor logs, model training data) and remote monitoring. The overlap is at the data-pipe level — same Qualcomm cellular modems used in connected vehicles and industrial IoT/robotics backhaul.

### Accessibility for US public equity
**Good** at semiconductor layer (QCOM, NXPI both large-cap liquid). Limited pure-play on AV telematics specifically.

---

## 8. Data-Collection Fleets / Ground-Truth Vehicles

### Vendor categories and named vendors
- **Captive AV operator fleets (not investable):** Waymo, Aurora, Zoox (Amazon), Wayve (SoftBank-backed), Motional (Hyundai/Aptiv JV)
- **Third-party mapping/survey vehicles:** Velodyne/Ouster-equipped survey vans (Nearmap – NX.AX; Cyclomedia – private); Trimble survey equipment (TRMB)
- **Sensor-equipped consumer fleet (crowdsourced):** Mobileye REM vehicles (~200M+ km crowdsourced map data), Tesla FSD fleet (~6M vehicles passively collecting
- **Data infrastructure:** AWS (Amazon), Google Cloud (Alphabet), Azure (Microsoft) — all AV operators use cloud for petabyte-scale sensor log storage

### Chokepoint / single-source?
Not a chokepoint for data collection hardware. The cloud storage/processing layer is an oligopoly (AWS/GCP/Azure) but not AV-specific.

### Captive / vertical integration risk
**Extremely high.** The data-collection fleet IS the AV operator itself in most cases. This node is almost entirely captive.

### Robotics/world-model overlap?
**Strong.** World-model labs (Physical Intelligence, Figure, 1X) operate their own data-collection hardware (robots + teleop rigs). The cloud infrastructure layer is shared. The sensor hardware (cameras, LiDAR) purchased for data-collection fleets is the same hardware analyzed under Nodes 1–3.

### Accessibility for US public equity
**Poor** as a standalone node. Leaks entirely to the sensor and cloud layers already mapped.

---

## 9. Teleoperation / Remote Operations

### Vendor categories and named vendors
- **Pure-play teleoperation platforms:** Ottopia (private – Israel), Designated Driver (private), Phantom Auto (private), Foretellix (private – AV scenario testing/teleop)
- **Integrated fleet ops:** Zoox (Amazon-captive), Waymo remote-ops (Google-captive)
- **Network infrastructure enabling teleop:** Qualcomm 5G, Ericsson (ERIC – Nasdaq), Nokia (NOK – NYSE) — low-latency 5G radio infrastructure essential for sub-100ms teleoperation loops
- **Data-rate compression:** Akamai (AKAM – Nasdaq), Cloudflare (NET – NYSE) — edge compute for teleoperation video streams

### Chokepoint / single-source?
No chokepoint at the teleoperation software layer — multiple private vendors. Network latency (5G) is the hard physical constraint; infrastructure suppliers (Ericsson, Nokia) benefit indirectly.

### Captive / vertical integration risk
**High.** Waymo and Zoox build bespoke teleoperation systems internally. Independent teleoperation vendors serve mid-tier AV programs.

### China-dominated or private-only?
Mostly private (Ottopia, Phantom Auto). Ericsson/Nokia are accessible public.

### Robotics/world-model overlap?
**Very strong.** Teleoperation is simultaneously the safety overlay for robotaxi fleets AND the primary method for generating robot training demonstrations (physical AI / embodied AI data collection). CVPR 2026 highlighted teleop-as-data-generation as a defining theme. This is a double-signal node.

### Accessibility for US public equity
**Poor** at the application layer (all private). **Partial** at the infrastructure layer (Ericsson, Nokia) but AV/robotics is a small fraction of their revenue.

---

## 10. Annotation / Simulation / Data Pipelines

### Vendor categories and named vendors
- **Annotation/data labeling:** Scale AI (private, 49% stake sold to Meta 2025 at $14.8B valuation), iMerit (private), Appen (APX.AX – small-cap Australia)
- **AV simulation platforms:** Applied Intuition (private – valued ~$6B+), Ansys (ANSS – Nasdaq, acquired by Synopsys deal in progress), dSPACE (private), IPG Automotive (private), Hexagon AB (HEXA-B.ST – Sweden, owns Vires sim)
- **Synthetic data / world-model sim:** Nvidia Omniverse / DRIVE Sim (NVDA), Cognata (private), Metamoto (private)
- **Cloud data infrastructure:** Databricks (private), Snowflake (SNOW – NYSE), AWS (AMZN)

### Chokepoint / single-source?
Scale AI is a near-chokepoint for high-quality AV-grade annotation but is now a Meta affiliate (not independently investable). Applied Intuition holds dominant mindshare in AV simulation for L4 programs. Nvidia DRIVE Sim benefits from the same CUDA lock-in as compute.

### Captive / vertical integration risk
**Very high.** Waymo, Tesla, Aurora run internal data engines. Scale AI's Meta acquisition partially captivates it. This is a heavily internalized node for top-tier operators.

### China-dominated or private-only?
**Heavily private.** Scale AI, Applied Intuition, Cognata all private. The most accessible public name is Nvidia (Omniverse/DRIVE Sim) and Ansys (sensor simulation, Synopsys merger pending).

### Robotics/world-model overlap?
**Maximum overlap.** The data pipeline for AV training IS the world-model training pipeline — the same annotation infrastructure, synthetic data generation, and sim-to-real validation workflows apply to humanoid robots, manipulation models, and general world models. This is the strongest overlap node in the entire supply chain.

### Accessibility for US public equity
**Poor** for pure-play (all major vendors private). Nvidia and Ansys are the only accessible public plays. Snowflake/Databricks benefit at the data warehouse layer but are not AV-specific.

---

## Summary: Node Accessibility Matrix

| Node | Best Public Access | Leakage Risk |
|---|---|---|
| LiDAR | Hesai (HSAI), Ouster (OUST), Aeva (AEVA), Innoviz (INVZ) | Waymo captive; Chinese volume concentration |
| Radar (4D) | NXP (NXPI), TI (TXN), ADI (ADI), Aptiv (APTV), Arbe (ARBE) | Private: Uhnder, Smartmicro |
| Camera/CIS | onsemi (ON), Sony (SONY ADR) | OmniVision private/Chinese |
| AI Compute | Nvidia (NVDA), Mobileye (MBLY), Qualcomm (QCOM), TSMC (TSM) | Rivian/Tesla/Waymo captive |
| HD Mapping | Mobileye (MBLY partial), TomTom (TOM2) | HERE private; most operators captive |
| Sensor Cleaning | Valeo (VLOF) partial | Kautex/Solero/Ficosa all private |
| V2X/Connectivity | Qualcomm (QCOM), NXP (NXPI), Ericsson (ERIC) | Harman private |
| Data-Collection | TSMC/Nvidia/cloud (indirect) | Entirely captive |
| Teleoperation | Ericsson (ERIC), Nokia (NOK) indirect | All app-layer vendors private |
| Annotation/Sim | Nvidia (NVDA), Ansys (ANSS) | Scale AI private; Applied Intuition private |

---

## Top 3 Double-Signal Nodes (forced AV spend + robotics/world-model overlap → accessible public supplier)

### 1. AI Compute (Nvidia / TSMC)
Nvidia DRIVE Thor is the reference platform for Aurora, Nuro, Bosch, and multiple L4 programs. The same GPU architecture (Jetson Orin → Thor) powers humanoid robot inference (Figure, 1X, Agility). Data-center H100/H200 trains world models. TSMC manufactures all leading-edge AV SoCs and robot chips. Both forced AV spend and world-model training demand converge on the same silicon node. Maximum overlap, excellent public equity accessibility, large-cap liquidity.

### 2. LiDAR — Hesai (HSAI) and the Automotive↔Robotics Crossover
Hesai (Nasdaq-listed) is the volume leader in automotive LiDAR (33% share) with robotics shipments growing at +1,312% YoY in Q3 2025. The same sensor family serves AV fleets (AT series) and mobile robots/delivery (JT/XT series). AV fleet scaling drives ASP compression and volume that funds robotics cost-down. RoboSense (HKEX) is the second vector. Warning: Hesai faces CISA/DOD national-security designation risk as a Chinese company with US-AV customer exposure.

### 3. Radar Semiconductors (NXP / TI / Analog Devices)
NXP's S32R47 imaging radar SoC (Gen-3, May 2025) is the reference silicon for 4D imaging radar at L2+–L4. TXN and ADI supply complementary radar MMIC chains. These chips are in every 4D radar module (Aptiv, Continental, Arbe) and increasingly in industrial robot proximity sensing and drone obstacle avoidance. Large-cap, liquid, US-listed — the "picks and shovels" play for the entire radar modality across AV + robotics.

---

## Honorable Mention: Camera Sensors — onsemi (ON)
onsemi is the most accessible US-listed pure-play on automotive CMOS image sensor demand, explicitly serving ADAS + industrial machine vision + robotics as a unified franchise. OmniVision's private/Chinese structure means onsemi captures the accessible portion of this forced spend. Camera count per vehicle is growing from 8 to 12 average by 2028 — structural volume tailwind.

---

## Coverage Gaps

The following areas are under-researched in this memo and should be flagged for additional diligence in subsequent waves:

1. **Inertial / IMU suppliers** — IMUs (Inertial Measurement Units) are safety-critical for AV localization fallback when GPS degrades. Key vendors (Analog Devices MEMS IMU, Honeywell, Northrop Grumman) not fully researched.

2. **GNSS / precision timing** — High-accuracy GNSS (u-blox, Trimble, Septentrio) used for ground-truth calibration and localization is not fully mapped. u-blox (UBXN.SW – Swiss exchange) is investable but not covered here.

3. **Power electronics / automotive-grade power management** — SiC/GaN power management for AV sensor rails (Wolfspeed, onsemi SiC, Infineon CoolSiC) overlaps with EV supply chain and is only partially covered via Infineon in the radar section.

4. **Edge AI accelerators (non-Nvidia)** — Hailo (private – Israel), Kneron (private), Axelera AI (private) provide power-efficient inference accelerators for camera/sensor pre-processing. None are public; leakage is 100%.

5. **Optical components / laser sourcing for LiDAR** — The VCSEL and APD photodetector supply chain (II-VI/Coherent, Lumentum, Princeton Lightwave/Onsemi) underpins LiDAR pulse generation. Lumentum (LITE – Nasdaq) and Coherent (COHR – NYSE) are accessible but not analyzed here.

6. **Fleet management / AV operations software** — Beyond simulation and annotation, fleet-ops platforms (Samsara – IOT, Motive – private) are not mapped for their AV-specific traction.

7. **Regulatory / safety certification infrastructure** — dSPACE, National Instruments (NI), and Vector Informatik (private) provide HIL (hardware-in-loop) test benches that are required for automotive safety certification (ISO 26262, SOTIF). Not covered.

8. **Sensor fusion / perception middleware** — Autoware (open-source), Apex.AI (private), and TTTech Auto (acquired by NXP) provide RTOS and middleware for sensor fusion. TTTech coverage is nascent in this memo.

9. **Chinese supply chain depth** — The Chinese AV supply chain (Baidu Apollo, AutoX, Pony.ai vertical stacks; ECARX integrated kits; NavInfo mapping) is only surface-level researched here. A China-specific sub-track is warranted for a complete picture.

10. **Thermal / environmental simulation for sensor validation** — Ansys AVxcelerate and NVIDIA DRIVE Sim provide sensor simulation, but the physical test equipment layer (temperature chambers, EMC labs) is not mapped.

---

*Sources: Waymo 6th-gen Driver announcements (Electrek, 2026); Aurora/AUMOVIO 8-K filings (SEC, 2026); Hesai Group 6-K filings (SEC, 2025); Innoviz 6-K filings (SEC, 2025); NXP S32R47 press release (May 2025); Qualcomm-Autotalks acquisition (June 2025); NXP-TTTech Auto acquisition (Jan 2025); Yole Automotive LiDAR 2025; MarketsandMarkets 4D Radar report 2025; Scale AI/Meta deal (June 2025); ECARX-May Mobility agreement 6-K (SEC, 2026); autoconnectedcar.com AV news roundups (Feb–Mar 2026); Applied Intuition company materials; Sony/OmniVision/onsemi CIS competitive landscape (Yole 2025); Grand View Research 4D Imaging Radar 2025.*
