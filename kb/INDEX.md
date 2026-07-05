# KB INDEX — Supply-Chain Asymmetry Hunter
**Read this FIRST every run (dedup guard).** Structure: flat files at kb/ root + per-company dossiers in kb/companies/ (populated as names are diligenced). Raw grounding archived in ../waves/ — do NOT re-derive it.

## Live candidates (causal dive pending)
| Ticker | What | Corner | Status |
|---|---|---|---|
| KASHIFUJI (verify JP listing) | gear-hobbing/skiving machine tools | reducer capital-equipment | dive PENDING |
| KLIN.SW (Klingelnberg) | gear grinding + metrology | reducer capital-equipment | dive PENDING |
| MLXSF / MELE.BR (Melexis) | robot-joint inductive encoder ICs | sensor ICs | dive PENDING |
| NEO.TO (Neo Performance) | ex-China NdFeB + Dy/Tb | magnets 2nd-order | dive PENDING |
| 6966.T (Mitsui High-tec) | motor-core laminations | actuator inputs | dive PENDING (test if already priced) |
| MKA.TO / IXR.AX / UCU.V | heavy-RE magnet recyclers | magnets 2nd-order | 2nd-tier |
| OMG.L / HSAI / NOVT / ON | survivors from pricing triage | mixed | WATCH — see watchlist.md |

## Files (flat for simple cloud reads)
- `watchlist.md` — live KEEP/watch + the monitoring signal per name
- `prices-cache.md` — last price/move/run-tag per ticker (staleness 7d; refresh if older)
- `decisions-log.md` — append-only KEEP/KILL one-liners (incl. already-run mainstream kills)
- `dead-ends.md` — proven-fruitless nodes/searches — never re-explore
- `trends.md` — specific sub-trends → implicated nodes/companies (make these sharper each run)
- `companies/<TICKER>.md` — per-name dossier: verdict + evidence + financials + re-rating grade + last-updated

## Grounding pointers (raw, ../waves/)
- wave-0-grounding/_node-map.md · wave-1-pricing/_not-moved-shortlist.md · wave-2-widen/_widen-candidates.md
