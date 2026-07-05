# COVERAGE MAP + SOURCING-VECTOR QUEUE
Each fire: hit ≥1 BLIND cell before revisiting COVERED; a dry run MUST pop the next unused vector. Update statuses at run-end.
**THREE TRACKS — pursue every node across W (world-model labs), R (robotics/humanoid), AV (autonomous vehicles). Rotate so all three get coverage; tag a cell with the track(s) covered. A name forced by ≥2 tracks = reinforced demand (note it) but that does NOT override the 4 gates — passing all gates is the only qualifier.**
**Track balance check (updated 2026-07-05):** last 2 fires have been R/AV-heavy (humanoid BOM teardowns, Korea/Japan robotics screens, HSAI). **W track is under-covered — next fire should prioritize W-track sourcing** (world-model data-capture rigs, synthetic-data infra, egocentric-video hardware, training-cluster tier-2/3 suppliers).

## Node × Geography grid — status: COVERED / PARTIAL / BLIND
| Node \ Geo | US | Japan | Korea | Europe | Taiwan | China-listed |
|---|---|---|---|---|---|---|
| Compute/HBM/optical | COVERED(killed:priced) | – | – | PARTIAL | PARTIAL | BLIND |
| Reducers/bearings | COVERED(killed:ran) | COVERED(ran; Hephaist+170% killed) | COVERED(killed:SBBTech+101%; SPG already-known) | PARTIAL | PARTIAL(ran) | BLIND |
| Motors/laminations | PARTIAL | COVERED(killed) | PARTIAL | BLIND | BLIND | BLIND |
| Force-torque/tactile | PARTIAL(NOVT) | BLIND | BLIND | BLIND | – | BLIND |
| Position/encoder ICs | PARTIAL | BLIND | BLIND | COVERED(killed:MLXSF) | BLIND | BLIND |
| Magnets/rare-earth | COVERED(ran) | PARTIAL | BLIND | COVERED(killed:Neo) | – | BLIND |
| LiDAR/optics subcomp | PARTIAL | BLIND | **COVERED(WATCH:SOSLAB)** | BLIND | BLIND | COVERED(WATCH:HSAI) |
| Power components | PARK(understood) | PARTIAL | BLIND | BLIND | BLIND | BLIND |
| Data/mocap/sim | PARTIAL(OMG.L) | BLIND | BLIND | BLIND | – | BLIND |

## Buyer-BOM teardown status (cross-node vector)
- Figure (prior fire): captive/mega-cap dead end.
- Apptronik Apollo: **dead end** — disclosed suppliers are TI/Jabil/NVIDIA/Google (mega-cap); mechanical core (actuators, gearboxes, FT sensors, encoders, batteries) proprietary/undisclosed.
- Agility Digit: **dead end** — explicitly vertically integrated (RoboFab, ~75% US-sourced parts, vendors unnamed); disclosed partners (NVIDIA/Intel/Schaeffler/Foxconn/Google) all mega-cap.
- **Lesson: outsourcing-buyer hypothesis is weaker than assumed for both Apptronik and Agility — both protect mechanical-component vendor names as competitive info. Next BOM teardown should target AV sensor pods (Waymo/Zoox) or Chinese humanoid OEMs (Unitree/UBTECH), which historically disclose more tier-2/3 vendor names via supply-chain press in China.**

## Sourcing-vector queue (pop top unused each dry run; recycle when exhausted)
1. ~~EDGAR EFTS "significant customer" + humanoid/AV/robot in 10-Ks~~ — POPPED 2026-07-05, 0 confirmed hits (mega-caps/false-positives only; 2 speculative micro-caps killed)
2. ~~Apptronik Apollo BOM teardown~~ — POPPED 2026-07-05, dead end
3. ~~Agility Digit BOM teardown~~ — POPPED 2026-07-05, dead end
4. **AV sensor-pod BOM teardown (Waymo 6th-gen / Zoox) — NEXT UP**
5. ~~Korea KOSDAQ reducer/motor/sensor screen (DART "로봇")~~ — POPPED 2026-07-05, PRODUCTIVE (SOS Lab found)
6. ~~Japan JASDAQ/TSE-Standard precision-parts screen (TDnet "ロボット")~~ — POPPED 2026-07-05, mostly dead end; KyoHA consortium logged as standing watch mechanism
7. Taiwan TWSE/TPEx linear-motion / PCB-for-edge-AI screen
8. 13F KOID minus ROBO/BOTZ sub-$3B residual
9. Patent assignees CPC B25J/F16H, sub-$500M, 2022–2025
10. Robotics consortium / Automatica-IREX-CES exhibitor lists (partially covered via KyoHA — recheck monthly for new small-cap joiners)
11. China-listed A-share reducer/magnet names (access-flagged, for mapping)
12. Design-win/"qualified supplier" PR sweep, precision-motion SIC
13. Data-center liquid-cooling COMPONENT sub-tier (QD couplings, TIM) small-caps
14. Ball-screw / roller-screw sub-tier (legs/linear actuators)
15. Specialty materials: magnet wire, electrical steel, flexspline forgings
16. **NEW — W-track specific:** world-model data-capture rig hardware (motion-capture suits, egocentric cameras, simulation-to-real hardware), synthetic-data-gen compute tier-2/3
17. **NEW — R-track:** Chinese humanoid OEM (Unitree/UBTECH) tier-2/3 BOM teardown — Chinese supply-chain press often names vendors more freely than US/EU peers
18. **NEW — Korea round 2:** DART direct filing pull for SBB Tech contract terms + SOS Lab financials (solvency check); Hwashin Precision Atlas-supplier status (only "evaluated," not confirmed — worth one more check)
