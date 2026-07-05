# S4 — Photonics Subcomponents: Inside the Transceiver & LiDAR Stack
**Wave 2-Widen | World Model Supply Chain**
*Memo date: 2026-07-05 | Constraint: ≤7 web searches (used: 7)*

---

## Thesis Frame

The primes — Coherent, Lumentum, Ouster — have been repriced. The thesis here is one layer down: who supplies the **guts** those primes consume to build the 800G/1.6T transceivers and solid-state LiDAR sensors now entering volume production? The spend is forced (network operators cannot slow AI cluster build-out; AV/robot integrators cannot defer their sensor roadmaps) and, at current run rates, the substrate/epi/modulator suppliers will see revenue try to multiply off tiny bases. Most of the interesting names are still micro/small-cap.

Key categories hunted:
- InP wafers & epiwafers (substrate layer beneath all datacom lasers)
- MOCVD/MBE epitaxy growth equipment (the tool that deposits laser-active layers)
- Optical interposers / integrated photonic platforms
- Thin-film lithium niobate (TFLN) modulators
- Specialty optics / infrared optics subcomponents
- Compound-semiconductor photodetectors (InGaAs/APD) for LiDAR & sensing

---

## Candidate Cards

### 1. AXT, Inc. (NASDAQ: AXTI)
**What they supply:** Indium phosphide (InP) and gallium arsenide (GaAs) single-crystal substrates — the raw wafers that Coherent, Lumentum, and laser-chip foundries grow their laser epitaxy on. InP is the only practical substrate for 800G/1.6T edge-emitting lasers (EMLs) and photodetectors.

**Why forced-spend & small base:**
- FY2025 TTM revenue ~$88M; InP ran +250% QoQ in the Q3 2025 surge. Q1 2026 revenue $26.9M (+39% YoY), non-GAAP gross margin recovered to +29.9% from –6.1% a year earlier.
- InP backlog hit a record $60M+ in early 2026. Coherent's 6-inch InP wafer line needs substrate supply; Lumentum's expansion to 6-inch will too. Only a handful of qualified InP substrate suppliers exist globally; AXT, Sumitomo, and a German private (Freiberger) hold most capacity.
- In April 2026 the company raised ~$550M in equity to fund capacity expansion — enormous relative to the revenue base, signaling hyperscaler-grade demand visibility.
- Northland raised PT to $125 (Outperform). Revenue at $88M in FY2025; if InP grows 3–4x by FY2027 (consistent with 800G → 1.6T volume ramp), AXT revenue could reach $200–250M range.

**Key risks:** Export controls on compound semiconductors to China could disrupt AXT's China-based manufacturing (raw material processing, furnace recycling); vertical integration in China is cost advantage but also geopolitical exposure. Already ran hard (stock had a $64.25 offering price in 2026 vs. prior-year lows near $4–5). **Partially re-rated** — check current price vs. $64 offering.

**6–12m move read:** Partially ran. The $550M raise at $64.25 was a major re-rating event. Upside from here requires InP revenue growth to materialize ahead of skeptic case; not a clean uncrowded setup any longer but the fundamental forcing function is intact.

**Accessibility:** US-listed, no direct China-exposure risk to US investor (operations in China, but listed NYSE/Nasdaq).

---

### 2. IQE plc (AIM: IQEP.L)
**What they supply:** Compound semiconductor epiwafers (epitaxially grown wafer stacks) — specifically InP epiwafers for optical connectivity. IQE doesn't make the final laser chip; it grows the specialized semiconductor "recipe" layers on a substrate that Coherent/Lumentum then process into laser dies.

**Why forced-spend & small base:**
- June 2026: IQE signed a multi-year agreement with Tower Semiconductor for InP epiwafer supply into AI datacenter optical connectivity — the first major disclosed commercial win tying IQE directly into the AI optics supply chain.
- Revenue base is small (~GBP 125–140M range TTM); the epiwafer segment is a fraction of that. A multi-year Tower deal growing from single-digit to double-digit millions would be a meaningful revenue step-up.
- Tower Semiconductor (Intel spin-out candidate) is aggressively building an InP photonics foundry; IQE is effectively the outsourced epiwafer kitchen for any InP foundry that doesn't want to run MOCVD in-house.

**Key risks:** AIM-listed (London), so liquidity is thin for US investors; GBP currency risk; IQE has historically disappointed on margin and execution; the Tower relationship is non-exclusive. Stock has already moved on the Tower deal announcement — check current price vs. pre-announcement.

**6–12m move read:** Moderate re-rating post Tower deal. Story depends on volume ramp timing at Tower's InP line — likely H2 2027 rather than 2026. May be another 6–12m of waiting before revenue inflects.

**Accessibility:** AIM: IQEP.L — accessible to US investors via ADR or international brokers; moderate liquidity risk. No China supply chain risk.

---

### 3. Riber S.A. (Euronext: ALRIB)
**What they supply:** Molecular Beam Epitaxy (MBE) production systems — the ultra-high-vacuum deposition tools used to grow quantum-dot laser structures, GaAs/InP epitaxial films, and precision photonic device layers. Riber has dominant market position in production-scale MBE globally.

**Why forced-spend & small base:**
- Riber's market cap was ~€28–35M (approximately $30–38M USD) as of mid-2026 — a genuine microcap.
- In late 2025 / early 2026: received orders for two MBE 6000 production systems for delivery in 2026 from a European vertically integrated photonics company (applications cited: AI datacenter optical connectivity, high-power LiDAR light sources, medical/industrial). Also received a third MBE 6000 order in the same month for quantum-dot laser epiwafer production (QD Laser datacom customer).
- The quantum-dot laser angle is important: QD lasers for datacom are a distinct InP-free path (GaAs substrate), and Riber is the MBE tool of record for QD production. If QD lasers take share in CPO/co-packaged optics (lower power, lower noise floor), Riber is the only practical tool supplier.
- Revenue base ~€20–25M; two MBE 6000 systems at ~€3–5M ASP each = material step-up. The backlog inflection in 2025/early 2026 reportedly drove ~+450% stock appreciation from trough.

**Key risks:** Already had a large move (+451% per one source) — critically need to verify current price vs. pre-run levels. Microcap liquidity (Euronext Paris, thin float). Revenue recognition lumpy (tool delivery, not recurring). Customer concentration. Not widely followed by US investors.

**6–12m move read:** May already have run substantially. If the +451% figure is accurate peak-to-peak, the easy money is gone. The fundamental driver (MBE orders for AI optical + QD lasers) is real and multi-year, but valuation may have overshot.

**Accessibility:** Euronext Paris: ALRIB — accessible via interactive brokers; EUR FX; thin float — sizing must be small. No China risk.

---

### 4. Aixtron SE (NASDAQ: AIXG / Xetra: AIXA)
**What they supply:** MOCVD (metal-organic chemical vapor deposition) production tools — the dominant epitaxy deposition method for volume laser manufacturing. ~70–90% market share in advanced photonic MOCVD; every Coherent/Lumentum InP laser fab runs Aixtron equipment. Also serves GaN, SiC (power), and emerging photonic III-V markets.

**Why forced-spend:**
- Optoelectronics guided to more than double YoY in 2026 (company guidance). AI optical demand explicitly called the primary driver for the optoelectronics segment.
- The NVIDIA $4B+ strategic partnerships with Coherent and Lumentum (announced March 2026) lock in multi-year capex cycles requiring Aixtron tools for any capacity expansion at either prime.
- Veeco (competitor) announced orders for multiple Lumina InP MOCVD tools — confirms industry-wide equipment pull. Aixtron's dominant position means most of that order flow routes to Aixtron.

**Caveats:** At market cap ~$6B+ (pre-run) Aixtron is larger than a micro/small-cap target. **Already re-rated substantially** — from the same source tracking Riber's +451%, Aixtron reportedly ran +334% off trough. The AI optics demand inflection is well-known; AIXG now trades on forward estimates that price in the ramp. This name is borderline "already priced" by the criteria of this hunt.

**6–12m move read:** The bulk of the re-rating has occurred. Can still compound if optoelectronics doubles as guided, but the alpha from being early is gone. Better as a holding/monitoring name than a new entry.

**Accessibility:** Dual-listed NASDAQ (AIXG) and Xetra (AIXA); EUR functional currency; large enough for institutional sizing. No China risk.

---

### 5. POET Technologies (NASDAQ: POET)
**What they supply:** Optical interposer platform — a wafer-level InP-based chip that integrates lasers, modulators, detectors, and passive optics into a single die, enabling chiplets-style assembly for CPO (co-packaged optics) and high-speed optical engines for AI clusters.

**Why forced-spend & small base:**
- Revenue is NRE-stage ($503K in Q1 2026 vs. $167K a year ago) — genuine pre-revenue. Market cap was ~$1.5B as of July 2026, down from a $2.2B peak in May.
- Partnered with QCi (see below) to co-develop 400G/lane TFLN modulator-based 3.2Tbps optical engines; POET funds the modulator development. Target completion H2 2026.
- If the optical interposer model wins a single CPO socket at a hyperscaler (e.g., for Broadcom's Bailly or NVIDIA's Quantum-X), revenue could step from <$1M/quarter to tens of millions — a small-base forcing dynamic.

**Key risks — substantial:**
- **Marvell/Celestial AI blowup (April 2026):** Marvell voided all outstanding POET orders tied to the Celestial AI partnership after POET allegedly violated NDA by disclosing order details publicly. This is a serious commercial execution red flag — the company's largest announced relationship was destroyed by management's own conduct.
- Revenue is essentially zero; market cap of $1.5B implies enormous optionality premium that requires execution POET has not yet demonstrated.
- The Q1 2026 net loss was $12.3M on $503K of revenue.

**6–12m move read:** Red-flag. Already ran to $20+ (52-week high) and collapsed back to ~$8–9. The Marvell incident raises counterparty confidence risk. Avoid or ultra-small speculative position only.

**Accessibility:** NASDAQ-listed, US investors, no China risk.

---

### 6. Quantum Computing Inc. (NASDAQ: QUBT)
**What they supply:** Thin-film lithium niobate (TFLN) photonic chip foundry (Fab 1 in Tempe, AZ; Fab 2 via NHanced Semiconductors acquisition). TFLN enables ultra-high-bandwidth modulators beyond the limits of silicon photonics or InP for 3.2T+ interconnects.

**Why forced-spend & small base:**
- One of only a handful of US-based TFLN fab operators; most others are private (HyperLight) or Chinese (Liobate).
- NIST awarded a TFLN chip contract; multiple commercial orders accumulated through 2025 (five disclosed TFLN chip orders as of late 2025).
- The commercial TFLN modulator market is <$200M today but projected to reach $10B+ by 2033 (23% CAGR). If QUBT captures even 2–3% of a $2B 2028 market that's $40–60M vs. essentially zero revenue today.

**Key risks — very substantial:**
- Capybara Research (short seller, 2025) accused QUBT of issuing misleading press releases and executing sham deals to inflate stock price.
- The TFLN market for AI datacenters doesn't inflect until the 3.2T generation, which volume shipments are unlikely before 2028 per industry analysts.
- The company acquired NHanced for ~$145M (cash + earnout) but Fab 2 commercial revenue runway is speculative.
- Extreme valuation: market cap well above reported revenue run rate by 100x+.

**6–12m move read:** Highly speculative; fraud allegations unresolved; real TFLN revenue inflection is 2028+, not 2026–2027. This is a high-volatility option, not a business-quality holding.

**Accessibility:** NASDAQ-listed. No China risk.

---

### 7. LightPath Technologies (NASDAQ: LPTH)
**What they supply:** Specialty infrared optics, collimating lenses, and optical assemblies — the precision glass/chalcogenide elements used in LiDAR receivers, thermal imaging cameras, and telecom fiber optic assemblies.

**Why forced-spend & small base:**
- TTM revenue ~$37M; market cap ~$900M (as of May 2026 peak, down from prior levels after POET-linked sentiment contagion).
- Secured an $18.2M purchase order for infrared camera systems to a "leading global technology customer" in 2026 — likely an AV or robotics platform.
- LiDAR optical assemblies and IR optics are consumed by every major robotics/AV platform deploying solid-state LiDAR; LightPath's BlackDiamond chalcogenide lens platform is a specialty material that cannot easily be substituted.
- Raised $60M (Dec 2025) and $50M (2026) in equity, building balance sheet to scale capacity.

**Key risks:** Valuation already elevated relative to $37M TTM revenue (market cap/revenue ~24x); thin margins (27.2% gross); still operating at a loss. Stock plunged in April 2026 in sympathy with POET Marvell blowup despite having no relationship — suggests fragile sentiment. Defense/government contract base adds revenue predictability but DoD budget uncertainty.

**6–12m move read:** Partially re-rated but has pulled back from peak. The $18.2M order + AV/robotics IR optics demand is a real forcing function. Revenue doubling from $37M to $75M+ in 2–3 years is plausible if AV volume scales. May be a better entry post-selloff than at the May peak.

**Accessibility:** NASDAQ-listed, US investor, no China risk.

---

### 8. Aeluma (NASDAQ: ALMU)
**What they supply:** Compound semiconductor photodetectors — InGaAs-on-silicon and GaAs-on-silicon wafer-scale detectors for LiDAR (APD/SPAD), 3D sensing, and short-reach optical communications. The key value proposition: manufacturing InGaAs detectors on large-format silicon wafers (6-inch+) using established CMOS fabs, dramatically cutting cost vs. traditional small-format InP substrates.

**Why forced-spend & small base:**
- TTM revenue $4.7M (FY2025 +408% YoY from $919K) — genuine micro-revenue base.
- Six new development engagements in AI datacenter and photonics markets disclosed in 2026; partnerships with Tower Semiconductor and Sumitomo Chemical Advanced Technologies for manufacturing scale-up.
- Every solid-state LiDAR (Ouster, Luminar, Innoviz) requires a photodetector array; if Aeluma's wafer-scale InGaAs approach reaches cost parity with APD arrays, it could displace incumbent detector suppliers across AV, robotics, and satellite ranging.

**Key risks:** Pre-commercial stage; guidance **lowered** for FY2026 (new range $4.2–4.6M, down from $4–6M) due to government contract delays — execution risk confirmed. Market cap ~$345M on $4.7M TTM revenue is a 73x revenue multiple. Customer concentration risk (early stage, few customers). The Silicon Valley CMOS foundry model for compound detectors is compelling in theory but unproven at volume.

**6–12m move read:** Highly speculative. Revenue inflection requires AV/robotics volume adoption that is 2–4 years away. Could easily trade down 50%+ on continued guidance misses. Long-duration call option only.

**Accessibility:** NASDAQ-listed. No China risk.

---

## Ranking Summary

| Rank | Ticker | Name | What They Supply | Small Base & Forced Spend | 6–12m Move | Accessibility |
|------|--------|------|-----------------|--------------------------|------------|---------------|
| 1 | AXTI | AXT Inc. | InP/GaAs single-crystal wafers | $88M rev; InP +250% QoQ; $550M raise at $64; only 2–3 qualified global InP substrate suppliers | Partially ran ($64 offering); further upside tied to InP vol ramp | US-listed; China ops risk on export controls |
| 2 | ALRIB | Riber S.A. | MBE epitaxy production tools (QD lasers, InP) | ~€25M rev microcap; 3x MBE orders in one month for AI optical + QD datacom | May have run +451% already — verify current vs. pre-run | Euronext Paris; thin float; EUR fx |
| 3 | LPTH | LightPath Technologies | IR optics, lenses, optical assemblies | $37M rev; $18.2M PO; chalcogenide specialty material; AV + LiDAR demand | Pulled back from peak; real forcing function intact | US-listed; no China risk |
| 4 | IQEP.L | IQE plc | InP epiwafers (compound semiconductor epitaxy) | Small GBP rev base; June 2026 Tower deal is first AI datacenter win | Modest re-rate post Tower deal; H2 2027 revenue ramp expected | AIM London; thin US liquidity; GBP |
| 5 | AIXG | Aixtron SE | MOCVD production tools | Dominant 70–90% share in photonic MOCVD; AI optics 2x guided | Already re-rated significantly (~+334%) — borderline priced | Dual US/Xetra listed; clean |
| 6 | ALMU | Aeluma | InGaAs/GaAs-on-Si photodetectors (LiDAR/3D sensing) | $4.7M rev; wafer-scale InGaAs novelty; Tower + Sumitomo partnerships | Pre-commercial; guidance cut; 73x revenue valuation | US-listed; no China risk |
| 7 | POET | POET Technologies | Optical interposer (CPO/AI cluster) | <$2M annualized rev; interposer CPO thesis compelling | Ran to $20, now $8–9; Marvell NDA blowup — serious red flag | US-listed; no China risk |
| 8 | QUBT | Quantum Computing | TFLN photonic chip foundry | Essentially zero commercial rev; one of few US TFLN fabs | Fraud allegations unresolved; TFLN volumes not until 2028 | US-listed; avoid near term |

---

## Key Themes Across Names

**1. InP substrate scarcity is the binding constraint** for the 800G → 1.6T transceiver ramp. AXT and IQE are the only two publicly accessible qualified InP substrate/epi suppliers. AXT is the cleaner US-listed play; IQE adds epiwafer differentiation via Tower.

**2. Epitaxy equipment (Aixtron, Riber) has already absorbed most of the re-rating** in the easy-money phase. Riber remains interesting as a quantum-dot MBE specialist in a niche that Aixtron does not dominate — but verify the post-run price carefully.

**3. TFLN modulators are 2028+ volume, not 2026.** QUBT and the POET/QCi collaboration are positioned ahead of the market — positive for long-term optionality, but current valuations reflect speculation on timelines that industry analysts are pushing out.

**4. IR optics / specialty glass (LightPath, LightPath-adjacent) benefit from AV sensor proliferation** more than pure AI datacenter spend. The AV/robotics capex cycle (Waymo, Tesla, Cruise restarts, humanoid robots) is the binding forcing function for this sub-category.

**5. Aeluma's InGaAs-on-silicon thesis is the most differentiated technology** in the detector space — if it works, it could displace incumbent APD arrays across LiDAR. But it is genuinely pre-commercial and the guidance cut suggests schedule slippage.

---

## Coverage Gaps

The following areas were searched but returned insufficient publicly accessible, non-China small-cap names to include as candidates:

1. **Optical isolators (standalone, small-cap):** No commercially shipping small-cap public optical isolator supplier identified. The field is dominated by private companies (Castech, Thorlabs divisions) or internal fab operations at Coherent/Lumentum. TFLN-integrated isolators are at research prototype stage only.

2. **VCSEL chip suppliers (non-Coherent/Lumentum):** Pure-play VCSEL die suppliers are almost entirely private (Vixar, Princeton Optronics, Trumpf Photonic Components) or subsidiaries. The only accessible public VCSEL play is ams OSRAM (SIX: AMS) — a large-cap with VCSEL as a minority revenue line, not a pure-play subcomponent supplier. Tower Semiconductor's InP photonic foundry may evolve into a VCSEL merchant supplier but is mid-cap and partially priced.

3. **Gallium nitride (GaN) substrates for LiDAR pump lasers:** Sumitomo Electric (JP: 5802) and Mitsubishi Chemical (JP: 4188) dominate GaN substrate supply but are diversified large-caps with no meaningful pure-play exposure.

4. **Silicon photonics (SiPh) modulators / grating couplers:** The leading SiPh pure-plays (GlobalFoundries, Intel Foundry, IMEC-related) are either private or large-cap divisions. No accessible small-cap SiPh modulator supplier was identified.

5. **Specialty anti-reflective coating / optical thin-film suppliers:** This segment (companies like Materion, II-VI Optical Coatings) is either private or absorbed into larger entities. No small-cap public pure-play was found.

6. **Japanese compound semiconductor laser epi suppliers (Mitsubishi, Sumitomo Electric laser chips):** Both are large diversified conglomerates; their laser-chip divisions are not separately investable.

7. **Israeli photonics/optical component companies:** No Israel-listed or Israeli-founded small-cap optical subcomponent supplier serving the Coherent/Lumentum/Ouster supply chain was identified in search results — this is a genuine blind spot that warrants targeted follow-up.

---

*Search count: 7 of 7 used.*
