# TARGET PROFILE — who we are actually looking for
*Written 2026-07-15 after 74-fire audit. This is the single most important file in the KB.*

## The core insight (from 74 fires of evidence)
Every name that has SURVIVED gate checks (Seyond 7/8, Intops 5/8, Asensing 3/8) was built specifically for this market. Every name that keeps getting KILLED is a legacy industrial that might incidentally benefit. **We are not looking for companies that might benefit. We are looking for companies that exist BECAUSE of this market.**

## Ideal target
1. **Founded ≤10 years ago** — or went through a genuine strategic pivot within the last 3-4 years, with new management and new capital allocation explicitly targeting this market. A company founded in 1971 (THK) or 1907 (SKF) whose humanoid exposure is 1-5% is not interesting regardless of how cheap it is.
2. **Thesis-market as primary business** — >30% of current revenue OR >50% of near-term (2-year forward) revenue comes from humanoid/AV/world-model buyers. NOT "they supply a component that might be used in robots."
3. **Management explicitly built/pivoted for this market** — CEO has spoken about the market by name on earnings calls or in IPO filings. This is a proxy for conviction and capital allocation discipline.
4. **Small enough that the thesis is the PRIMARY driver** — target market cap <$500M. At this size, a genuine humanoid ramp is a stock re-rating event, not a footnote.
5. **Named buyers in primary filings** — not press speculation, not "industry sources," not "we serve the robotics sector." A named OEM in an IPO prospectus, 互动易 IR filing, DART filing, or SEC 10-K/20-F.

## What to SKIP (save compute)
- Any company older than 10 years where thesis-market exposure is <15% — even if it's cheap, the stock will be driven by its 20 other businesses.
- Any company in a SATURATED CATEGORY (see dead-ends.md) — precision-motion/bearings/reducers/mainstream-chips are mined out.
- Any company where "humanoid" appears only in a product-brochure sentence or TAM slide, not as a named customer.
- EDGAR EFTS full-text sweep — 16 consecutive null results. Do not re-run unless there is a specific new reason.
- Legacy industrials with marginal adjacency — stop looking for the 30th ball bearing company.

## Quality-adjusted valuation gate (replaces the binary +60% kill)
The old gate (>+60%/12m = kill) is too blunt. Use this instead:

**QUALITY SCORE = (thesis-exposure % × causal-lock-in strength × near-term revenue visibility) / (EV/revenue vs. pre-thesis-era comps)**

- If Quality Score > threshold AND the company fits the target profile above → WATCH even if stock has moved 40-70%
- If the company is a legacy industrial with marginal exposure → kill at +30% (the old companies don't deserve the benefit of the doubt)
- A 10-year-old company with 50% revenue from Unitree and 1 named contract that's up 45% → might still be the most interesting name in the KB
- A 50-year-old industrial with 3% robotics adjacency that's up 25% → skip, the upside case requires too many things going right

**Operationally:** flag the founding year + thesis-exposure % BEFORE checking 12m price. If both are favorable (young company, high exposure), lower the kill threshold to +80%; if unfavorable (old company, low exposure), lower it to +30%.

## The best sourcing angles for finding the right targets
(These find companies that EXIST for the market, not companies that might benefit)

1. **VC portfolio mining** — Nvidia NVentures, Samsung Next, Bosch Ventures, Hyundai Motor Group Strategic Finance, GV (Google), LG Technology Ventures all invest in the direct supply chain. Their portfolio companies are the actual suppliers. Look at their websites and announced deals.
2. **Chinese Series A/B rounds, 2021-2025** — the cohort of companies that raised ¥50-500M specifically to supply humanoid/AV OEMs. Many are now approaching STAR Market/HKEX IPO. High Zong/高工机器人 tracks these systematically.
3. **IPO prospectuses from buyers** — Unitree's STAR Market prospectus has a real supplier appendix. Agility Robotics' S-4 (when filed) will too. UBTECH's HK annual report has supplier disclosures. Read these carefully — every named supplier is a lead.
4. **Korean KOSDAQ new listings 2023-2025** — Korea has the most transparent small-cap robotics IPO market globally. Search DART for companies that IPO'd with >30% revenue from hyundai/boston-dynamics/bear-robotics/samsung-bots.
5. **HK A1 filings (HKEX)** — Asensing was found this way. Search HKEX A1 applications in the robotics/AV space from 2024-2026.
6. **SAM.gov + NATO contracts** — US government robotics programs (DARPA, Army, Navy) name their suppliers. These are often small companies with a highly credible single customer.
7. **Chinese trade press (高工机器人, 机器之心)** — they publish named supply chain relationships 3-6 months before formal filings. Search `供应商 + 独家 + 人形机器人 + 2025/2026`.

## Business-model-fit check (added Fire 76, after the TrunkTech near-miss)
VC-portfolio-mining hits (Bosch Ventures, Nvidia NVentures, etc.) are NOT automatically hardware-component suppliers — the same funds also back AV solutions/software companies and fleet operators. **Before running the 4-gate check on any VC-portfolio or forward-listing find, confirm what the company actually SELLS**: a physical unit that goes into an OEM's bill-of-materials (sensor, actuator, motor, chip, connector, structural part) vs. a software/driving-system/service sold to end-users or deployment sites. A young (<10yr), thesis-focused, real-VC-backed company can still fail the screen instantly if it's the latter — TrunkTech (Bosch-backed since 2019, HK Chapter-18C filer, genuinely built for AV) still killed on this basis: it installs its own driving stack onto OEM-supplied trucks and sells to port/logistics deployment sites, not a component into anyone's BOM. This is a distinct, faster fail-mode from the age/exposure quick-kill — check it FIRST, before age or exposure %.

## Confirmed twice now (added Fire 90, after the HSAI downgrade)
The "What counts as AV" lesson below was validated a SECOND time at Fire 90: HSAI's carried 7/8 score rested on the identical error (Mercedes-Benz L3, an ordinary passenger-vehicle ADAS program per Hesai's own 6-K segment taxonomy, was being scored as "robotaxi/L3+-grade"). **Operational upgrade to the rule: before crediting ANY thesis-exposure claim that leans on a named passenger-vehicle-OEM program, check the SELLING COMPANY'S OWN customer/segment classification in its primary filings first** — companies in this space usually already draw an explicit ADAS-vs-robotaxi/robotics line in their own disclosures (Hesai's 6-K does), it just wasn't being read that way. This is now a standing pre-check for any name whose causal-link story includes a named consumer-automaker buyer, not only a periodic staleness-guard trigger. See companies/HSAI.md Fire 90, decisions-log.md.

## What counts as "AV" (added Fire 89, after the Seyond downgrade)
This campaign's "humanoid/AV/world-model" thesis means **robotaxi/AV-fleet/L4+ autonomy and humanoid embodied-AI demand** — NOT ordinary passenger-vehicle L2/L3 driver-assist (ADAS). A lidar/sensor company selling into NIO/GAC/SAIC-VW/Leapmotor-style consumer passenger cars is serving the mainstream automotive-ADAS market, a much larger, more mature, and differently-priced market than the thesis this campaign screens for — even though the underlying sensor technology looks similar. **Before crediting any "AV" thesis-exposure %, decompose it: is the named buyer/program a robotaxi fleet, an L4+ autonomy developer, or a humanoid/embodied-AI OEM (qualifying) — or is it a passenger-vehicle OEM's L2/L3 driver-assist program (NOT qualifying, regardless of how the company markets itself)?** This distinction was missed for 15+ fires on Seyond Holdings (2665.HK) — see decisions-log.md Fire 89 and companies/SEYOND.md — where passenger-ADAS lidar revenue to NIO was counted as AV thesis exposure. Any current or future shortlist/WATCH name with "AV" in its causal-link story should have this decomposition run explicitly, not assumed.

## What the KB has been getting wrong (the honest diagnosis)
- Spending 2-3 fires on Klingelnberg (founded 1863, gear-grinding) before confirming no named humanoid buyer has ever been disclosed
- Running EDGAR EFTS 16 consecutive times with zero results (stopped working months ago)
- Finding and killing 15+ companies in "precision-motion" when the category was clearly saturated at fire 20
- Carrying OMG.L (1984) and KLIN.SW (1863) as WATCH placeholders for dozens of fires without genuine 4-gate diligence
- Looking for "exposure" to the theme rather than companies "built for" the theme
