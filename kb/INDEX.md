# KB INDEX — Supply-Chain Asymmetry Hunter
**Read this FIRST every run (dedup guard).** Structure: flat files at kb/ root + per-company dossiers in kb/companies/ (populated as names are diligenced). Raw grounding archived in ../waves/ — do NOT re-derive it.

## Live candidates (see kb/pipeline.md for full ranked table; 11 live, target 15)
| Ticker | What | Corner | Status |
|---|---|---|---|
| **464080.KQ (SOS Lab)** | Korean automotive/industrial LiDAR | Hyundai MobED+PluD co-dev | **WATCH — top idea (3/4 gates), dossier in companies/SOSLAB.md** |
| HSAI | dominant China LiDAR | AV robotaxi/ADAS — 8 of top-10 robotaxi developers incl. Zoox + Mercedes-Benz + Motional | WATCH — dossier in companies/HSAI.md |
| **603662.SH (Keli Sensing)** | China force/torque sensors | Huawei embodied-intelligence design-win | **WATCH — dossier in companies/KELI.md** |
| **ARBE (Arbe Robotics)** | Israel 4D imaging radar | AV — named Hirain L4-robotaxi + US Army wins | **WATCH (early-stage) — dossier in companies/ARBE.md** |
| **ZENTEC (Zen Technologies)** | India defense-robotics (C-UAS + Bhairav quadruped stake) | named Indian MoD buyer | **WATCH (early-stage, new Fire 10) — dossier in companies/ZENTEC.md** |
| **INVZ (Innoviz Technologies)** | Israel LiDAR | AV — named Daimler Truck/Torc Robotics L4-truck design-win | **WATCH (early-stage, new Fire 10) — dossier in companies/INVZ.md** |
| **POCI (Precision Optics)** | medical-robotics optics/endoscopes | near-certain buyer Procept BioRobotics (insourcing risk) | **WATCH (weak, new Fire 10) — dossier in companies/POCI.md** |
| OMG.L (Oxford Metrics/Vicon) | motion-capture | data/mocap | WATCH(lean-kill) — dossier in companies/OMG.md |
| KLIN.SW (Klingelnberg) | gear grinding+metrology | reducer capital-equipment | WATCH — dossier in companies/KLIN.md |
| NOVT, ON | force-torque, camera CMOS | mixed | WATCH — see watchlist.md |
| TKR (Spinea) | cycloidal reducer | reducers | PARK |
| PENDING (Fire 10): RoboSense 2498.HK / Weimao Electronics 833346.BJ / Huarui Precision 688059.SH / Landai Technology 002765.SZ | warehouse-AMR LiDAR / interconnect / Unitree+Leju IPO-pipeline supplier finds | adjacent-vertical + interconnect + forward-listing | see pipeline.md |
| KASHIFUJI / MLXSF / NEO.TO / 6966.T / SBB Tech / Hephaist Seiko / GSIT / LQMT / SPG / Higen / Robotis / Zhongda Leader / Changsheng Bearing / Zhaowei Mechatronics / TBI Motion / Movella-Xsens / Green Harmonic / Wolong / Zhucheng Tech / Xiangxin Tech / Far East Cable / Siling / Zhongding / China Leadshine / Estun / Jiangsu Guomao / Doosan Robotics / CTS Corp / Shuanglin / Valeo / Neuromeka / Servotronics / Allied Motion(ALNT) / NN Inc(NNBR) / Orbbec / Hota Industrial(1536.TW) / Jiangsu Leili(300660.SZ) / SmartSens(688213.SH) / Zhejiang Sanhua(002050.SZ) / Sona BLW(SONACOMS) / Fulin Precision(300432.SZ) / Bukom(688160.SH) / Moons' Electric(603728.SH) / Ouster(OUST) / Belden(BDC) / MicroVision(MVIS) / Element Fleet Mgmt(EFN) / UL Solutions(ULS) / **Ramkrishna Forgings(RKFORGE) / Kraken Robotics(PNG) / Ocean Power Technologies(OPTT) / Weifeng Electronics(301328.SZ)** | various | various | KILLED/PARK — see decisions-log.md |

## Files (flat for simple cloud reads)
- `pipeline.md` — ranked living pipeline (primary working file each fire)
- `coverage-map.md` — node×geo grid + sourcing-vector queue (pop next vector each dry fire)
- `watchlist.md` — live KEEP/watch + the monitoring signal per name
- `prices-cache.md` — last price/move/run-tag per ticker (staleness 7d; refresh if older)
- `decisions-log.md` — append-only KEEP/KILL one-liners (incl. already-run mainstream kills)
- `decisions-log-archive.md` — older rolled-off KILL entries (read only to dedup an old name not in the main log)
- `dead-ends.md` — proven-fruitless nodes/searches — never re-explore
- `trends.md` — specific sub-trends → implicated nodes/companies (make these sharper each run)
- `companies/<TICKER>.md` — per-name dossier: verdict + evidence + financials + re-rating grade + last-updated

## Grounding pointers (raw, ../waves/)
- wave-0-grounding/_node-map.md · wave-1-pricing/_not-moved-shortlist.md · wave-2-widen/_widen-candidates.md · runs/bom-humanoid.md · runs/omg-dive.md
