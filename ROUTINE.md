# DRAFT ROUTINE — Supply-Chain Asymmetry Hunter (self-improving, checkpointed)

*Draft 2026-07-05. NOT yet scheduled — awaiting user confirmation of execution parameters (see §8).*
Governed by Desktop/CLAUDE.md (model tiering, worker/extractor split, tool-call caps, no-straggler). This file is the playbook each triggered run executes.

## 1. Objective (unchanged criteria)
Continuously find suppliers to the **world-model / robotics / AV** buildout that (a) can see **revenue MULTIPLY** (spend dwarfs their base), (b) have a **physically-necessary, high-certainty causal link** to a specific tracked trend, and (c) have **NOT already re-rated**. Get faster and cheaper every run by reusing a persistent knowledge base instead of re-gathering.

## 2. Knowledge base (the anti-duplication layer) — `kb/`
```
kb/
  INDEX.md         master registry: every company/node/trend → 1 line + file pointer + last-updated. CHECK THIS FIRST, always.
  companies/<TICKER>.md   ticker, node(s), causal link {airtight/probable/speculative}, revenue base + segment, multiplication math, VERDICT {keep/kill/watch}, last-price + run-status + date, sources
  nodes/<node>.md         what it is, forced?, vendors, leakage (mega/captive/china/private), status
  trends/<trend>.md       a SPECIFIC sub-trend (e.g. "humanoid-dexterous-hand-ramp", "1p6T-optical-transition", "rare-earth-export-controls", "AV-cold-weather-expansion") → implicated nodes → implicated companies
  prices/CACHE.md         ticker | last price | 3/6/12m move | run-tag | date-pulled  (staleness window: 7 days)
  decisions/LOG.md        append-only KEEP/KILL with reason + date — NEVER re-diligence a killed name unless new catalyst
  dead-ends.md            nodes/searches proven fruitless (e.g. tactile e-skin = no public vehicle) — do not re-explore
  lessons.md             per-run: what searches were wasteful, what to do differently — read at run start
watchlist.md             current KEEP survivors + the monitoring signal that would trigger action
```
**Dedup rule:** before any web lookup, read INDEX + the relevant file. If fresh (price <7d, causal <30d), REUSE — do not re-gather. Only refresh stale/missing. This is the primary token-saver and compounds every run.

## 3. State & resumability — `STATE.md`
Holds: current phase, a **task queue** (prioritized backlog of atomic actions), token-budget-used estimate, and "next action" pointer. Checkpointed **after every agent batch** (finer than per-wave), so a mid-run kill (like the 2026-07-05 session-limit) loses ~nothing.

## 4. Per-run loop (each scheduled fire)
1. **Load** STATE + INDEX + lessons.md (cheap, Haiku/inline). Identify stale items + top backlog tasks.
2. **Plan** the run: pick the highest-value bounded chunk that fits the per-run budget (§7). Prefer: finish in-flight causal dives → refresh stale KEEP prices → drill a hot sub-trend → widen into a new node.
3. **Execute a bounded wave-step** with tiering:
   - **Sonnet** workers: discovery scouts, pricing sweeps, trend drill-downs (≤6–8 searches each, stop-and-write-partial with coverage_gaps).
   - **Opus**: only the deep causal-chain diligence + final synthesis, on a SMALL candidate set.
   - **Haiku**: extraction → KB JSON, INDEX/price-cache updates, dedup.
   - Worker writes memo (no schema) → Haiku extractor updates KB.
4. **Persist immediately** after each agent: update companies/nodes/trends/prices/decisions + INDEX. Never hold insight only in context.
5. **Report incrementally**: append a dated bullet to `REPORT.md` after each batch; push-notify ONLY material events (new KEEP survivor, a KEEP name showing a pre-re-rating signal, a killed thesis).
6. **Budget check**: if projected next batch exceeds remaining per-run budget → checkpoint STATE, write lessons.md, exit clean.
7. Loop to 2 until budget exhausted or backlog empty.

## 5. Self-improvement (gets better each run)
- `lessons.md` + `dead-ends.md` read at start → never re-explore killed nodes/searches.
- `trends/` grows: each run tries to make the thesis MORE specific (a named lab capex event, a named production ramp) and re-maps which nodes/companies that forces — sharper causal links over time.
- Cached insights mean cross-lookups (e.g. "who supplies X") resolve from KB, not the web.

## 6. Failure handling (a flaky web ≠ a failed run)
- Every agent bounded; `.filter(Boolean)` on returns; never block on a straggler.
- A failed fetch / search → logged as a `coverage_gap` + a "needs-retry" task in STATE; the run proceeds. No single lookup can fail the run.
- Unverified prices are tagged `stale?` and re-queued, never trusted silently.

## 7. Budget & cadence
- **Per-run budget:** a soft cap of ~N Sonnet scouts + ~M Opus dives per fire (default N≈6, M≈3), so each fire is a bounded, checkpointed chunk — not an unbounded blast.
- **Runs until plan tokens run out:** frequent checkpointing means if the harness kills the run on a plan/token limit, the next scheduled fire simply resumes from STATE. "Runs until out, ready to run again" = recurring schedule + sub-wave checkpoints.

## 8. Seed backlog (carry-over from the 2026-07-05 manual run)
1. **Finish Wave-3 causal dives (Opus):** Kashifuji+Klingelnberg (gear machine-tools), Melexis (MLXSF), Neo Performance (NEO.TO), Mitsui High-tec (6966.T). [interrupted, zero memos]
2. 2nd-tier magnet recyclers: MKA.TO / IXR.AX / UCU.V.
3. Then Wave-4 synthesis + watchlist on KEEP survivors.
4. Standing: refresh KEEP prices weekly; drill one new sub-trend per run.
Already-killed (do not revisit w/o catalyst): the whole re-rated mainstream list in wave-1-pricing/_not-moved-shortlist.md. Parked (market-understood): power BELFB/VSH/NVTS, crowded photonics.

## 9. CONFIRMED EXECUTION (2026-07-05)
- **Trigger:** REMOTE routine (claude.ai cron) — runs unattended. → forces KB off local disk (see §10).
- **Cadence:** "continuous until tokens out" = frequent cron (target hourly); each fire runs its cloud session to its limit, commits, next tick resumes from checkpoint.
- **Notifications:** SILENT — no pushes; all output to `REPORT.md`.
- **KB seed:** migrate existing `waves/` (Wave 0–2 findings, kills, parked list, 4 pending causal dives) into `kb/`.
- **Per-fire budget:** ~6 Sonnet scouts + ≤3 Opus dives, then checkpoint (adjustable).

## 10. REMOTE ⇒ KB MUST BE CLOUD-ACCESSIBLE — recommended: private GitHub repo
A cloud routine cannot see local Desktop files. Resolution: host `kb/` (and `waves/`, `REPORT.md`, `STATE.md`) in a **private GitHub repo**. Each fire: clone → read INDEX (dedup) → bounded chunk → write insights → commit/push. This gives durable, versioned, cross-fire state.
**BLOCKER (needs user OK — outward-facing):** create/push to a private GitHub repo + grant the scheduled agent access. Do NOT push research externally until confirmed.
Fallback if GitHub is unwanted: switch trigger to LOCAL durable schedule (KB stays on Desktop, only advances while a local session is open).

## 11. BUILD ORDER (once GitHub OK'd)
1. `git init` the `World Model Supply Chain/` folder; migrate `waves/` → `kb/` (companies/nodes/trends/prices/decisions/INDEX seeded from Wave 0–2).
2. Create private GitHub repo; push.
3. Seed `STATE.md` backlog (§8) + empty `REPORT.md`.
4. Create the remote routine (hourly) with this playbook as its prompt; verify one manual fire; then let cron run.
Note: 2026-07-05 session hit its limit (resets 7pm Europe/Zagreb) — build may need to wait for reset.

## 12. SOURCING & EFFICIENCY UPGRADES (v2, 2026-07-05)

### A. Higher-alpha supply-chain mapping — upgrade the discovery step (§4.3)
Stop relying on generic "who makes X" scouting. Layer these, and record the EVIDENCE of each supplier link in kb/companies (so the causal chain rests on a disclosure, not inference):
- **Buyer-BOM teardown:** start from a specific buyer artifact (a humanoid, an AV sensor pod, a GPU rack), decompose its bill-of-materials to named parts → find each part's supplier. Reason from the physical object, not the narrative.
- **Disclosure mining:** 10-K/10-Q customer-concentration & "significant customers," MD&A, supplier design-win PRs, buyer earnings-call supplier mentions.
- **Flow signals:** import/export records, qualified-vendor lists, ecosystem/consortium membership (e.g., Nvidia partner lists), conference exhibitor & award lists.
- **Nth-order expansion:** for any already-ran node, map its INPUTS (arms-dealer-to-the-arms-dealer) — proven productive (gear machine-tools, magnet 2nd-order).
- Cheapest signal first; escalate only when a link looks real.

### B. Cheap ELIMINATION GATE — before ANY Opus diligence (new §4 step; Sonnet/Haiku)
Biggest token saver after KB dedup. Kill a candidate fast if:
- **Financial distress:** going-concern, covenant/liquidity risk, cash << burn, serial heavy dilution, negative FCF with no path. Distress = kill regardless of causal story.
- **Weak management execution:** serial guidance misses, restatements, governance flags, value-destructive M&A, exec churn.
- **Re-rating GRADE (graded, not binary):** NOT-MOVED → full candidate · PARTIALLY re-rated → keep, lower priority, demand stronger multiplication · GREATLY re-rated → drop, minimal time.
Only names passing the gate reach Opus causal diligence.

### C. KB PRUNING discipline — run-end step (keeps cloud reads cheap & REPORT sharp)
- Each evergreen file capped (~1 screen): only current distilled verdict + key evidence + last-updated. Raw research goes to `runs/<id>/` logs, never the evergreen file.
- Prune pass each run: compact verbose files, archive killed names to `decisions/LOG.md` as ONE line and delete their long files, keep INDEX tight.
- **REPORT.md is curated, not a dump:** top-N most-interesting LIVE ideas, one-paragraph thesis each, freshest first; everything else stays in the KB.

### D. Simplicity & time-boxing (reduce complication)
The goal is a SHORT LIST of straightforward ideas that deeply nail the science, the linkage, financial health, and execution — not sprawling investigations.
- **Time-box every agent.** If a diligence runs long, keeps spawning searches, or the causal chain needs ever more caveats to survive, ABANDON it and log "too-complicated / low-confidence" in decisions/LOG. **Complication is itself a sell signal** — a clean, obvious causal story beats a clever fragile one.
- A candidate should be expressible in a few sentences: what they sell → who is forced to buy it → why demand multiplies → financials are healthy → not yet re-rated. If it can't be, drop it.
- Bias to clarity and confidence over completeness. Fewer, stronger ideas.

## 13. NORTH STAR + guardrails (do NOT drift, do NOT give up)

### GOAL — re-read at the start of EVERY run; the only thing that matters
Find **publicly-traded, NOT-yet-re-rated companies whose revenue is VERY LIKELY to MULTIPLY** because they are near-forced suppliers to the world-model / robotics / AV capital injection. Output = a ranked **BUY/WATCH** list, never a catalog.

### The 4 hard gates every BUY must pass (score each 0–2; a BUY is strong on ALL four)
1. **NOT re-rated** (live price; greatly-run = disqualified).
2. **Causal link AIRTIGHT & physically necessary** — a specific forced buyer, not a narrative.
3. **Revenue MULTIPLIES** — forced spend dwarfs the current base. Small base + ONE concentrated design-win beats a big diversified base.
4. **Financially healthy + competent management.**
Failing #1 or #3 = not a buy however interesting (Wave-3 proof: Klingelnberg real but bump-not-multiply → WATCH; Neo/Mitsui already-run → KILL).

### Anti-drift
- Score every candidate against the 4 gates; off-thesis names are dropped, not chased. Tangents go to trends/ for later, not followed now.
- Progress = **NEW QUALIFIED candidates found**, not searches run. The funnel only moves toward a BUY list.

### Anti-false-negative — do NOT conclude "no ideas exist"
- **STANDING PRIOR:** >$50B of forced capital is being injected → forced beneficiaries MUST exist. A dry run is a **SEARCH failure, not a THESIS failure.** Never terminate the hunt.
- If a wave kills every candidate, the NEXT wave MUST open a **new sourcing vector** (fresh buyer-BOM teardown, new sub-trend, smaller/earlier names, new geography) — never just re-confirm kills.
- **Feed kill-reasons back into sourcing.** Wave-3 kills were "already-run" or "too-diversified" → next sourcing biases to SMALL-base names with ONE forced design-win, surfaced by starting from the BUYER's bill-of-materials.
- Always keep a live "best current idea" so REPORT never reads "nothing found."

### Each search better than the last
- `lessons.md` updated every run: what made the last batch weak + sharper targeting next.
- A **sharpened-hypothesis** line in STATE evolves each run. Current: *the un-crowded multiplier is a small-base company with a single forced design-win into a high-volume program, found via buyer-BOM teardown — not a diversified component maker.*

## 14. v3 IDEA-YIELD UPGRADES (many candidates × high pass-rate) — adopted 2026-07-05
Synthesized from 4 improvement agents. Upgraded per-fire loop:
**SOURCE (breadth) → CHEAP PRE-GATE (Haiku, kill most cheaply) → EV-RANK → CAUSAL-RIGOR checklist (best-first) → PERSIST → PIPELINE update (keep ≥15 WATCH) → PRUNE → COMMIT.** Never exit empty.

### A. SOURCING methods (rotate; each fire hit a BLIND coverage cell / pop next vector)
- **Multi-buyer BOM teardown**, biased to buyers that OUTSOURCE (Apptronik, Agility, Chinese OEMs, AV sensor pods) — and go Tier 2/3 (encoder disks, flexspline forgings, magnet wire, gate drivers), not just Tier 1. (Figure is captive — low yield.)
- **SEC EDGAR full-text (EFTS, free):** `"significant customer" AND (humanoid OR "collaborative robot" OR "autonomous vehicle" ...)` in 10-Ks; + design-win / "qualified supplier" language across precision-motion SIC (3562/3679/3825/3829).
- **13F delta:** specialist robotics funds/ETFs (e.g. KOID) minus generalist (ROBO/BOTZ) → sub-$3B residual = neglected set.
- **Asia small-cap screens:** KOSDAQ/JASDAQ/TWSE + DART/TDnet keyword (humanoid/로봇/ロボット), small revenue, backlog >30% YoY, no US coverage.
- **Consortium / exhibitor / QVL + patent-assignee** (CPC B25J/F16H) mining for un-covered small names.

### B. CHEAP PRE-GATE (Haiku, Step-0, before ANY Opus) — biggest token saver
- **ALREADY-RUN kill:** 12m move >~+60% OR EV/EBITDA >1.5× 3-yr median → drop (catches VPG/Neo/Mitsui at ~0 cost).
- **SIZE/CONCENTRATION kill:** total rev >$800M AND robotics <30% of it → can't multiply → drop.
- **SOLVENCY kill:** net debt >1.5× EBITDA AND FCF<0 AND no facility → drop.
- **TWO-SOURCE price rule:** never trust one agent's price; confirm via 2 independent fetches (fixes the VPG "not moved" mis-report).
- **EV-RANK** survivors (base-smallness × causal lock-in × time-to-revenue); deep-dive best-first.

### C. CAUSAL-RIGOR checklist (each a kill gate; best-first)
1. **NAMED forced buyer + disclosure/design-win** (SEC/call/PR) — else auto-KILL.
2. **VERTICAL-INTEGRATION early-warning** (buyer job posts/patents/calls building in-house) → require rebuttal.
3. **DISPLACEMENT screen** (sim/synthetic/markerless substitute) → require a reason this product survives.
4. **CAPTURE-RATE:** needed ≠ this vendor wins — # qualified vendors, sole/preferred, ASP trend.
5. **≤24-MONTH revenue mechanism** (named program/quarter) — no 2028 optionality as near-term.
6. **ADVERSARIAL bear paragraph** on survivors — rebut with citations or hold at WATCH.

### D. COVERAGE / PIPELINE / TIMING (KB artifacts)
- **kb/coverage-map.md** — nodes × geographies grid + ~30-item sourcing-vector queue. Touch a BLIND cell / pop next vector each fire; a dry run MUST pop a new vector.
- **kb/pipeline.md** — ranked living pipeline; **target ≥15 live WATCH names.** If <15 → next fire is forced sourcing. Tracks tripwires (book-to-bill>1.15 ×2q, first design-win, capex +20%, insider buys) + first-rev-proximity; a tripwire / SAMPLE-SHIPPED hit → immediate deep-dive.
- **BUYER-CAPEX cascade:** watch ~12 big buyers; a ≥20% capex uplift auto-re-screens their Tier-1/2 suppliers.

## 15. THREE-TRACK COVERAGE + FAIL-SAFE PERSISTENCE (2026-07-05)
### All three tracks, discrete
Every fire sources across **W (world-model labs), R (robotics/humanoid), AV (autonomous vehicles)** — three DISCRETE demand pipelines. Rotate so each gets coverage over time (coverage-map cells carry a track tag). A supplier forced by **≥2 tracks has reinforced demand — NOTE it, but combined exposure is NOT a bonus that overrides the gates.** The ONLY qualifier is passing all 4 gates: a clean single-track name that passes beats a multi-track name that doesn't.
### Fail-safe persistence (PUBLIC repo + layered fallback)
KB = public repo `github.com/garg-anubhav53/world-model-supply-chain-kb` (reads need no auth). Each fire: **clone → loop → commit → push** (ambient/env credential). Robust to ALL failure modes:
- clone fails → seed from the trigger prompt, note CLONE_FAILED;
- a source is blocked → route around it, log the gap, continue;
- push fails (no credential / network) → **FAILSAFE: dump the full contents of every changed KB file into the run's final message**, so nothing is lost and it can be folded back by hand.
Never crash, never lose findings, never conclude "no ideas." Schedule: every 2h at :23 (user-set).

## 16. UNIVERSE = COVERAGE FRAMEWORK, not a checklist (2026-07-06)
The universe (`kb/universe/README.md`) is a holistic map of the ecosystem's DIMENSIONS + discovery sources — NOT a name list to iterate. Each fire: READ `kb/coverage-ledger.md` → pick the least-explored **surface** (a node × geography × business-model reachable via an under-used, ideally NON-anchored discovery source) → discover + gate + diligence names there → UPDATE the ledger. `kb/universe/seed-map.md` holds ~300 illustrative seed names — examples to calibrate a surface, never an assignment. **Completeness = dimension coverage, not name count.** Standing anti-bias rules (full list in README): every fire uses ≥1 NON-anchored source (customs/bill-of-lading, patents, standards rosters, native trade press, forward-listing pipeline); consumables/recurring-spend reframe on every node; rotate business models (only component-BOM is deep — consumables/royalty/TIC/insurance are BLIND); China A/STAR + India + SE-Asia + Israel are ACTIVE, not map-only; every new WATCH back-propagates "who supplies THEM + any IPO/spin into this node"; dead-ends decay (quarterly re-test); any dimension idle 3 fires → forced next. The taxonomy is OPEN — add nodes/sources when found.

## 17. IDEA-YIELD — converge on EFFECTIVE, high-conviction ideas (2026-07-06)
**NORTH STAR (sharpened):** the output is a SHORT set of HIGH-CONVICTION ideas where (a) the forced spend has a HIGH PROBABILITY of flowing to THIS company AT SCALE, (b) the resulting re-rating is LARGE (huge valuation upside), and (c) it is not yet priced. Effective ideas beat a long WATCH list.
**Diagnosis (Fires 1-6):** strong discovery, ZERO BUYs — every candidate stalls at capture-rate (one-of-many supplier), unproven multiplication, or solvency; discovery over-concentrated in Chinese IR-filing names. Fixes:
1. **ASYMMETRY score + rank** every candidate: Upside ≈ (revenue-multiplication factor on the exposed segment) × (probability the spend captures to THIS name) × (not-yet-priced discount). Keep a **top-5 CONVICTION shortlist by asymmetry** in pipeline.md; concentrate compute there.
2. **CONVICTION capture bar:** "high chance of benefiting" needs SOLE / PREFERRED / spec-locked / qualification-moated supply. A non-exclusive 1-of-N supplier is WATCH-optionality, not a BUY — unless content×volume is huge.
3. **PROACTIVELY SIZE multiplication** (don't wait for disclosure): content-$/unit × plausible program unit-volume ÷ current segment base. If even the bull case < ~2-3× the exposed segment, deprioritize regardless of a named buyer.
4. **CONVICTION/DILIGENCE track EVERY fire** (parallel to discovery): deepen the top-asymmetry WATCH names toward a BUY or KILL by chasing the binding gate (confirm/quantify the contract $, verify sole-source, clear the overhang). **Each fire must move ≥1 name toward a DECISION, not only add WATCHes.**
5. **DE-CONCENTRATE:** rotate discovery across the universe framework (non-anchored sources + other geographies + other business models), not just Chinese IR filings.
6. **MORE DEPTH per fire:** ~8-12 Sonnet scouts + ≤4 Opus deep-dives, target 30-40 min wall-clock, stay token-lean (Haiku extract; Opus only for deep reasoning; time-box each agent; abandon complication).

## 18. FAN-OUT ROTATION + KB SCALING (2026-07-06)
### Don't circle — deterministically march the whole universe over time
- `kb/coverage-ledger.md` holds a **ROTATION CURSOR**: an ordered 12-entry ring spanning ALL dimensions (non-anchored sources, blind business-models, blind geographies, blind nodes, adjacent verticals, forward-listing). **EACH fire: read CURSOR → dedicate ≥1 EXPLORE-scout to that focus → advance CURSOR=(CURSOR mod 12)+1 → save it.** This forces the routine through every corner over one cycle regardless of where the productive vein is — the fix for circling.
- **EXPLORE/EXPLOIT split:** of ~8-12 scouts, ≥4 EXPLORE (cursor focus + least-recently-touched surfaces) and the rest EXPLOIT (conviction/diligence on the top-5). A fire may chase a live high-asymmetry lead off-cursor, but must still advance the cursor.
### Stay legible as the KB grows — read the important insights cheaply
- **`kb/DIGEST.md` is the READ-FIRST 1-pager** (rewrite it every fire): top-5 conviction shortlist + binding gates, the cursor focus, one-line coverage status, pointers. **Read DIGEST + INDEX + coverage-ledger + pipeline + the decisions-log KILL-INDEX every fire (all compact); open a full companies/<T> dossier or an archive ONLY for the name you're actively working.** Never read all companies/* or full raw logs each fire.
- **SIZE DISCIPLINE:** keep `decisions-log.md` a compact one-line-per-name KILL-INDEX (ticker | 3-word reason | date); when it exceeds ~120 lines, roll the oldest into `decisions-log-archive.md` (read only to dedup an old name). Keep every evergreen file ~1 screen; raw notes to `runs/<UTC>/`. The DIGEST + INDEX are the routing layer — everything else is opened on demand, so per-fire read cost stays bounded no matter how large the KB gets.

## 19. READ / WRITE CONTRACT + FILE MAP (keep the KB organized — do exactly this each fire)
**FILE MAP (one job per file — never duplicate content across files, never invent new top-level files; extend the map):**
`DIGEST.md`=read-first 1-pager (rewritten each fire) · `INDEX.md`=router/map (update only on structure change) · `coverage-ledger.md`=dimension coverage + ROTATION CURSOR · `pipeline.md`=full ranked table + top-5 conviction shortlist · `decisions-log.md`=append-only KILL-INDEX (1 line/name; roll >120 lines→`decisions-log-archive.md`) · `dead-ends.md`=no-public-vehicle nodes (quarterly decay) · `trends.md`=named sub-trends · `prices-cache.md`=price/move per ticker (7d staleness) · `watchlist.md`=live WATCH + signal · `coverage-map.md`=node×geo grid + vector queue · `universe/README.md`=framework (rarely changes) · `universe/seed-map.md`=example names (append new seeds) · `companies/<T>.md`=per-name dossier (only names diligenced this fire) · `STATE.md`=checkpoint (hypothesis, task queue) · `REPORT.md`=curated human-facing top ideas · `runs/<UTC>/`=raw scratch.

**READ CONTRACT (every fire, in order — bounded & cheap):** 1) DIGEST 2) INDEX 3) coverage-ledger (cursor + blind surfaces) 4) pipeline (shortlist) 5) decisions-log KILL-INDEX (dedup guard) 6) dead-ends 7) STATE 8) universe/README (skim). **ON-DEMAND ONLY:** the specific `companies/<T>` dossier(s) for the shortlist name(s) you diligence this fire; seed-map/coverage-map when picking a surface. **DO NOT** read all `companies/*`, full decisions-log history, or raw `runs/`.

**WRITE CONTRACT (every fire, in order — organized, targeted):** 1) `companies/<T>.md` for each name diligenced 2) append KILL lines to `decisions-log.md` 3) update `pipeline.md` (ranked + top-5 conviction) 4) advance CURSOR + mark reduced dimensions in `coverage-ledger.md` 5) targeted appends to coverage-map/trends/prices-cache/watchlist/dead-ends/seed-map (only what changed) 6) `STATE.md` checkpoint 7) rewrite `REPORT.md` (curated) 8) rewrite `DIGEST.md` LAST (reflects final state). Keep each evergreen file ~1 screen; raw to `runs/`. If a file isn't in the write list for what you did, don't touch it.
