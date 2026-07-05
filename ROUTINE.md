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
