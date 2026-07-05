# Melexis (MELE.BR / MLXSF) — Wave 3 Causal Diligence

**Verdict: KILL (on the 2-3yr multiplication test) — hold as a watch-list "real causal link, wrong timeframe."**

Date: 2026-07-05 · Time-boxed, 6 searches.

---

## Step 0 — Elimination Gate

| Test | Reading | Pass? |
|---|---|---|
| (a) Financial health | Fabless, over-cycle targets ~45% GM / ~25% EBIT. FY2025 rev €839.6M (-10% YoY), earnings €112.5M (-34% YoY) — cyclical trough, not distress. Dividend held €3.70. FY26 guided flat H1, growth H2, GM already recovering. Balance sheet clean. | **PASS** |
| (b) Management execution | Guided the auto inventory correction early and honestly; delivered 19 new products in 2025; explicit robotics design-win disclosure. Credible, non-promotional. | **PASS** |
| (c) Re-rating grade (did it genuinely LAG?) | De-rated hard on the auto/EV inventory cycle. BUT BofA (Underperform) argues it trades at a *premium* to global peers — 10.4x 2027 vs 9.8x peer avg — on below-peer growth (1% rev CAGR '24-27). So it lagged the AI/automation names on *price action*, but is **not statistically cheap**. Absolute P/E compressed from 70x (2020) to mid-teens trough. | **PARTIAL** — has not "run" on robotics, but no valuation cushion. |

Gate result: **PASSES** (healthy + well-run + has not re-rated on robotics). Premise "it lagged" is directionally true.

---

## 1. Causal Chain — rating: **PROBABLE** (design-in real; not exclusive)

Every articulated/geared robot joint physically needs absolute position feedback, typically **dual** (motor-side + output-side after the gearbox, because harmonic-drive elasticity decouples the two). This is airtight for "robots need encoders."

Is Melexis *designed in* (not just "robots need encoders")?
- Dedicated robotics silicon: **MLX90520** (22-bit inductive encoder, 20-200mm joints), **MLX90514-robotics** (16-bit dual-input), Arcminaxis 18-bit Hall angular encoder, MLX90510 resolver IC.
- Published "Encoders & Resolvers for Robot Joints" application flyer + robotics vertical page.
- **FY2025 disclosed "a significant win with a high number of inductive position sensors per robot"** — concrete design win, multiple parts/robot (content-per-robot leverage).
- Tactile expansion: **Tactaxis** 3D-force sensor integrated on Faive Robotics / ETH Zurich humanoid hand — widens per-robot content beyond position.

But NOT "robots need MELEXIS." The joint-encoder socket is contested by entrenched merchants: **RLS/Renishaw** (AksIM-2, Orbis — already in PAL Robotics knee/wrist/elbow), **iC-Haus**, **Allegro**, **AMS-Osram**. Melexis competes on cost-vs-optical and automotive-grade robustness (ISO 11452-8 stray-field immunity, SIL 3), not on a unique lock-in. Rating capped at **probable**, not airtight.

## 2. Multiplication Math — **NO** (not on a 2-3yr horizon)

- Base: FY25 rev €839.6M. Non-auto (industrial+robotics+consumer+data center) ≈ **12% ≈ €100M**. Robotics is a *subset* → today **<2% of sales, a rounding error**.
- Content/robot (physically necessary): humanoid ≈ 28-40 actuated DOF; dual sensing → ~20-40 Melexis-addressable position ICs/robot. At ~$2-4 ASP → **~$50-150 encoder content/robot**, plus tactile.
- Scenarios (Melexis take at ~30% share):
  - 2027-28 realistic industry volume (sub-500k humanoids/yr) → Melexis robotics rev **sub-€30-50M**. Real, but does not multiply a €840M base.
  - 1M units/yr × $100 × 30% ≈ **$30M** → still a rounding error.
  - 10M units/yr (bull, ~2030+) × $100 × 30% ≈ **$300M** → +~35% on base — but that is a 5-7yr optionality story, NOT 2-3yr.

**Arithmetic verdict:** physically-necessary link is real; the near-term earnings multiplier is not. This is long-dated optionality riding on top of an auto-cycle recovery bet, which fails the thesis's "MULTIPLY revenue in 2-3 yrs" bar.

## 3. Red-Team

- **(i) Vertical integration (Tesla/large labs insource):** LOW risk *on the IC*. Tesla insources the actuator/harmonic drive, but the position-sensing IC is automotive-grade mixed-signal analog with functional-safety (SIL 3) and stray-field immunity — low-value, high-effort to insource vs. a proven $2-3 merchant part. Insourcing pressure lands on the actuator, not the encoder chip. Melexis stays a merchant-silicon beneficiary.
- **(ii) IP/licensing speculation:** N/A — upside is **product/order sales** (unit ICs), not licensing. Confirmed clean.
- **(iii) Auto cyclicality masks the signal (value trap):** HIGH. 88% auto. Any robotics ramp is dwarfed and obscured by the auto inventory cycle; you're primarily buying an auto-semi recovery, and BofA flags no valuation cushion (premium to peers, ~1% rev CAGR). The robotics narrative can be "true but invisible" in the P&L for years.
- **(iv) Socket competition:** HIGH. RLS/Renishaw already shipping in named humanoid joints; iC-Haus, Allegro, AMS contest the same socket. No exclusivity → share and ASP both at risk exactly when volume arrives.

## Coverage gaps
- No hard $ content-per-robot or units-per-joint figure from Melexis IR/analyst decks (design win is disclosed but unquantified).
- Robotics revenue not broken out separately from the ~12% non-auto bucket — cannot size the current base precisely.
- Identity of the disclosed "high number of inductive position sensors per robot" customer unknown (industrial vs humanoid; China/EU/Korea-led per mgmt).
- Tesla Optimus / major-lab encoder sourcing unconfirmed (in-house vs merchant, and which merchant).
- BofA 2027 multiples are analyst estimates, not primary filings — verify before sizing.
