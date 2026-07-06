# KB INDEX — Supply-Chain Asymmetry Hunter
**Read this FIRST every run (dedup guard).** Structure: flat files at kb/ root + per-company dossiers in kb/companies/ (populated as names are diligenced). Raw grounding archived in ../waves/ — do NOT re-derive it.

## Live candidates (see kb/pipeline.md for full ranked table; 10 live, target 15)
| Ticker | What | Corner | Status |
|---|---|---|---|
| **464080.KQ (SOS Lab)** | Korean automotive/industrial LiDAR | Hyundai MobED co-dev | **WATCH — top idea (3/4 gates), dossier in companies/SOSLAB.md** |
| HSAI | dominant China LiDAR | AV robotaxi/ADAS — now confirmed at 4/5 Chinese robotaxi buyers | WATCH — dossier in companies/HSAI.md |
| **1536.TW (Hota Industrial)** | Taiwan reduction gears | Tesla Optimus-linked JV | **WATCH (fraying — gate 2 unconfirmed 4 fires running, solvency weakening), dossier in companies/HOTA.md** |
| **603662.SH (Keli Sensing)** | China force/torque sensors | Huawei embodied-intelligence design-win | **WATCH — new Fire 5, dossier in companies/KELI.md** |
| **300660.SZ (Jiangsu Leili)** | China hollow-cup motors/joint modules | Zhiyuan Robotics/AgiBot + Wellblue "stable orders" | **WATCH — new Fire 6, dossier in companies/LEILI.md** |
| OMG.L (Oxford Metrics/Vicon) | motion-capture | data/mocap | WATCH(lean-kill) — dossier in companies/OMG.md |
| KLIN.SW (Klingelnberg) | gear grinding+metrology | reducer capital-equipment | WATCH — dossier in companies/KLIN.md |
| NOVT, ON | force-torque, camera CMOS | mixed | WATCH — see watchlist.md |
| TKR (Spinea) | cycloidal reducer | reducers | PARK |
| KASHIFUJI / MLXSF / NEO.TO / 6966.T / SBB Tech / Hephaist Seiko / GSIT / LQMT / SPG / Higen / Robotis / Zhongda Leader / Changsheng Bearing / Zhaowei Mechatronics / TBI Motion / Movella-Xsens / Green Harmonic / Wolong / Zhucheng Tech / Xiangxin Tech / Far East Cable / Siling / Zhongding / China Leadshine / Estun / Jiangsu Guomao / Doosan Robotics / CTS Corp / Shuanglin / Valeo / Neuromeka / Servotronics / Allied Motion(ALNT) / NN Inc(NNBR) / Orbbec | various | various | KILLED — see decisions-log.md |

## Files (flat for simple cloud reads)
- `pipeline.md` — ranked living pipeline (primary working file each fire)
- `coverage-map.md` — node×geo grid + sourcing-vector queue (pop next vector each dry fire)
- `watchlist.md` — live KEEP/watch + the monitoring signal per name
- `prices-cache.md` — last price/move/run-tag per ticker (staleness 7d; refresh if older)
- `decisions-log.md` — append-only KEEP/KILL one-liners (incl. already-run mainstream kills)
- `dead-ends.md` — proven-fruitless nodes/searches — never re-explore
- `trends.md` — specific sub-trends → implicated nodes/companies (make these sharper each run)
- `companies/<TICKER>.md` — per-name dossier: verdict + evidence + financials + re-rating grade + last-updated

## Grounding pointers (raw, ../waves/)
- wave-0-grounding/_node-map.md · wave-1-pricing/_not-moved-shortlist.md · wave-2-widen/_widen-candidates.md · runs/bom-humanoid.md · runs/omg-dive.md
