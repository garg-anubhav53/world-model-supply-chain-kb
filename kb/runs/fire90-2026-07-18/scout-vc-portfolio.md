# Fire #90 — VC Portfolio Mining, 30-60 Day Window (mid-May through 2026-07-18)

Scope: Nvidia NVentures, Samsung Next, Bosch Ventures, Hyundai CRADLE, GV, LG Technology Ventures, Qualcomm Ventures.

## Pre-existing KB context (found via grep before starting)
dead-ends.md already contains an explicit prior-fire finding for this EXACT task:
> "VC portfolio mining (9-fund list incl. Nvidia NVentures, Samsung Next, Bosch Ventures, Hyundai CRADLE, GV, LG Technology Ventures, Qualcomm Ventures, Schaeffler Ventures, Amazon Industrial Innovation Fund) — 30-60 day window, RE-CONFIRMED near-fully-exhausted for physical-BOM-component finds. Every recent (May-July 2026) deal from these funds backs an OEM/integrator (Walden Robotics, Neura Robotics, Agility, Unitree) or a software/AI-model company (Acumino) rather than a physical-component supplier. Recommend not re-running these specific 9 funds until their next quarterly deal-flow cycle (~Sept-Oct 2026)."

This fire independently re-ran the search anyway (per orchestrator task) and the result below CONFIRMS that recommendation still holds as of 2026-07-18.

## Per-fund findings (last 30-60 days)

### 1. Nvidia NVentures
- **Gradium** (Paris, voice-AI dev tools) — $30M extension to $100M+ seed, Nvidia joined 2026-07-08/09. Off-thesis: consumer/enterprise voice-AI software, zero humanoid/AV/robotics exposure. NOT IN KB — new to KB but trivially off-thesis, not addable.
- **Revolut** — ~$196-200M stake, fintech. Irrelevant, not robotics-adjacent at all.
- No hardware/robotics-BOM deal found in window.

### 2. Samsung Next
- **Walden Robotics** — Samsung Ventures/Samsung Next participated in $300M round disclosed 2026-07-15, $1.1B valuation (Toyota Research Institute spinout, "full-stack Physical AI," general-purpose robots deployed at a Toyota plant). **DEDUP-SKIP** — already in KILL-LIST.md multiple times (Fire 81 kill, reconfirmed Fire 82 dead-ends, reconfirmed again in the 9-fund fire): business-model-fit fail (sells/deploys whole robots-as-a-service, not a BOM component) + oversized ($1.1B > $500M cap).
- Samsung Electronics corporate-level announcement of ₩19T humanoid robot production base in Gumi — not a VC portfolio deal, not a specific ticker/company, not actionable.

### 3. Bosch Ventures
- Latest logged deal: **Boyin Innovation Alliance** (Bosch Ventures/Boyuan Capital-Galbot JV), 2026-05-15, within window. **DEDUP-SKIP** — already in KILL-LIST.md as "Boyin Innovation Alliance = already-tracked Bowintec," killed on business-model-fit (sells a complete dual-arm mobile robot, not a BOM component).
- No other in-window Bosch Ventures hardware/robotics deal surfaced (other 2026 activity — Neurophos, Cloover — predates window or is unrelated photonics/climate-tech).

### 4. Hyundai Motor Group CRADLE
- **Xnergy Autonomous Power** — Accuron Technologies + Hyundai CRADLE co-investment press activity dated around July 2026 (original investment actually Jan 2025 per Tracxn; this looks like a follow-on/PR re-surfacing). **DEDUP-SKIP** — already flagged in campaign as private/sub-threshold ("Xnergy Autonomous Power Technologies (private/sub-threshold)" in the already-killed list).
- No other in-window CRADLE deal found. CRADLE's own portfolio/news pages remain thin on itemized recent announcements (a recurring tooling gap noted in prior fires too).

### 5. GV (Google Ventures)
- In-window deals found: **Nebex** (space fintech, $30M seed, 2026-06-30), **MOTHER.tech** (AI creative app, $15M seed, 2026-06-02), **Odyssey** (Series B $310M/$1.45B val, 2026-06-18), **Verse** (Series B $54M, 2026-06-19).
- None are robotics/hardware/BOM-component related — all software/fintech/consumer-AI. Zero thesis relevance. No candidate.

### 6. LG Technology Ventures
- **Config** (private, Samsung Venture Investment-led w/ Hyundai ZER01NE/LG Tech Ventures/SKT America/GS Futures/Kakao Ventures, $27M seed, May 2026) — **DEDUP-SKIP** — already in KILL-LIST.md: business-model-fit fail (sells structured motion/sensor training data, not a physical BOM unit).
- **Drive Powerline** ($7M seed, 2026-02-09, EV battery-connection AI software) — outside the 30-60-day window (Feb 2026) and off-thesis anyway (software solution, not a physical component, not humanoid/AV-specific — ordinary EV).
- **Cloaked** — appears to be a consumer privacy/identity-protection product, not robotics-adjacent; not pursued further (clearly off-thesis on a quick check).
- No new in-window hardware/BOM candidate.

### 7. Qualcomm Ventures
- **Neura Robotics** — up to $1.4B round. **DEDUP-SKIP** — already tracked/killed repeatedly in KB (mega-cap OEM, off-thesis on business-model-fit: it's the humanoid OEM itself, not a supplier).
- **Hark** — $700M Series A at $6B valuation, disclosed 2026-05-21 (within window), Qualcomm Ventures among many participants (also Nvidia, AMD Ventures, Intel Capital, Salesforce Ventures, etc.). Hark builds "personal AI hardware" — a vertically-integrated consumer AI-assistant device company (multimodal models + native hardware + interface), founded by Brett Adcock (also Figure AI founder). **BUSINESS-MODEL-FAIL / off-thesis**: this is a consumer AI-gadget OEM, not a humanoid-robotics/AV-robotaxi component supplier, and at $6B valuation it's also wildly oversized. Not addable regardless.
- $150M India Strategic AI Venture Fund (Feb 2026) — a fund-of-funds commitment, not a single portfolio company, not actionable, and also outside window.
- No physical-BOM-component candidate found in window.

## Structural pattern check
Confirmed AGAIN this window: every hardware/robotics-adjacent deal from these 7 funds in the last 30-60 days backs either (a) a finished-robot/OEM/integrator play (Walden Robotics, Neura Robotics, Boyin Innovation Alliance/Bowintec), (b) a training-data/software company one step removed from hardware (Config), or (c) an unrelated consumer-AI hardware/software company with zero humanoid/AV exposure (Gradium, Hark, GV's slate). Zero physical BOM-component suppliers surfaced. The "funds chase integrators/software, not component suppliers" pattern fully holds and shows no sign of reversing.

## Recommendation
Consistent with the existing dead-ends.md guidance: do not re-run this specific 7-9-fund list again until their next quarterly deal-flow cycle (~Sept-Oct 2026), or pivot future fires to a component-keyword-first search method / expand to other CVCs (e.g., the Chinese strategic CVC set — Xiaomi, Li Auto, Tsinghua Holdings Capital, Fosun Venture Capital — already flagged elsewhere in dead-ends.md as more productive for this thesis).
