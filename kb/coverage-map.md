# COVERAGE MAP + SOURCING-VECTOR QUEUE
Each fire: hit ≥1 BLIND cell before revisiting COVERED; a dry run MUST pop the next unused vector. Update statuses at run-end.
**THREE TRACKS — pursue every node across W (world-model labs), R (robotics/humanoid), AV (autonomous vehicles). Rotate so all three get coverage; tag a cell with the track(s) covered. A name forced by ≥2 tracks = reinforced demand (note it) but that does NOT override the 4 gates — passing all gates is the only qualifier.**
**Track balance check (updated 2026-07-05, Fire 4):** W-track got its first dedicated sourcing fire this run — came back dry (right theme [Xsens Humanoid mocap], dead equity [delisted OTC shell]; real component suppliers private). R/AV remain the productive tracks. Next fire: continue R/AV harvest (China A-share pre-gate pass, Hota/SOS Lab gate completion) rather than forcing another full W-track sweep — but keep an eye out opportunistically for a public world-model-lab hardware supplier.

## Node × Geography grid — status: COVERED / PARTIAL / BLIND
| Node \ Geo | US | Japan | Korea | Europe | Taiwan | China-listed |
|---|---|---|---|---|---|---|
| Compute/HBM/optical | COVERED(killed:priced) | – | – | PARTIAL | PARTIAL | BLIND |
| Reducers/bearings | COVERED(killed:ran) | COVERED(ran; Hephaist+170% killed) | COVERED(killed:SBBTech+101%; SPG already-known) | PARTIAL | **COVERED(WATCH:Hota 1536.TW; killed:TBI Motion +71.6%)** | **COVERED(killed:headline names +100-490%; 8 second-tier names PRICE-PENDING — see decisions-log Fire 4)** |
| Motors/laminations | PARTIAL | COVERED(killed) | PARTIAL | BLIND | BLIND | PARTIAL(Wolong 600580.SH price-pending, Leadshine 002979.SZ +24.2% causal-check-pending) |
| Force-torque/tactile | PARTIAL(NOVT) | BLIND | BLIND | BLIND | – | PARTIAL(Keli Sensing 603662.SH +10.1% causal-check-pending) |
| Position/encoder ICs | PARTIAL | BLIND | BLIND | COVERED(killed:MLXSF) | BLIND | BLIND |
| Magnets/rare-earth | COVERED(ran) | PARTIAL | BLIND | COVERED(killed:Neo) | – | BLIND |
| LiDAR/optics subcomp | PARTIAL | BLIND | **COVERED(WATCH:SOSLAB)** | BLIND | BLIND | COVERED(WATCH:HSAI — now w/ confirmed Zoox link; RoboSense 2498.HK price-pending) |
| Power components | PARK(understood) | PARTIAL | BLIND | BLIND | BLIND | BLIND |
| Data/mocap/sim (W-track) | **COVERED(dead-end: Movella/Xsens delisted shell)** | BLIND | BLIND | PARTIAL(OMG.L) | – | BLIND |
| AV sensor pods (buyer-BOM) | **COVERED(Waymo=dead end; Zoox→HSAI reinforced)** | – | – | – | – | – |

## Buyer-BOM teardown status (cross-node vector)
- Figure (prior fire): captive/mega-cap dead end.
- Apptronik Apollo: **dead end** — disclosed suppliers are TI/Jabil/NVIDIA/Google (mega-cap); mechanical core (actuators, gearboxes, FT sensors, encoders, batteries) proprietary/undisclosed.
- Agility Digit: **dead end** — explicitly vertically integrated (RoboFab, ~75% US-sourced parts, vendors unnamed); disclosed partners (NVIDIA/Intel/Schaeffler/Foxconn/Google) all mega-cap.
- Waymo 6th-gen Driver (Honeycomb): **dead end** (Fire 4) — same vertically-integrated non-disclosure pattern.
- Zoox robotaxi: **PRODUCTIVE** (Fire 4) — Hesai (HSAI) self-disclosed as LiDAR supplier, $40M+ order; reinforces existing WATCH, not a new name. Teledyne FLIR (thermal cams) also named but now mega-cap-absorbed, excluded.
- UBTECH Walker S2 / Unitree G1-H1-R1: **PRODUCTIVE** (Fire 4) — dense tier-2/3 disclosure via Chinese BOM-teardown press, but most named suppliers already re-rated +100-490%; 8 second-tier names logged price-pending.
- **Lesson (sharpened, Fire 4): the predictor isn't US-vs-China or captive-vs-startup — it's whether the SPECIFIC buyer builds the component in-house (Figure/Apptronik/Agility/Waymo = dead ends) or buys merchant (Zoox, Hyundai MobED, Chinese humanoid OEMs, Tesla Optimus-candidate Hota = productive).**

## Sourcing-vector queue (pop top unused each dry run; recycle when exhausted)
1. ~~EDGAR EFTS "significant customer" + humanoid/AV/robot in 10-Ks~~ — POPPED 2026-07-05, 0 confirmed hits
2. ~~Apptronik Apollo BOM teardown~~ — POPPED, dead end
3. ~~Agility Digit BOM teardown~~ — POPPED, dead end
4. ~~AV sensor-pod BOM teardown (Waymo 6th-gen / Zoox)~~ — POPPED Fire 4: Waymo dead end, Zoox→HSAI productive (reinforcing, not new)
5. ~~Korea KOSDAQ reducer/motor/sensor screen~~ — POPPED, PRODUCTIVE (SOS Lab)
6. ~~Japan JASDAQ/TSE-Standard precision-parts screen~~ — POPPED, mostly dead end
7. ~~Taiwan TWSE/TPEx linear-motion / PCB-for-edge-AI screen~~ — POPPED Fire 4, PRODUCTIVE (Hota Industrial new WATCH; TBI Motion killed already-run; Asia Optical parked)
8. ~~13F KOID minus ROBO/BOTZ sub-$3B residual~~ — POPPED Fire 4: KOID confirmed = KraneShares Global Humanoid Robotics & Physical AI ETF; 2 causal-check-pending leads (Keli Sensing, Leadshine), 1 price-pending (RoboSense), 1 price-conflict (Shuanglin) — see decisions-log
9. Patent assignees CPC B25J/F16H, sub-$500M, 2022–2025
10. Robotics consortium / Automatica-IREX-CES exhibitor lists (partially covered via KyoHA — recheck monthly for new small-cap joiners)
11. ~~China-listed A-share reducer/magnet names~~ — POPPED Fire 4 (via Unitree/UBTECH BOM teardown), PRODUCTIVE but mostly already-run; 8 second-tier names price-pending
12. Design-win/"qualified supplier" PR sweep, precision-motion SIC
13. Data-center liquid-cooling COMPONENT sub-tier (QD couplings, TIM) small-caps
14. Ball-screw / roller-screw sub-tier (legs/linear actuators) — NOTE: TBI Motion (Taiwan) touches this, already-run; check for a non-Taiwan angle
15. Specialty materials: magnet wire, electrical steel, flexspline forgings
16. ~~W-track: world-model data-capture rig hardware~~ — POPPED Fire 4, dead end (right theme [Xsens Humanoid], dead equity [MVLA delisted shell]; real suppliers private [Leopard Imaging])
17. ~~R-track: Chinese humanoid OEM (Unitree/UBTECH) tier-2/3 BOM teardown~~ — POPPED Fire 4, hypothesis CONFIRMED (see #11 above)
18. **NEXT UP — cheap PRICE PRE-GATE pass (Haiku-tier, 2-source) on 8 China A-share second-tier names logged Fire 4:** Green Harmonic 688017.SH, Wolong Electric Drive 600580.SH, Zhucheng Tech 301280.SZ, Xiangxin Tech 002965.SZ, Far East Cable 600869.SH, Siling 301550.SZ, Zhongding 000887.SZ, Jiangsu Leili 300660.SZ — plus reconcile the Shuanglin 300100.SZ price-conflict (2-source rule).
19. **NEXT UP — causal-rigor check** on Keli Sensing Technology 603662.SH + China Leadshine Technology 002979.SZ (index-inclusion only so far, no named design-win yet) and price-check RoboSense 2498.HK.
20. **NEXT UP — Hota Industrial (1536.TW) gate 2 completion:** find a confirmed Tesla Optimus purchase order/contract (not just press-reported capability), plus gate 4 (financials).
21. Korea round 2: DART direct filing pull for SOS Lab's own filing (cross-check the KIS ₩13-18B estimate against primary disclosure); Hwashin Precision Atlas-supplier status (still unconfirmed).
