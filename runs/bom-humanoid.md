# BOM Teardown: Figure 03 / Apptronik Apollo — Fresh Supplier Candidates
**Run date:** 2026-07-05  
**Method:** Buyer-BOM teardown → named parts → public supplier hunt, small-base/forced-design-win focus  
**Exclusion list applied:** Harmonic Drive, Nabtesco, THK, Hiwin, Ouster, Aeva, Lumentum, Coherent, GE Vernova, Vertiv, Modine, nVent, TTM, Amkor, STM, ADI, TXN, LSCC, MPWR, NXPI, Lynas, MP, Novanta, Marvell, NVDA, TSM, MU, Melexis, Neo Performance, Mitsui High-tec, Kashifuji, Klingelnberg, Vicon/Oxford Metrics

---

## BOM Decomposition — Figure 03 / Apollo

| Subsystem | Key Part | BOM % share (est.) | Supplier landscape |
|---|---|---|---|
| Actuators (joints ×20–32) | Integrated rotary actuator = motor + reducer + encoder + FT sensing | 40–60% | Mostly captive (Figure builds in-house); Apollo sources externally |
| Gearboxes / Reducers | Cycloidal (RV-type) for legs/hips; strain-wave for arms/wrists | 15–25% | Nabtesco (excluded), Sumitomo (large-cap), **Timken/Spinea** (US-listed mid-cap), China privates |
| Motors (stator/rotor) | Brushless DC/PMSM, high-torque-density, custom winding | 10–15% | Nidec (large-cap), **Lin Engineering** (private), motor-winding specialists |
| Force-Torque Sensors | 6-DoF wrist + ankle FT modules, ~4–8 per robot | 3–6% | Bota Systems (private), FUTEK (private), **VPG (VPG)** via load cell/sensing ICs |
| Joint Encoders | Absolute magnetic encoders at each joint | 2–4% | Broadcom (large-cap), **RLS Merilniki** (private, Slovenia), **BOURNS** (private) |
| IMU | High-rate 6-axis IMU (1–3 per robot) | <1% | Bosch Sensortec (private sub), **SBG Systems** (private), **mCube** (private) |
| Compute — Main AI | Edge inference SoC/module | 5–10% | NVIDIA Jetson (Apollo; large-cap), Figure in-house ASIC |
| Compute — Motor control | Real-time MCU/DSP for joint control loops | 2–4% | TI (large-cap per Apollo CES reveal), STM (excluded) |
| Batteries / Pack | Li-ion cylindrical or prismatic pack, ~2 kWh | 5–10% | Mostly captive (Figure F.03 cell; LG/Samsung as cell suppliers); China dominant |
| BMS | Battery management IC + pack architecture | 1–2% | TI (large-cap), **Monolithic Power** (excluded) |
| Power Electronics | DC-DC converters, motor driver ICs | 2–4% | TI, ADI (excluded), **Vicor** (VICR) |
| Cameras / Depth | RGB cams + stereo depth modules (~6–10 per robot) | 3–5% | Sony sensor (large-cap), OmniVision (private/China), **Leopard Imaging** (private) |
| Tactile Sensors (fingertip) | Custom pressure-sensing skin | 1–2% | Figure captive (custom-built), **Roboskin/BeBop** (private) |
| Structural / Chassis | Die-cast Al/Mg frames, injection-molded covers | 3–5% | Die-casting foundries (various privates, China-heavy) |
| Wiring Harness | Custom flex + micro-coax harness | 1–2% | Aptiv (large-cap), Yazaki (private), custom shops |
| Connectors | Micro/nano board-to-board, circular MIL-spec | 1–2% | Amphenol/TE/Molex (large-caps); **Nicomatic** (private) |
| Thermal Management | Heat spreaders, TIM pads, graphite sheet | <1% | Laird Thermal (private), **Momentive** (private sub) |
| Bearings (non-reducer) | Deep-groove, thin-section | 1–2% | SKF/Schaeffler (large-cap), **Kaydon (Kaydon div. of RBC Bearings)** |

---

## Fresh Candidate Assessment

### 1. Vishay Precision Group (VPG) — PRIORITY
- **Ticker:** VPG (NYSE) | **Market cap:** ~$200M (small-cap)
- **Part:** 6-DoF force/torque sensors and load-cell sensing modules for humanoid wrists/ankles/feet
- **Causal link:** VPG disclosed in early 2026 SEC annual report that it received orders from THREE humanoid robot developers in 2025, with prototype + follow-on programs underway; secured an additional $1M order from an existing humanoid customer in early 2026.
- **Why small-base + forced:** VPG's entire revenue is ~$170M/yr (FY2025). Even 3–5 humanoid production wins at scale = 20–50% revenue upside. Its precision strain-gauge technology (via Vishay Weighing Technologies, formerly Revere Transducers) is the exact form factor needed for compliant joint sensing. Not easily substituted.
- **Move status:** Stock has been depressed on margin pressure; robotics thesis has NOT driven a re-rate yet as of mid-2026.
- **Accessibility:** Public, US-listed, liquid enough for institutional small-cap position.
- **Flags:** Execution risk (slow ramp), mix shift needed from legacy industrial weighing.
- **Verdict:** BEST-IN-CLASS candidate — small base, confirmed design wins, not yet re-rated.

### 2. Timken Company (TKR) — SECONDARY (mid-cap, partially known)
- **Ticker:** TKR (NYSE) | **Market cap:** ~$2.8B (mid-cap, not strictly small)
- **Part:** Cycloidal reduction gears via Spinea (Slovakia); harmonic strain-wave via Cone Drive; precision miniaturized gears via CGI Inc.
- **Causal link:** Spinea is **the only European producer** of precision cycloidal gears and **only one of two suppliers globally** that can cover all six axes of small/medium-payload robots. Timken completed Spinea acquisition in 2022 (~$40M sales then). CGI added in 2024.
- **Why small-base + forced:** Spinea revenue was ~$40M in 2022; TKR's total revenue ~$4B — so Spinea is a small, concentrated slice. As humanoid volume scales, Spinea's actuator content could become material. Forced because qualified alternatives are essentially Nabtesco (excluded, Japan-only orientation) and Chinese privates.
- **Move status:** TKR has moved modestly (+15–20%) but humanoid thesis is not fully priced. Morgan Stanley's Humanoid 100 includes TKR; still below prior highs on broader industrial weakness.
- **Accessibility:** Public, liquid US mid-cap.
- **Flags:** Already in Humanoid 100 (some coverage), but robotics is <10% of revenue — not yet a re-rate story. Balance sheet healthy.
- **Verdict:** SECONDARY — mid-cap, partially covered, but Spinea moat is real and underappreciated vs. the Japan/China alternatives.

### 3. Vicor Corporation (VICR) — SPECULATIVE
- **Ticker:** VICR (NASDAQ) | **Market cap:** ~$1.5B
- **Part:** High-density DC-DC power conversion modules (48V bus → local motor drive rails) in humanoid power electronics
- **Causal link:** Vicor's "Factorized Power Architecture" and BCM/PRM modules are the preferred solution for high-power-density robotics where the board space and weight constraints are severe. Humanoid robots run 48V or higher bus to minimize I²R losses and need point-of-load converters at each joint board.
- **Why small-base + forced:** Vicor's total revenue ~$350M. Robot power electronics is nascent. At 20–40 joints per robot × power converter per joint, Vicor content per robot could be $100–300. At 100K robots/year = $10–30M incremental.
- **Move status:** VICR has been volatile; had a significant run on AI datacenter power narrative in 2024, then gave back much of it. Humanoid-specific re-rate has not happened.
- **Accessibility:** Public, US NASDAQ.
- **Flags:** Datacenter power already drove one narrative; market may not reward a second re-rate on robotics without clear design-win disclosure. Competition from Murata, CUI (Bel Fuse sub) in smaller modules.
- **Verdict:** SPECULATIVE — physical link is real but indirect; no confirmed humanoid design-win disclosed.

### 4. RBC Bearings (RBC) via Kaydon Division
- **Ticker:** RBC (NASDAQ) | **Market cap:** ~$6B (mid-cap, border case)
- **Part:** Thin-section precision bearings (Kaydon product line) in humanoid hip/shoulder joints where ring-gear integration demands thin-section profiles
- **Causal link:** Kaydon thin-section bearings are the industry standard for joints requiring large bore with minimal axial/radial envelope — exactly the geometry of a humanoid hip or shoulder socket. SKF and Schaeffler compete but Kaydon has the US defense/aerospace certification legacy.
- **Why small-base + forced:** Kaydon is a division; its robotics exposure is small relative to RBC's $2B revenue. Forced because the form factor (large bore, thin-section, ring-integrated) has few qualified suppliers.
- **Move status:** RBC has had moderate moves on aerospace + defense tailwinds; humanoid angle not priced.
- **Accessibility:** Public, liquid.
- **Flags:** Mid-cap, already has other re-rate drivers (defense aerospace). Robotics optionality is a 2027+ story.
- **Verdict:** LOWER PRIORITY — too large, too diversified, robotics exposure too small to be a pure-play.

### 5. SPG Co. (058610.KQ) — WATCH
- **Ticker:** 058610.KQ (Korea, KOSDAQ) | **Market cap:** ~$300–500M est.
- **Part:** Precision reducers (planetary + strain-wave + cycloidal) — only Korean company making all three types in volume
- **Causal link:** Korean humanoid OEMs (Samsung, Hyundai) have home-country procurement preference. SPG is positioned as the domestic Korean alternative to Japanese reducer monopoly.
- **Why small-base + forced:** Small Korean company; Korean robot OEMs face geopolitical pressure to diversify from Japanese suppliers; SPG is the natural beneficiary.
- **Move status:** Unknown (Korean market, limited English-language coverage).
- **Accessibility:** Public, but Korea-listed — requires ADR or direct Korean brokerage. Not easily accessible to most US investors.
- **Flags:** FX risk, Korean market liquidity, limited English disclosure.
- **Verdict:** INTERESTING but accessibility constrained. Flag for Korea-capable investors.

---

## Ranked Fresh-Candidate Summary

| Rank | Ticker | Name | Part (causal link) | Small-base + Forced? | Move status | Accessible | Clean flag |
|---|---|---|---|---|---|---|---|
| 1 | VPG | Vishay Precision Group | 6-DoF FT sensors for wrist/ankle joints; 3 confirmed humanoid customers disclosed 2025/2026 | Yes — $170M rev, confirmed wins, not priced | NOT moved | US public | Clean |
| 2 | TKR | Timken Company | Spinea cycloidal reducers (only EU producer, one of two global qualified); Cone Drive harmonic | Partial — Spinea is $40–60M sub of $4B parent; moat is real | Modest move, not re-rated on humanoids | US public | Clean |
| 3 | VICR | Vicor Corporation | 48V→local rail DC-DC power conversion at each joint board | Speculative — $350M rev, no confirmed humanoid win | Volatile; datacenters drove prior run | US public | Speculative |
| 4 | RBC | RBC Bearings (Kaydon) | Thin-section precision bearings for hip/shoulder joints | Mid-cap, diversified; robotics optionality only | Moderate moves on aero/defense | US public | Lower priority |
| 5 | 058610.KQ | SPG Co. | All-three-type reducer supplier; Korean OEM home-team supplier | Small, Korea-only, genuine moat if Samsung/Hyundai scale | Unknown | Korea KOSDAQ only | Accessibility constrained |

---

## Captive / Private / China BOM Lines (no actionable public vehicle)

| BOM part | Status | Notes |
|---|---|---|
| Actuators (Figure 03) | **CAPTIVE** — Figure builds in-house | Explicitly confirmed; no external supplier |
| Tactile / fingertip sensors | **CAPTIVE** — Figure built first-gen in-house | Confirmed in Figure 03 announcement |
| Onboard AI compute (Figure "Helix" silicon) | **CAPTIVE** — custom ASIC | Figure designed its own inference chip; no public exposure |
| Battery cells / pack | **CAPTIVE + CHINA** — Figure F.03 custom pack; LG/Samsung for cells | Cells = large-cap Korea; pack assembly = captive |
| Cameras / depth sensors (image sensor) | **PRIVATE/LARGE-CAP** — Sony IMX sensor (large-cap); OmniVision (private/China) | No small-cap public play |
| IMU | **PRIVATE** — Bosch Sensortec (private sub), SBG Systems, mCube | No independent small-cap listed |
| Motor winding (custom) | **PRIVATE** — Lin Engineering, specialty shops | No public pure-play |
| Joint encoders | **PRIVATE/LARGE-CAP** — Broadcom (large-cap), RLS Merilniki (private Slovenia), Bourns (private) | No small-cap public play |
| Wiring harness | **PRIVATE + LARGE-CAP** — Yazaki (private), Aptiv (large-cap) | Humanoid harness = custom; no pure-play public small cap |
| Connectors | **LARGE-CAP** — Amphenol / TE Connectivity / Molex | All large-caps; Nicomatic private |
| Structural / die-cast chassis | **PRIVATE + CHINA** | Mostly China foundries; no actionable public vehicle |
| Thermal management | **PRIVATE** — Laird Thermal (private), Momentive (private sub) | No independent small-cap listed |
| Cycloidal reducers (China) | **CHINA-LISTED** — Zhejiang Shuanghuan, Shaanxi Qinchuan, Ningbo ZhongDa Leader | China A-share only; not accessible |

---

## Coverage Gaps

1. **Apollo 2 BOM** — Apptronik has not published a detailed component list for Apollo 2 (announced 2025). TI modules confirmed for Apollo gen-1 (CES 2025) but exact scope unclear.
2. **Figure 03 external suppliers** — Figure explicitly treats its supply network as confidential. The ~35+ commodity suppliers are unnamed. The "three motor winding, flexible OLED, precise optical" categories are known needs but suppliers unknown.
3. **Force-torque sensor volumes** — VPG confirms humanoid orders but has not disclosed which robot OEMs or exact volumes; could be pre-production/prototype quantities only.
4. **SPG Co. financials** — Limited English-language data; Korean DART filings needed for revenue/margin verification.
5. **Emerging actuation architectures** — Several humanoid OEMs are moving toward linear actuators (ball-screw + BLDC) for legs rather than rotary; this shifts BOM toward precision ball-screw suppliers (NSK, THK excluded; PMI Taiwan potentially relevant but not searched).
6. **Battery BMS standalone** — No search confirmed a small-cap standalone BMS IC supplier differentiated enough to be a pure-play humanoid bet; TI and MPWR (excluded) dominate.

---

*Sources used: Figure AI official announcements, Apptronik TechCrunch/CES coverage, McKinsey humanoid supply chain report, Morgan Stanley Humanoid 100 (excerpts), VPG FY2025 Annual Report (SEC), Timken press releases (Spinea acquisition, CGI acquisition), humanoid.press supplier database, humanoid.guide supply chain report.*
