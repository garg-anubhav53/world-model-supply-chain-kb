# KB INDEX — Supply-Chain Asymmetry Hunter
**Read this FIRST every run (dedup guard).** Structure: flat files at kb/ root + per-company dossiers in kb/companies/ (populated as names are diligenced). Raw grounding archived in ../waves/ — do NOT re-derive it.

## Live candidates (see kb/pipeline.md for full ranked table; 8 live, target 15)
| Ticker | What | Corner | Status |
|---|---|---|---|
| **SMSH (Smart Shooter, TASE)** | Israel defense fire-control/target-acquisition | named US Army/USMC/Navy/UK MoD buyers | **WATCH — strongest in KB, capture-rate gate CLEARED Fire 16, price now binding gate, dossier in companies/SMSH.md** |
| **464080.KQ (SOS Lab)** | Korean automotive/industrial LiDAR | Hyundai MobED+PluD co-dev | **WATCH — top idea (3/4 gates), dossier in companies/SOSLAB.md** |
| HSAI | dominant China LiDAR | AV robotaxi/ADAS — 8 of top-10 robotaxi developers incl. Zoox + Mercedes-Benz (L3 confirmed) + Motional | WATCH — dossier in companies/HSAI.md |
| ~~POCI (Precision Optics)~~ | medical-robotics optics/endoscopes | Procept BioRobotics link vanished from disclosure | **KILLED Fire 32 (staleness-guard re-derivation) — see decisions-log.md, dossier in companies/POCI.md** |
| OMG.L (Oxford Metrics/Vicon) | motion-capture | data/mocap | WATCH(lean-kill) — dossier in companies/OMG.md |
| KLIN.SW (Klingelnberg) | gear grinding+metrology | reducer capital-equipment | WATCH — dossier in companies/KLIN.md |
| **NOVT (Novanta/ATI)** | force-torque sensing (ATI Axia80/Omega191) | unnamed-Amazon warehouse win, NVIDIA Halos partner, 10+ unnamed humanoid engagements | **WATCH (materiality-capped) — first-ever full gate-check Fire 33, dossier in companies/NOVT.md** |
| ON | camera CMOS | mixed | WATCH — see watchlist.md |
| TKR (Spinea) | cycloidal reducer | reducers | KILLED (Fire 43, 2/8) |
| PENDING: Momentus (MNTS, new Fire 16, space vertical) / Zhejiang Fine Motion (环动科技, pre-IPO, buyer-claim caution) / Laifual Harmonic Drive (03952.HK) / Xinjian Transmission (新剑传动, pre-IPO) / Weimao Electronics (920346.BJ) / Landai Technology (002765.SZ) | space robotics contracts / humanoid roller-screw/joint-module (Tesla/Zhiyuan/Unitree named, unconfirmed for Fine Motion) / interconnect / IPO-pipeline supplier finds | forward-listing + interconnect + space | see pipeline.md, companies/XINJIAN.md |
| KASHIFUJI / MLXSF / NEO.TO / 6966.T / SBB Tech / Hephaist Seiko / GSIT / LQMT / SPG / Higen / Robotis / Zhongda Leader / Changsheng Bearing / Zhaowei Mechatronics / TBI Motion / Movella-Xsens / Green Harmonic / Wolong / Zhucheng Tech / Xiangxin Tech / Far East Cable / Siling / Zhongding / China Leadshine / Estun / Jiangsu Guomao / Doosan Robotics / CTS Corp / Shuanglin / Valeo / Neuromeka / Servotronics / Allied Motion(ALNT) / NN Inc(NNBR) / Orbbec / Hota Industrial(1536.TW) / Jiangsu Leili(300660.SZ) / SmartSens(688213.SH) / Zhejiang Sanhua(002050.SZ) / Sona BLW(SONACOMS) / Fulin Precision(300432.SZ) / Bukom(688160.SH) / Moons' Electric(603728.SH) / Ouster(OUST) / Belden(BDC) / MicroVision(MVIS) / Element Fleet Mgmt(EFN) / UL Solutions(ULS) / Ramkrishna Forgings(RKFORGE) / Kraken Robotics(PNG) / Ocean Power Technologies(OPTT) / Weifeng Electronics(301328.SZ) / Innoviz(INVZ) / KULR Technology(KULR) / RoboSense(2498.HK) / Huarui Precision(688059.SH) / NextVision(NXSN.TA) / Aryt Industries(ARYT.TA) / Dongfang Precision(002611.SZ) / Everwin Precision(300115.SZ) / Arbe Robotics(ARBE) / TomTom(TOM2.AS) / Zen Technologies(ZENTEC) / Keli Sensing(603662.SH) / Ningbo Yunsheng(600366.SH) / Smart Shooter(SMSH) / Aishida(002403.SZ) / Momenta Global(6880.HK) / Chenming Electronic(3013.TW, misidentified as "Cooler Master") / Mobyus & Value Chain (Korea) / **Jiangsu Azure/蔚蓝锂芯(002245.SZ) / Hanwei Technology/Nengsida(300007.SZ) / Donghua Testing(300354.SZ) / Jiechang Drive(603583.SH) / Dingzhi Technology(BJ873593) / Swarmer(SWMR) / Boresight(ASX:BST) / Lingyunguang/LUSTER LightTech(688400.SH)** | various | various | KILLED/PARK — see decisions-log.md |

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
