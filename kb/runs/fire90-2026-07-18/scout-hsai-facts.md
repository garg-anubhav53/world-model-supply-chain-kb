# HSAI (Hesai Group) — Fire 90 Fact-Refresh Scout Notes (2026-07-18)

Pure fact-gathering only, no scoring/verdict (that's the follow-up Opus pass). Compiled from SEC EDGAR primary filings (CIK 1861737), Hesai IR press releases, and 2-source price cross-checks.

---

## 1. Named customers/programs — QUALIFIES vs DOES NOT QUALIFY

### THE SINGLE MOST IMPORTANT FINDING THIS FIRE

Hesai's own FY2025 Q4/full-year earnings release (SEC 6-K, accession 0001104659-26-033591, exhibit 99.1) contains this **verbatim, primary-source definitional sentence** in its "About Hesai" boilerplate:

> "The Company's lidar products enable a broad spectrum of applications including passenger and commercial vehicles ("ADAS"), as well as autonomous driving vehicles and robotics and other non-automotive applications such as last-mile delivery robots and AGVs ("Robotics")."

Read together with the earnings release's own business-highlights bullet list (verbatim, same filing):

> "ranked No.1 in the long-range automotive lidar market, as well as across major robotics submarkets, including: ⬢ Humanoid & quadruped robots (new orders from companies such as Unitree, HONOR Robot, Galbot, Magiclab and Vita Dynamics); ⬢ Robotaxis (new orders from companies such as Pony.ai, WeRide, Baidu Apollo Go, DiDi, and other global players across North America, Asia, and Europe); ⬢ Robovans (new orders from companies such as Zelos, Neolix, and Meituan); ⬢ Robotic lawn mowers (new orders from...)"

**This confirms Hesai itself classifies "Robotaxis" as a sub-segment of its "Robotics" reporting category — grouped with humanoid robots, robovans (delivery), and lawn mowers — NOT as part of its "ADAS" reporting category, which is explicitly defined as "passenger and commercial vehicles" only.**

This directly matters for the Seyond-style audit this fire is running, because it means:
- **Mercedes-Benz L3 is a passenger-vehicle program, not a robotaxi program, and sits in Hesai's own "ADAS" bucket.** Multiple KB entries (Fires 8/13/34/40/59/80/81/87 etc.) and the prior scout note cite "Mercedes-Benz L3" as if it were robotaxi/L3+-grade AV exposure. It is NOT. Mercedes' "Level 3" lidar program (publicly known as DRIVE PILOT-style conditional automation) is a **consumer-owned passenger car feature** sold across "10+ China JV models" / "1M+ units" — individually-purchased vehicles, not a fleet operator, not L4, not robotaxi. Per Hesai's own segment definition this is squarely "ADAS" (passenger vehicle), and per this campaign's explicit exclusion rule it **DOES NOT QUALIFY** — this is the exact same category error the campaign just caught in the Seyond downgrade (counting mainstream passenger-vehicle driver-assist as "AV exposure").
- The prior scout's claim of "8 of top-10 robotaxi developers incl. Zoox, Mercedes-Benz L3, Motional" **conflates two genuinely different buckets**: Zoox/Motional/Pony.ai/WeRide/Baidu Apollo Go/DiDi are correctly robotaxi (verified — see below); Mercedes-Benz L3 is not and should never have been listed alongside them as "robotaxi/L3+-grade."

### QUALIFIES (robotaxi fleet operator / L4+ autonomy developer / humanoid-embodied-AI OEM)

All of these are drawn from primary-source Hesai 6-Ks (FY2025 Q4 release, Q1 2026 release) and are explicitly listed by Hesai itself under its "Robotics" segment / "Robotaxis" or "Humanoid & quadruped robots" sub-categories, i.e. Hesai's own reporting agrees these are NOT ADAS:

- **Zoox** (Amazon-owned robotaxi) — confirmed via Hesai's own 6-K/press ("Announcing Our Partnership with Zoox," ~Jul 2025) and a follow-on **$40M+ lidar order**, delivery through end of 2026. QUALIFIES — robotaxi fleet operator.
- **Motional** (Hyundai/Aptiv robotaxi JV) — exclusive short-range lidar supplier on the IONIQ 5 robotaxi (Gasgoo, corroborated across multiple fires). QUALIFIES — robotaxi fleet operator.
- **Pony.ai** — named main-lidar supplier for its robotaxi fleet (4x AT128 units/vehicle on 7th-gen robotaxi per Fire 20 disclosure-mining). QUALIFIES.
- **WeRide** — named robotaxi lidar supplier (strategic cooperation since 2021/2022). QUALIFIES.
- **Baidu Apollo Go** — named main-lidar supplier, ~$300M-potential 6th-gen RT6 deal + Dubai 1,000+ vehicle deployment (per Fire 20 disclosure-mining, unverified as to whether the $300M figure is still current). QUALIFIES.
- **DiDi** — named robotaxi customer in Hesai's own Q4 2025 release bullet list. QUALIFIES.
- **Unitree, HONOR Robot ("Lightning"), Galbot, Magiclab, Vita Dynamics** — named humanoid/quadruped robot makers, explicitly listed by Hesai in its own Q4 2025 release under "Humanoid & quadruped robots." Notably, **Unitree is separately also listed by Hesai as an "ADAS" design-win name** in the same release ("Selected by Unitree to equip JT128 lidar in all of its humanoid robots" — this is unambiguously humanoid, JT128 is Hesai's robotics-line product) — confirms these are genuine embodied-AI/humanoid buyers. QUALIFIES.
- **Zelos, Neolix, Meituan** — named "Robovans" (autonomous delivery vehicle) customers in the same Q4 2025 bullet list. **Borderline/judgment call for Opus**: these are L4 autonomous ground-vehicle fleets (delivery robots/robovans), arguably within an "AV-fleet/L4+" reading of the thesis, but they are not passenger robotaxis and not humanoid — flagging as a gray-zone category rather than asserting a verdict.
- **Aurora Innovation** (L4 autonomous trucking) — appears in the KB's historical "8-of-top-10 robotaxi developers" list and in general search results as a Hesai customer, but **this fire found a red flag**: Aurora's own 2026 disclosures describe it developing and deploying **proprietary in-house "FirstLight" lidar** (2nd-gen hardware kit, mid-2026, extending range to 1,000m) for its commercial driverless-truck fleet. This raises real doubt about whether Hesai still has an active/material supply position with Aurora as of mid-2026 — **flag as UNVERIFIED CURRENT STATUS, do not carry forward as a confirmed current qualifying buyer without a fresher primary-source check.**

### DOES NOT QUALIFY (passenger-vehicle L2/L3 driver-assist, regardless of Hesai's marketing language)

- **Mercedes-Benz (L3 lidar partnership)** — see above. Passenger-vehicle OEM program, "ADAS" per Hesai's own segment definition. DOES NOT QUALIFY.
- **Li Auto** — exclusive multi-lidar design win, standard on all new models since May 2025, "start of production planned for 2026-2027," "3 to 6 lidars per vehicle" — this is a Chinese passenger-EV OEM's consumer ADAS program. DOES NOT QUALIFY.
- **Xiaomi** — multi-lidar design win, same passenger-EV ADAS bucket. DOES NOT QUALIFY.
- **Changan** — multi-lidar design win, same passenger-EV ADAS bucket. DOES NOT QUALIFY.
- **Great Wall Motor, GAC Toyota bZ3X, Toyota, BAIC, FAW Bestune** — all named in the KB/press as passenger-vehicle OEM ADAS design wins across "40 automotive brands globally across over 160 vehicle models, including all top ten OEMs in China" per Hesai's own Q4 2025 release. DOES NOT QUALIFY (mainstream consumer ADAS).
- **Cadillac VISTIQ** (in-cabin lidar), **NIU** (electric two-wheeler) — consumer-vehicle applications, unrelated to AV-fleet/robotaxi/humanoid thesis. DOES NOT QUALIFY.
- **NVIDIA DRIVE Hyperion 10** — Hesai is the named "primary/default turnkey lidar partner" for this AV-development platform. This is a **channel/platform relationship, not a single buyer** — Hyperion 10 is licensed to a broad mix of OEMs spanning both consumer L2/L3 ADAS programs and genuine robotaxi/L4 developers. Cannot be cleanly counted as qualifying revenue; treat as **mixed/enabling exposure**, not a clean qualifying buyer.
- **Dreame, MOVA** (robotic lawn mowers), **Exyn Technologies** (drone/mining SLAM, ~15% of its lidar supply per its own 10-Q) — non-automotive robotics/industrial, outside both the passenger-ADAS and the robotaxi/humanoid qualifying buckets. Non-qualifying under the campaign's specific robotaxi/AV-fleet/humanoid-embodied-AI thesis (these are neither).

---

## 2. Estimated % of revenue: QUALIFYING vs NON-QUALIFYING

**Hesai does NOT disclose a revenue-dollar or percentage breakdown by application/segment in its public filings — only unit-shipment counts, split into two buckets ("ADAS" and "Robotics") that do not line up cleanly with this campaign's qualifying/non-qualifying test.** This is the load-bearing caveat for the Opus follow-up.

**FY2025 unit shipments (Hesai 6-K, Q4/FY2025 release, primary source):**
| Segment (Hesai's own label) | FY2025 units | % of total units | What's inside it |
|---|---|---|---|
| ADAS | 1,381,133 | 85.2% | Passenger + commercial vehicle driver-assist ONLY (Li Auto, Xiaomi, Changan, Mercedes-Benz L3, Great Wall, Toyota, etc.) — **100% NON-QUALIFYING** under this campaign's thesis |
| Robotics | 239,273 | 14.8% | Robotaxis (Pony.ai/WeRide/Baidu/DiDi/Motional/Zoox) + Humanoid/quadruped robots (Unitree/Galbot/Magiclab/Vita Dynamics/HONOR) + Robovans (Zelos/Neolix/Meituan) + robotic lawn mowers (Dreame/MOVA) + AGVs/industrial — **MIXED: only a sub-fraction qualifies** |
| Total | 1,620,406 | 100% | |

**Derived estimate (my own back-of-envelope, NOT a disclosed figure — flag explicitly as an estimate):**
- The 85.2%-of-units "ADAS" bucket is unambiguously non-qualifying and, per Hesai's own commentary that "ADAS lidars... typically carry a lower gross margin than Robotics lidars," most likely represents an even LARGER share of revenue than of units (ASP/mix effects push revenue concentration toward ADAS, not away from it) — plausibly **80-90%+ of total company revenue is non-qualifying passenger-vehicle ADAS.**
- The remaining ~10-20% of revenue (the "Robotics" bucket) is itself split, undisclosed, among robotaxi + humanoid (genuinely qualifying) vs. lawn mowers/AGVs/delivery robots/industrial (does not qualify under a strict robotaxi/L4-fleet/humanoid reading). Historical KB notes reference very large humanoid/consumer-robotics unit deals (e.g., a "300k-unit/12-month smart-home robotics deal," a "10M+ unit backlog") that are NOT humanoid or robotaxi — this suggests the qualifying slice within the already-small Robotics bucket may be a minority of that bucket too.
- **Best-effort estimate: genuinely qualifying (robotaxi + humanoid) revenue is very likely a SINGLE-DIGIT-TO-LOW-TEENS percentage of Hesai's total revenue** — this is a rough, unverified estimate flagged explicitly for Opus to sanity-check or refine, not a company-disclosed number. No primary source gives an exact split; this scout could not find one despite searching the 20-F, Q4 2025 and Q1 2026 earnings releases, and the Q1 2026 earnings-call transcript.
- **Sources checked and found NOT to contain a dollar/percentage split:** Hesai FY2025 20-F (sec.gov/Archives/edgar/data/0001861737/000110465926048025/hsai-20251231x20f.htm) — no application-level revenue table found in the accessible sections; Q4/FY2025 earnings release (accession 0001104659-26-033591) — units only, no revenue $ by segment; Q1 2026 earnings-call transcript (multiple aggregator sources) — qualitative commentary only ("backlog exceeding 6 million units," "significant new design wins in both automotive and robotics"), no revenue split disclosed.
- Customer concentration disclosed in the 20-F per prior KB fires (Fire 29, not independently re-verified this fire due to time-box): top-5 customers = 55.8% of FY2025 revenue (down from 59.9% FY24, 67.5% FY23) — but the 20-F does not name which customers are in the top 5, so this concentration figure cannot itself be mapped to qualifying vs non-qualifying.

**Bottom-line for Opus:** Treat the "8 of top-10 robotaxi developers" and "Mercedes-Benz L3" framing as NOT equivalent — the robotaxi names are genuinely qualifying but represent a small slice of a small (14.8%-of-units) segment; Mercedes-Benz L3 and the broader ADAS book (85.2% of units, likely a similar-or-larger share of revenue) is ordinary passenger-vehicle driver-assist and should be treated the same way the Seyond audit treated NIO/Onvo/SAIC-VW/GAC — i.e., excluded from "AV thesis exposure."

---

## 3. Current stock price and market cap (2-source cross-check, ADS count used explicitly)

**Standing KB trap reminder (confirmed still relevant): Hesai's outstanding ORDINARY share count is ~1,257,137,688 (post 8-for-1 subdivision), but the ADS ratio was simultaneously changed 1:1 → 1:8, so the actual tradeable Nasdaq ADS count is UNCHANGED at ~156-157M. Market cap MUST be computed as ADS price × ~156.44M ADS, never × the 1.257B ordinary-share count (that produces a false ~8x-inflated figure).**

- **Source 1 — stockanalysis.com (2026-07-17 close, 4:00pm EDT):** price **$15.00** (−4.15% that day), shares outstanding **156.44 million** (ADS-equivalent), market cap **$2.35 billion**. After-hours $15.15 (+1.00%).
- **Source 2 — Google Finance (as of 2026-07-17, 7:59pm GMT-4):** price **$15.00**, market cap displayed as **$2.42 billion** (after-hours $15.03).

**Manual verification: 156.44M ADS × $15.00 = $2.347B ≈ $2.35B** — matches stockanalysis.com almost exactly. Google Finance's $2.42B is ~3% higher (likely a slightly different/stale share-count denominator, ~161M implied), but both sources are in the same ~$2.3-2.4B order of magnitude, and **neither shows anything close to the false ~$18.9B figure** that the 1.257B ordinary-share count × $15.00 would produce. **8x trap correctly avoided; ADS count of ~156.44M used as the basis, consistent with the KB's standing rule.**

Stock is down from the $18.22 print on 2026-07-01, near its 52-week-low territory (consistent with prior fires' framing).

---

## 4. D.C. Circuit case No. 25-5256 status

**Still UNRESOLVED — no ruling has been issued as of 2026-07-18.**

- Oral argument was held **March 18-19, 2026**, before Judges Pillard, Garcia, and Edwards (per CourtListener/Justia docket metadata and Law360 coverage). This fire's check is thus almost exactly **4 months post-argument**.
- Law360 ("Judges Scrutinize DOD's Claim Of Hesai's China Military Ties") confirms the panel pressed DoD's counsel skeptically on the evidentiary basis for the "military-civil fusion enterprise zone" theory — a favorable tone, not a ruling.
- December 2025: the court declined to formally coordinate the Hesai and DJI (also 1260H-designated) parallel appeals — the last confirmed procedural docket movement found this fire.
- Direct attempts to pull the live CourtListener/Justia docket page and the CADC "recent opinions" feed both hit access errors this fire (403s) rather than confirming content directly, but **multiple independent news/search sweeps (WebSearch across Law360, tradelawdaily, exportcompliancedaily, general news) found no report of any ruling, opinion, judgment, or mandate having issued** — consistent with, not contradicting, the "no ruling yet" status the KB has carried since Fire 8.
- Background (unchanged): the D.C. District Court upheld the DoD's 1260H "Chinese Military Company" designation on July 11, 2025, on a "military-civil fusion enterprise zone" geography theory, explicitly WITHOUT finding actual military use of Hesai's products or a direct/indirect PLA connection.

**No change from the prior fire's finding — case remains binary/pending.**

---

## 5. Aug-28-2026 EGM status

**Confirmed via primary source (SEC 6-K, accession 0001104659-26-081573, filed 2026-07-08, exhibit 99.1): record date confirmed, but the agenda/circular is explicitly NOT yet published.**

Verbatim quotes from the primary-source press release:
> "The record date for the purpose of determining the eligibility of the holders of the Class A ordinary shares and/or Class B ordinary shares of the Company... to vote and attend the forthcoming EGM will be as of the close of business on Thursday, July 23, 2026, Hong Kong time."

> "The 2026 second extraordinary general meeting (the 'EGM') of Hesai Group... is proposed to be convened and held on Friday, August 28, 2026, Hong Kong time."

> "Further details, including the meeting date and location of the EGM, will be set out in the circular and the notice of such meeting to be issued by the Company in due course."

**No agenda/purpose is disclosed in this announcement.** A direct pull of Hesai's full EDGAR 6-K filing list (CIK 1861737) shows the most recent filings are dated **2026-07-10** (two filings, both confirming execution of the 8-for-1 subdivision/ADS-ratio change from the June-26 AGM) and **2026-07-08** (the EGM record-date notice quoted above). **No 6-K has been filed since 2026-07-10 — the EGM circular has NOT been published as of 2026-07-18 (today).**

Context (per the standing KB framing, not independently re-derived this fire): this is Hesai's *second* 2026 EGM. The March-3 EGM and June-26 AGM already executed the split/ADS-ratio change and standing share-issuance mandates, which somewhat lowers (does not eliminate) the odds this follow-on meeting carries a fresh dilutive/hostile item — but this remains unconfirmed until the circular actually posts. Record date (2026-07-23) is 5 days out from this fire's check date.

---

## Sources (all fetched/verified this fire, 2026-07-18)

- Hesai Group FY2025 Q4/full-year earnings release, SEC Form 6-K exhibit 99.1, accession 0001104659-26-033591 (sec.gov/Archives/edgar/data/1861737/000110465926033591/tm269592d1_ex99-1.htm) — fetched raw HTML directly via curl and parsed for verbatim quotes (segment definitions, named customers, unit shipments).
- Hesai Group FY2025 Form 20-F, sec.gov/Archives/edgar/data/0001861737/000110465926048025/hsai-20251231x20f.htm — reviewed via WebFetch (no application-level revenue $ breakdown or named customers found in accessible sections).
- SEC EDGAR 6-K filing list, CIK 1861737 (atom feed, sec.gov/cgi-bin/browse-edgar?action=getcompany&CIK=0001861737&type=6-K) — pulled directly to confirm no filing after 2026-07-10.
- SEC Form 6-K, EGM record-date notice, accession 0001104659-26-081573, exhibit 99.1 (sec.gov/Archives/edgar/data/1861737/000110465926081573/tm2620039d1_ex99-1.htm) — fetched directly, verbatim quotes above.
- stockanalysis.com/stocks/hsai/ — price/mkt cap/shares outstanding, 2026-07-17 close.
- Google Finance (google.com/finance/beta/quote/HSAI:NASDAQ) — price/mkt cap cross-check, 2026-07-17.
- Law360, "Judges Scrutinize DOD's Claim Of Hesai's China Military Ties" (law360.com/articles/2455251).
- Justia docket listing for D.C. Cir. 25-5256 (dockets.justia.com/docket/circuit-courts/cadc/25-5256) — metadata only, direct content fetch 403'd; corroborated via WebSearch news sweep.
- tradelawdaily.com (Dec-2025 non-coordination order); exportcompliancedaily.com (July-2025 district-court designation upholding).
- Q1 2026 earnings-call transcript aggregation (Investing.com, Yahoo Finance, Motley Fool, gurufocus.com — gurufocus direct fetch 403'd, used via search-result synthesis only).
- Aurora Innovation FirstLight in-house lidar disclosure (via WebSearch, act-news.com/fifthlevelconsulting.com aggregation) — flagged as a reason to doubt Aurora's current-status as an active Hesai customer.
