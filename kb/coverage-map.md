# COVERAGE MAP + SOURCING-VECTOR QUEUE
Each fire: hit ≥1 BLIND cell before revisiting COVERED; a dry run MUST pop the next unused vector. Update statuses at run-end.
**THREE TRACKS — pursue every node across W (world-model labs), R (robotics/humanoid), AV (autonomous vehicles). Rotate so all three get coverage; tag a cell with the track(s) covered. A name forced by ≥2 tracks = reinforced demand (note it) but that does NOT override the 4 gates — passing all gates is the only qualifier.**
**Track balance check (updated 2026-07-06, Fire 6):** R got the most coverage again (Jiangsu Leili promoted, Shuanglin/Neuromeka gate checks, USPTO patent sweep on 3 US names). AV got one check (Valeo size-gate, killed). **W-track finally got a genuine hit** — Orbbec/Robbyant is the first real world-model forced-buyer link found across 6 fires, opening a new W+R cross-track vector (Orbbec's own upstream suppliers). Next fire: prioritize the Orbbec-upstream and Robbyant-ecosystem-partner vectors (queue #26-27) to keep W-track momentum, alongside routine Hota/Leili monitoring.

## Node × Geography grid — status: COVERED / PARTIAL / BLIND
| Node \ Geo | US | Japan | Korea | Europe | Taiwan | China-listed |
|---|---|---|---|---|---|---|
| Compute/HBM/optical | COVERED(killed:priced) | – | – | PARTIAL | PARTIAL | BLIND |
| Reducers/bearings | COVERED(killed:ran) | COVERED(ran; Hephaist+170% killed) | COVERED(killed:SBBTech+101%; SPG already-known) | PARTIAL | **COVERED(WATCH:Hota 1536.TW — fraying, gate 2 still unconfirmed 4 fires running; killed:TBI Motion +71.6%)** | **COVERED & EXHAUSTED(2nd-tier pre-gate complete: 8 killed [incl. Shuanglin Fire 6], 1 promoted to WATCH [Jiangsu Leili 300660.SZ, Fire 6 — named buyers Zhiyuan/AgiBot+Wellblue] — see decisions-log Fire 6)** |
| Motors/laminations | PARTIAL | COVERED(killed) | PARTIAL | BLIND | BLIND | **COVERED(Wolong killed:size+already-run; Leadshine killed:no-named-buyer)** |
| Force-torque/tactile | PARTIAL(NOVT) | BLIND | BLIND | – | – | **COVERED(WATCH:Keli Sensing — named Huawei buyer, see kb/companies/KELI.md)** |
| Position/encoder ICs | PARTIAL | BLIND | BLIND | COVERED(killed:MLXSF) | BLIND | BLIND |
| Magnets/rare-earth | COVERED(ran) | PARTIAL | BLIND | COVERED(killed:Neo) | – | BLIND |
| LiDAR/optics subcomp | PARTIAL | BLIND | **COVERED(WATCH:SOSLAB)** | PARTIAL(Valeo named but likely size-gate fail — pending check) | BLIND | **COVERED(WATCH:HSAI — now w/ 4/5-buyer confirmed reinforcement; RoboSense reinforced 2/5, context only)** |
| Power components | PARK(understood) | PARTIAL | BLIND | BLIND | BLIND | BLIND |
| Data/mocap/sim (W-track) | **COVERED(dead-end: Movella/Xsens delisted shell)** | BLIND | BLIND | PARTIAL(OMG.L) | – | **PARTIAL(Orbbec/Robbyant productive causal link, Fire 6 — Orbbec itself killed on re-rating, upstream image-sensor/ToF-chip tier UNTESTED)** |
| AV sensor pods (buyer-BOM) | **COVERED(Waymo=dead end; Zoox→HSAI reinforced)** | – | – | – | – | **COVERED(Pony.ai/WeRide/Baidu Apollo Go/Didi all → Hesai/RoboSense reinforced, no new tickers; Momenta→Valeo pending size-gate)** |
| Patent-assignee (CPC B25J/F16H) | **COVERED(Servotronics killed:delisted: Allied Motion/ALNT killed:already-run+wrong-CPC; NN Inc killed:no-patent-fit)** | PARTIAL(Nitta deprioritized:stale filings) | **COVERED(Neuromeka killed:vertical-integration, gate 2 fails)** | – | PARTIAL(Tung Pei parked:tradability unconfirmed) | PARTIAL(Estun/Guomao killed:size) |

## Buyer-BOM teardown status (cross-node vector)
- Figure / Apptronik / Agility / Waymo: **dead ends** — all vertically integrate.
- Zoox robotaxi: **PRODUCTIVE** — Hesai (HSAI) self-disclosed LiDAR supplier, $40M+ order; reinforces existing WATCH.
- UBTECH Walker S2 / Unitree G1-H1-R1: **PRODUCTIVE but now EXHAUSTED** — dense tier-2/3 disclosure fully priced this fire (7 of 9 fresh names killed already-run/size-gated; 2 pending pre-revenue).
- **NEW (Fire 5) Chinese robotaxi multi-buyer BOM (Pony.ai, WeRide, Baidu Apollo Go, Momenta, AutoX, Didi):** PRODUCTIVE for reinforcement, not new names — Hesai confirmed at 4/5 buyers, RoboSense at 2/5. AutoX/SiLC/ZVision confirmed dead ends (private, no ticker). Momenta→Valeo the one fresh named design-win, pending a size-gate check.
- **Lesson (sharpened, Fire 5): once a buyer-BOM vector is productive, it saturates fast — the FIRST few buyers surface the dominant merchant supplier(s), and subsequent buyers mostly reinforce rather than diversify. Don't over-invest in exhaustively re-running the same buyer-BOM method on adjacent buyers once 2-3 have confirmed the same supplier; rotate to a different sourcing METHOD (patent-assignee, consortium, design-win PR) instead.**
- **NEW (Fire 6) Ant Group "Robbyant" embodied-AI world-model BOM:** PRODUCTIVE, first W-track hit — Orbbec (688322.SH) confirmed depth-sensor vendor into Robbyant's "LingBot-Depth" world-model + named humanoid buyers X-Humanoid/AgiBot/UBTech. Orbbec itself killed (already-run, revenue-mix) but its own upstream (image-sensor/ToF-chip suppliers) is untested — see coverage-map queue #26.

## Sourcing-vector queue (pop top unused each dry run; recycle when exhausted)
1-8. ~~(EDGAR, Apptronik, Agility, AV sensor-pod BOM, Korea screen, Japan screen, Taiwan screen, 13F KOID residual)~~ — all POPPED prior fires, see decisions-log.
9. ~~Patent assignees CPC B25J/F16H, sub-$500M, 2022–2025~~ — **POPPED Fire 5: MODERATE yield.** 1 pending (Neuromeka), 1 parked (Tung Pei — tradability unconfirmed), 1 needs-retry (Servotronics — use direct USPTO assignee-field search, not general web search, next pass). Worth ONE more focused pass on US small-caps (Allied Motion/Allient, NN Inc) via USPTO Patent Public Search directly.
10. Robotics consortium / Automatica-IREX-CES exhibitor lists (partially covered via KyoHA — recheck monthly for new small-cap joiners) — still open, low cadence.
11. ~~China-listed A-share reducer/magnet names~~ — POPPED Fire 4, price-gate COMPLETED Fire 5 (see #18 below, now EXHAUSTED).
12. Design-win/"qualified supplier" PR sweep, precision-motion SIC — still UNTESTED, next priority new vector.
13. Data-center liquid-cooling COMPONENT sub-tier (QD couplings, TIM) small-caps — still open, low priority (parked corner).
14. Ball-screw/roller-screw sub-tier — TBI Motion (Taiwan) already-run; Shuanglin (China) now pending gate-1, not a fresh angle needed.
15. Specialty materials: magnet wire, electrical steel, flexspline forgings — still open.
16. ~~W-track: world-model data-capture rig hardware~~ — POPPED Fire 4, dead end.
17. ~~R-track: Chinese humanoid OEM (Unitree/UBTECH) tier-2/3 BOM teardown~~ — POPPED Fire 4, price-gated Fire 5, EXHAUSTED.
18. ~~China A-share 2nd-tier price pre-gate (12 names)~~ — **POPPED & COMPLETED Fire 5**: 7 KILL, 2 PENDING (Jiangsu Leili, Shuanglin). Vector exhausted.
19. ~~Causal-rigor check Keli Sensing + Leadshine~~ — **POPPED & COMPLETED Fire 5**: Keli WATCH, Leadshine KILL.
20. ~~Hota Industrial gate 2+4 completion~~ — **POPPED & COMPLETED Fire 5**: HOLD at WATCH, fraying — see pipeline.md.
21. Korea round 2: DART direct filing pull for SOS Lab's own filing; Hwashin Precision Atlas-supplier status (still unconfirmed) — still open.
22. ~~gate-1 (named buyer) check on Jiangsu Leili (300660.SZ) + Shuanglin (300100.SZ)~~ — **POPPED & COMPLETED Fire 6: Jiangsu Leili PROMOTED TO WATCH** (named buyers Zhiyuan Robotics/AgiBot + Wellblue, "stable orders" per Oct 2025 IR filing, price -5.7%/-6.0%/12m — not re-rated). **Shuanglin KILL** (still "not yet designated" per own FY25/Q1'26 filings + weakening fundamentals).
23. ~~Valeo size-gate check~~ — **POPPED & COMPLETED Fire 6: KILL, confirmed** (LiDAR/"Brain" division ~23.9% of €20.9B total, below 30% threshold).
24. ~~direct USPTO Patent Public Search (assignee-name field) for Servotronics/Allied Motion/NN Inc~~ — **POPPED & COMPLETED Fire 6: all 3 KILL** (SVT delisted; ALNT wrong CPC + already-run +125%; NNBR no patent fit). Vector CLOSED for these three names.
25. ~~Neuromeka (348340.KQ) 2-source price reconfirm~~ — **POPPED & COMPLETED Fire 6: KILL** (price +39.5%/+46.1%, under already-run bar, but fails gate 2 — vertically-integrated own-brand humanoid maker, no external buyer).
26. **NEW (Fire 6) — Orbbec (688322.SH) upstream supply chain**: chase Orbbec's own image-sensor/ToF-chip suppliers (the component Orbbec itself is forced to buy) — Orbbec is a confirmed named vendor into Ant Group's Robbyant "LingBot-Depth" world-model plus X-Humanoid/AgiBot/UBTech, so its own upstream tier inherits the same forced-demand logic one level removed. First W-track-productive vector in KB history — HIGH PRIORITY next fire.
27. **NEW (Fire 6) — Robbyant/Ant-Group embodied-AI ecosystem partner mining**: identify OTHER named hardware vendors into Robbyant beyond Orbbec (analogous to the Huawei 16-partner list in T10) — untested.
28. **NEW (Fire 6) — Jiangsu Leili robotics-revenue disclosure trigger**: check the FY2025 annual report (due ~April 2026) for a broken-out robotics-segment revenue % — currently qualitative "small-batch shipment" only.
