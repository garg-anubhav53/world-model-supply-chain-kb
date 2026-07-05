# KB INDEX — Supply-Chain Asymmetry Hunter
**Read this FIRST every run (dedup guard).** Structure: flat files at kb/ root + per-company dossiers in kb/companies/ (populated as names are diligenced). Raw grounding archived in ../waves/ — do NOT re-derive it.

## Live candidates (see kb/pipeline.md for full ranked table; 8 live, target 15)
| Ticker | What | Corner | Status |
|---|---|---|---|
| **464080.KQ (SOS Lab)** | Korean automotive/industrial LiDAR | Hyundai MobED co-dev | **WATCH — top idea (3/4 gates), dossier in companies/SOSLAB.md** |
| **1536.TW (Hota Industrial)** | Taiwan reduction gears | Tesla Optimus-linked JV | **WATCH — new Fire 4, dossier in companies/HOTA.md** |
| HSAI | dominant China LiDAR | AV robotaxi/ADAS (Li Auto/Great Wall + confirmed Zoox) | WATCH — dossier in companies/HSAI.md |
| OMG.L (Oxford Metrics/Vicon) | motion-capture | data/mocap | WATCH(lean-kill) — dossier in companies/OMG.md |
| KLIN.SW (Klingelnberg) | gear grinding+metrology | reducer capital-equipment | WATCH — dossier in companies/KLIN.md |
| NOVT, ON | force-torque, camera CMOS | mixed | WATCH — see watchlist.md |
| TKR (Spinea) | cycloidal reducer | reducers | PARK |
| Pending (not yet WATCH): Keli Sensing 603662.SH, China Leadshine 002979.SZ | force/torque, servo motors | China | causal-check pending — see pipeline.md |
| Pending price-check: RoboSense 2498.HK, Shuanglin 300100.SZ (price-conflict), 8 China 2nd-tier humanoid-BOM names | various | China | see coverage-map.md queue #18-19 |
| KASHIFUJI / MLXSF / NEO.TO / 6966.T / SBB Tech / Hephaist Seiko / GSIT / LQMT / SPG / Higen / Robotis / Zhongda Leader / Changsheng Bearing / Zhaowei Mechatronics / TBI Motion / Movella-Xsens | various | various | KILLED — see decisions-log.md |

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
