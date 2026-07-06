# COVERAGE MAP + SOURCING-VECTOR QUEUE
Each fire: hit ≥1 BLIND cell before revisiting COVERED; a dry run MUST pop the next unused vector. Update statuses at run-end.
**THREE TRACKS — pursue every node across W (world-model labs), R (robotics/humanoid), AV (autonomous vehicles). Rotate so all three get coverage; tag a cell with the track(s) covered. A name forced by ≥2 tracks = reinforced demand (note it) but that does NOT override the 4 gates — passing all gates is the only qualifier.**
**Track balance check (updated 2026-07-06, Fire 5):** R and AV both got heavy coverage this fire (China 2nd-tier reducer/motor/sensor pre-gate, Keli Sensing gate-1, Hota gate completion, patent sweep = R; Chinese robotaxi BOM reinforcement = AV). W-track untouched this fire (by design — stays opportunistic per Fire 4 finding). Next fire: continue closing the pending list (Jiangsu Leili/Shuanglin/Neuromeka/Valeo gate-1 checks) before opening a brand-new vector — cheaper than fresh discovery.

## Node × Geography grid — status: COVERED / PARTIAL / BLIND
| Node \ Geo | US | Japan | Korea | Europe | Taiwan | China-listed |
|---|---|---|---|---|---|---|
| Compute/HBM/optical | COVERED(killed:priced) | – | – | PARTIAL | PARTIAL | BLIND |
| Reducers/bearings | COVERED(killed:ran) | COVERED(ran; Hephaist+170% killed) | COVERED(killed:SBBTech+101%; SPG already-known) | PARTIAL | **COVERED(WATCH:Hota 1536.TW — fraying, gate 2 still unconfirmed 4 fires running; killed:TBI Motion +71.6%)** | **COVERED & EXHAUSTED(2nd-tier pre-gate complete: 7 killed, 2 pending [Jiangsu Leili, Shuanglin] — see decisions-log Fire 5)** |
| Motors/laminations | PARTIAL | COVERED(killed) | PARTIAL | BLIND | BLIND | **COVERED(Wolong killed:size+already-run; Leadshine killed:no-named-buyer)** |
| Force-torque/tactile | PARTIAL(NOVT) | BLIND | BLIND | – | – | **COVERED(WATCH:Keli Sensing — named Huawei buyer, see kb/companies/KELI.md)** |
| Position/encoder ICs | PARTIAL | BLIND | BLIND | COVERED(killed:MLXSF) | BLIND | BLIND |
| Magnets/rare-earth | COVERED(ran) | PARTIAL | BLIND | COVERED(killed:Neo) | – | BLIND |
| LiDAR/optics subcomp | PARTIAL | BLIND | **COVERED(WATCH:SOSLAB)** | PARTIAL(Valeo named but likely size-gate fail — pending check) | BLIND | **COVERED(WATCH:HSAI — now w/ 4/5-buyer confirmed reinforcement; RoboSense reinforced 2/5, context only)** |
| Power components | PARK(understood) | PARTIAL | BLIND | BLIND | BLIND | BLIND |
| Data/mocap/sim (W-track) | **COVERED(dead-end: Movella/Xsens delisted shell)** | BLIND | BLIND | PARTIAL(OMG.L) | – | BLIND |
| AV sensor pods (buyer-BOM) | **COVERED(Waymo=dead end; Zoox→HSAI reinforced)** | – | – | – | – | **COVERED(Pony.ai/WeRide/Baidu Apollo Go/Didi all → Hesai/RoboSense reinforced, no new tickers; Momenta→Valeo pending size-gate)** |
| Patent-assignee (CPC B25J/F16H) | PARTIAL(Servotronics needs-retry, CTS killed:size) | PARTIAL(Nitta deprioritized:stale filings) | **PARTIAL(Neuromeka pending gate-1)** | – | PARTIAL(Tung Pei parked:tradability unconfirmed) | PARTIAL(Estun/Guomao killed:size) |

## Buyer-BOM teardown status (cross-node vector)
- Figure / Apptronik / Agility / Waymo: **dead ends** — all vertically integrate.
- Zoox robotaxi: **PRODUCTIVE** — Hesai (HSAI) self-disclosed LiDAR supplier, $40M+ order; reinforces existing WATCH.
- UBTECH Walker S2 / Unitree G1-H1-R1: **PRODUCTIVE but now EXHAUSTED** — dense tier-2/3 disclosure fully priced this fire (7 of 9 fresh names killed already-run/size-gated; 2 pending pre-revenue).
- **NEW (Fire 5) Chinese robotaxi multi-buyer BOM (Pony.ai, WeRide, Baidu Apollo Go, Momenta, AutoX, Didi):** PRODUCTIVE for reinforcement, not new names — Hesai confirmed at 4/5 buyers, RoboSense at 2/5. AutoX/SiLC/ZVision confirmed dead ends (private, no ticker). Momenta→Valeo the one fresh named design-win, pending a size-gate check.
- **Lesson (sharpened, Fire 5): once a buyer-BOM vector is productive, it saturates fast — the FIRST few buyers surface the dominant merchant supplier(s), and subsequent buyers mostly reinforce rather than diversify. Don't over-invest in exhaustively re-running the same buyer-BOM method on adjacent buyers once 2-3 have confirmed the same supplier; rotate to a different sourcing METHOD (patent-assignee, consortium, design-win PR) instead.**

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
22. **NEXT UP — gate-1 (named buyer) check on Jiangsu Leili (300660.SZ) + Shuanglin (300100.SZ)** — the two mechanical survivors of the now-exhausted China 2nd-tier vector; cheapest remaining path to a promotion since they're already priced.
23. **NEXT UP — Valeo size-gate check** (LiDAR/SCALA segment revenue as % of ~€20B total revenue) — likely kill but needs an explicit number before dropping.
24. **NEXT UP — direct USPTO Patent Public Search (assignee-name field)** for Servotronics (SVT), Allied Motion/Allient, NN Inc — general web search under-indexes assignee metadata.
25. **NEXT UP — Neuromeka (348340.KQ) 2-source price reconfirm** — may already exceed +60% re-rating threshold; verify before spending more budget on gate-1.
