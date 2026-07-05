# Slice 2 — Sensor Materials & Position-Sensing ICs
*World-Model / Robotics / AV Supply Chain — Wave-2 Widening*
*Authored: 2026-07-05 | 7 web searches consumed*

---

## Thesis Frame

The obvious sensor-system nodes (Lumentum, Coherent, Ouster, Aeva, Novanta) already re-rated. This slice hunts one level deeper: the **materials and ICs that go inside** robot and AV sensors — strain-gauge alloy foil, precision resistors, magnetic/inductive position encoder ICs, Hall-effect chips, and the signal-conditioning ASICs that translate strain-gauge bridges into digital torque signals. Forced-spend dynamic: every humanoid-robot joint (≥20 per bot) needs at minimum one position encoder IC and ideally one force-torque channel; every AV needs ≥4 wheel-speed / steering-position sensors. Volume ramps multiply small bases rapidly.

---

## Candidates

### 1. Vishay Precision Group (NYSE: VPG)
**What they supply:** Precision foil strain gauges (Micro-Measurements brand, originator of Karma/K-alloy designations), precision resistor networks, and force-torque measurement systems. The foil and resistive alloy inside virtually every 6-axis force-torque sensor used in robot arms and humanoid wrists is Micro-Measurements technology.

**Size & forced-spend:** Q1 2026 revenue $84.4 M (annualised ~$338 M). Booked $1.0 M in humanoid-robotics orders in Q1 alone — tiny absolute but represents new demand against a ~$85 M/quarter base. Book-to-bill 1.21, Sensors segment book-to-bill 1.36. Management guided low-tens-of-millions humanoid revenue at 50 % CAGR from 2025 base. The "forced spend" angle is real: no robot arm achieves sub-1 % force accuracy without precision foil gauges and the signal conditioning behind them; there is no credible substitute.

**Already ran? YES — material re-rating has occurred.** Stock up ~216 % YTD as of early July 2026, ~430 % over 52 weeks. Trades at ~270x trailing P/E ($133 per share as of mid-June). The robotics optionality is now well-priced. Included here for completeness and as valuation benchmark; **do not initiate at current levels without near-term revenue de-risking.**

**Accessibility:** US-listed, fully accessible. No China risk.

---

### 2. Melexis (Euronext Brussels: MELE / OTC: MLXSF)
**What they supply:** Pure-play mixed-signal sensor IC designer — magnetic position sensor ICs (Triaxis® Hall-effect 3D technology), inductive position encoder ICs (MLX90520, 22-bit resolution, launched for robotics joints 20–200 mm diameter), current sensor ICs, motor driver ICs. Every joint encoder in a robot arm that uses a magnetic or inductive scheme is a potential socket for a Melexis chip.

**Size & forced-spend:** Market cap ~€3.1 B (~$3.5 B), TTM revenue ~€840–980 M (2025 declined ~10 % on automotive demand weakness; H2 2026 expected to recover). Automotive is 88–89 % of revenue — robotics/industrial is a single-digit slice today. That is the asymmetry: the MLX90520 inductive encoder product is now sampling specifically for robot joints; if humanoid ramps to even 2–5 % of revenue by 2027–28 off a small base, the absolute dollar increment on a ~$1 B revenue run-rate is meaningful relative to current segment size. Inductive position is technically superior for joint sensing (immune to magnetic stray fields from coil motors) — this is an important product-fit advantage.

**Already ran? NOT MEANINGFULLY.** Stock underperformed the Belgian semiconductor sector (which was +65 % over the past year) and the broader Belgian market (+15 %). Stock ranged €48–87 over 52 weeks; trading near €78, close to the analyst average target of €71 (consensus slightly underwater vs. current price, but range to €92 high target). Automotive headwinds (EV regulation changes, China pricing agreements) masked robotics optionality. This is the most compelling "variant perception" name in the slice: the market is repricing Melexis as a cyclical auto-semiconductor, while the product pipeline is quietly repositioning it as a robot-joint position-sensor specialist.

**Key catalyst:** July 29, 2026 earnings — H2 2026 revenue recovery guidance and any quantification of robotics design-win pipeline.

**Accessibility:** Euronext Brussels; US investors access via ADR/OTC (MLXSF) or broker with Euronext access. Liquidity adequate for mid-size positions. No China manufacturing risk (Belgium HQ, third-party foundry, TSMC/GlobalFoundries).

---

### 3. Allegro MicroSystems (Nasdaq: ALGM)
**What they supply:** Hall-effect current sensors, magnetic speed and position sensors, motor-driver ICs. Dominant in automotive wheel-speed / ABS sensors and motor-current sensing. Position sensing for robot joints (speed feedback, commutation) is a direct adjacency — product families overlap substantially with what Melexis offers.

**Size & forced-spend:** Market cap ~$10.3 B (as of July 3, 2026 at $55.80). TTM revenue roughly in the $700–900 M range (precise 2026 figure not confirmed in searches). The stock already rallied significantly — 52-week low $22.41 to high $71.77, currently $55.80. Strong Buy consensus (11 analysts), TD Cowen $70 target.

**Already ran? PARTIALLY.** Stock has re-rated materially off the 52-week low but pulled back from the $71 high. Less dramatically re-rated than VPG, but not unpriced. At $10 B+ market cap this is no longer micro-cap territory. Included because it remains the best-liquid US-listed pure-play on Hall-effect position/speed sensing and robotics exposure is genuine, but it is a mid-cap with partial re-rating already reflected.

**Accessibility:** US-listed Nasdaq, fully liquid. No China risk.

---

### 4. indie Semiconductor (Nasdaq: INDI)
**What they supply:** Mixed-signal SoCs for automotive ADAS and adjacent robotics — LiDAR signal processing, radar (77 GHz), vision/computer vision, ultrasound. Acquired ams OSRAM's CMOS image sensor group (fabless) for €40 M in 2026. Supplies signal-processing ASICs that sit behind multi-modal sensor arrays.

**Size & forced-spend:** Market cap ~$1.1 B, TTM revenue ~$217–266 M. Unprofitable (guided to profitability in 2027 at $24.5 M net income). Claims active humanoid robotics design wins with "market leaders" in humanoid robotics, 77 GHz radar in global field trials with a Tier 1 partner for robot applications. Revenue base is small; if humanoid ramps, INDI's per-unit ASP (full SoC vs. a single sensor IC) could be high.

**Already ran? SOMEWHAT — but not VPG-scale.** Stock was around $4–5 range as of late June 2026, with analyst average target ~$5.50 (53 % above then-price). Valuation is not stretched relative to the growth path if profitability arrives on schedule. The ams OSRAM CMOS sensor acquisition is genuinely additive to humanoid hands/tactile camera sensing.

**Risk:** Persistent losses, execution risk on profitability timeline, and the humanoid robotics revenue claim has not yet shown up materially in reported numbers. High variance name.

**Accessibility:** US Nasdaq-listed, good liquidity. No direct China risk, though some automotive customer concentration in China (common for ADAS chipmakers).

---

### 5. AMS-Osram (SIX Swiss Exchange: AMS)
**What they supply (post-divestiture):** Digital photonics — VCSELs, LEDs, optical sensors, Time-of-Flight distance sensing ICs, spectral sensing, biosensing. After selling the non-optical position-sensor portfolio to Infineon for €570 M (closed ~July 2026), AMS-Osram is now a pure photonic-sensing/illumination company. Relevant for robot ToF ranging and structured-light sensing.

**Size & forced-spend:** Market cap ~$2.0 B (post-divestiture, trimmed balance sheet, leverage ratio 2.5x). TTM revenue ~€3.3–3.8 B. The Infineon sale proceeds clean up the balance sheet; company intensifying investment in multi-zone ToF for robotics.

**Already ran? PARTIALLY — but for different reasons.** The stock reflects divestiture news and debt reduction. The optical-sensing robotics exposure (ToF, VCSEL, spectral) is real but less direct to the "sensor materials & ICs inside robot sensors" frame of this slice. Primarily a photonics name now.

**Accessibility:** SIX Swiss Exchange; accessible to US investors via broker with Swiss exchange access or ADR. No direct China risk in manufacturing.

---

## Summary Ranking

| Rank | Ticker | What They Supply | Why Small-Base & Forced-Spend | 6-12m Move | Accessibility |
|------|--------|-----------------|-------------------------------|------------|---------------|
| 1 | MELE (Euronext) | Inductive & magnetic position encoder ICs; MLX90520 for robot joints; Hall-effect current/position sensors | ~€840 M rev base, 88 % auto; robotics is <5 % today but inductive encoder product is designed specifically for robot joints; auto headwind masking optionality; stock lagged sector by >50 pp | NOT MOVED (underperformed sector) | Good — Euronext Brussels / OTC MLXSF; no China |
| 2 | INDI (Nasdaq) | ADAS/robotics signal-processing SoCs; 77 GHz radar; CMOS image sensor for robot perception; multi-modal sensor ASICs | ~$217–266 M rev, unprofitable but path to 2027 profit; humanoid design wins claimed; ams OSRAM CMOS acquisition adds tactile-camera sensing | PARTIAL MOVE — in $4–5 range, below prior highs; 53 % upside to analyst avg | Good — US Nasdaq; mild China customer concentration |
| 3 | ALGM (Nasdaq) | Hall-effect wheel-speed / position sensor ICs; motor-current sensing; motor drivers; direct robot joint encoding | ~$700–900 M rev, auto-heavy but large robotics adjacency; per-joint ASP leverage | MOVED (52-week low $22 → $55; partially re-rated but off $71 high) | Good — US Nasdaq; no China risk |
| 4 | AMS (SIX) | VCSELs, ToF ICs, spectral sensing for robot perception post-divestiture | ~€3.3 B rev (large base now); photonics for robot distance sensing; balance sheet cleanup is catalyst | PARTIAL — divestiture repricing ongoing; not a clean robotics materials play | Partial — SIX Swiss; no direct China manufacturing risk |
| 5 | VPG (NYSE) | Precision foil strain gauges (Karma/K-alloy); force-torque measurement systems; precision resistor networks | ~$338 M annualised rev; foil gauges are essential, non-substitutable inside every FT sensor | ALREADY RAN — +216 % YTD, +430 % 52-week; 270x P/E; priced | Good — US NYSE; no China risk |

---

## Key Finding: The One Genuinely Un-Crowded Name

**Melexis (MELE)** is the most compelling candidate. It sits at the intersection of: (a) irreplaceable technology — inductive encoder ICs with 22-bit resolution purpose-built for robot joints, immune to motor-coil stray fields; (b) a temporarily depressed price anchored to automotive cycle weakness that obscures the robotics ramp; and (c) a specific near-term catalyst (July 29, 2026 earnings + H2 recovery guidance). The stock has underperformed the Belgian semiconductor index by more than 50 percentage points over the last year despite launching robotics-specific product families. That is textbook variant perception.

indie Semiconductor (INDI) is the second-best idea — smaller base, more explosive upside if humanoid production scales, but requires more execution faith.

---

## Coverage Gaps

1. **Strain-gauge foil pure-plays remain private or subsidiary.** Hamilton Precision Metals (Evanohm foil) is a subsidiary of AMETEK (large cap, already liquid, not a pure-play); BCM Sensor and Zemic are private. MFL Strain Gauges (Northern Ireland) is private. No accessible micro-cap pure-play was surfaced in this slice for the raw alloy/foil manufacturing layer — this node appears to be a coverage gap requiring targeted private-market research or a search for Japanese specialty metals companies (e.g., Hitachi Metals subsidiary, Ohkura Shoji) that may have small listed vehicles.

2. **Tactile / haptic sensor pure-plays are predominantly private.** XELA Robotics, GelSight, SynTouch, Pressure Profile Systems, Chinese players (Tashan, PaXiniTech) — all private. No accessible small-cap public pure-play on tactile skin or haptic feedback for robot hands was identified. This is a real gap in the investable universe and likely represents a future IPO/SPAC opportunity.

3. **Signal-conditioning ASIC tier for force-torque sensors.** ATI (robot FT sensor leader) is a subsidiary of Schunk (private). HBM/HBK is part of Spectris (mid-cap UK, not a pure-play). FUTEK is private. The custom ASIC layer (analog front-end + SPI readout) is either done in-house by the FT sensor maker or sourced from standard precision ADC suppliers (ADI, TI — both large-cap, already priced). No small-cap ASIC specialist for FT sensing was surfaced as a standalone public entity.

4. **Japanese precision resistor makers.** Susumu, Kamaya, KOA, Bourns Japan — Japanese listed precision resistor specialists that supply the bridge resistors inside strain-gauge circuits. These were not fully investigated due to search budget constraints. KOA Corporation (Tokyo: 6999) is a listed mid-cap Japanese precision resistor specialist worth a separate focused search.

5. **iC-Haus (Germany) and RLS (Slovenia/Renishaw JV)** — both confirmed private. The encoder IC layer below Melexis and Allegro has no other accessible public vehicle at small-cap scale.

6. **Rotary-encoder mechanical + IC combination suppliers in Japan/Taiwan.** Companies like Nidec (large-cap) and Kyowa Electronic Instruments (small-cap, listed in Japan, specialises in strain gauges and data recorders) warrant a dedicated Japan-focused pass. Kyowa was not fully diligenced here.

---

*Search budget consumed: 7 of 7. Further diligence on Melexis (MELE) and KOA (6999.T) recommended as immediate next steps.*
