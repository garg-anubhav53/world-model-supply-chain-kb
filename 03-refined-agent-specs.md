# Refined Agent Architecture — Wave-Based, Market-Pricing-Central

*2026-07-05. Supersedes 02. Rebuilt per user feedback + Desktop/CLAUDE.md operating doctrine.*

## Organizing principle
Follow **forced capital spend**, not milestones: who raised cash → what they are *non-discretionarily forced* to buy in the next **6–9 months** to make ANY roadmap progress → which suppliers catch it. Forced spend is indifferent to the humanoid failure base rate (a company that dies still bought its compute/sensors/robots first).

## The central lens (applies at EVERY wave, not the end)
**"What has the market NOT already priced, as of today 2026-07-05?"** Every public name we touch gets a *live* price/valuation check — 3/6/12-mo move, valuation vs. own history, and whether the order/revenue inflection is already reflected. **No stale data.** Candidates that have already re-rated are pruned early; the prize is the **not-yet-moved but forced-spend-exposed** name. This is a first-class filter woven through the funnel, not a final step.

## Two parallel tracks (same structure, different meat)
- **Track W — World-Model supply chain** (labs: World Labs, AMI, Physical Intelligence, Runway, Cosmos, Odyssey, Decart…)
- **Track R — Robotics / Physical-AI supply chain** (builders: Figure, Apptronik, Neura, Skild, Boston Dynamics, Agility…)

Shared nodes (compute, sensors, optics) are de-duped across tracks. Each track reports independently.

## Grounding standard (kills speculation)
Every needs-assessment is done through **two expert lenses, explicitly**:
- **Engineer lens** — how world models / robots are *actually* built; which physical inputs are non-negotiable in the next 6–9 months and *why* (not what's hyped for 2030).
- **Supply-chain-analyst lens** — maps each need to real vendors; flags chokepoints, single-source, lead times, captive/vertical-integration risk.
A node only advances if BOTH lenses agree it is real, near-term, and non-discretionary. Confidence-tag everything; low-confidence = early-kill candidate.

---

## Wave structure (parallel fan-out; report after each; kill before advancing)

### Wave 0 — Grounded needs → node map  *(report before Wave 1)*
Per track, 2 agents:
- **W0a Engineer** (Sonnet, no schema, ≤6 searches) → non-negotiable BOM for next 6–9 mo, each node tagged {confidence, why-forced, time-to-spend}.
- **W0b Supply-chain analyst** (Sonnet, no schema, ≤6 searches) → maps needs to vendor categories; flags chokepoint / single-source / captive / vertical-integration risk.
- **W0-extract** (Haiku, schema) reads both, emits the node table.
**Kill here:** speculative, discretionary, or >9-mo-horizon nodes are dropped and *named as dropped*.
→ Report: grounded node map per track + first kill list.

### Wave 1 — Forced-spend + suppliers + FIRST market-pricing triage  *(the core wave)*
On surviving nodes, pipeline (no barrier):
- **W1a Forced-Spend Ledger** (Sonnet, ≤8 searches) → who raised / must spend on this node, $ and timing; weight by cash-in-bank, model burn-before-failure. Haiku extractor → JSON.
- **W1b Supplier enumeration** (Sonnet, ≤8) → public small/mid-cap vs. mega-cap vs. private vs. China/captive, per node.
- **W1c Market-pricing triage** (Sonnet sweep + Haiku extractor) → **live** 3/6/12-mo move + valuation-vs-history for every public name; tag ALREADY-RAN / PARTIAL / NOT-MOVED as of 2026-07-05.
**Kill here:** nodes whose only catchable suppliers already ran, or whose spend leaks entirely to mega/China/private → abandon and say so.
→ Report: node × (forced-spend size, supplier list, priced-in status). **The not-yet-re-rated shortlist emerges here.**

### Wave 2 — Asymmetry + red-team, survivors only  *(Opus judgment)*
On the NOT-MOVED shortlist only:
- **W2a Revenue-multiplication** (Opus, no schema) → content-$-per-buyer × forced-spend scenario ÷ supplier's *current* segment revenue; keep only credible >2–3x. Haiku extractor.
- **W2b Leakage red-team** (Opus) → vertical integration, China/captive, private-only, synthetic-data substitution, mega-cap capture; *try to kill each name.*
→ Report: ranked survivors with asymmetry math + kills-survived.

### Wave 3 — Watchability + synthesis, survivors only
- **W3a Leading indicators** (Sonnet/Haiku) → exact signal + threshold + source + lag that front-runs a re-rating.
- **W3b Final synthesis** (Opus) → conviction ranking, entry/monitoring, what-must-be-true.
→ Report: monitorable, ranked candidate set. Only now consider a full scanner.

---

## CLAUDE.md compliance (baked in)
- **Model tier on every call:** Haiku = extractors/parsers/pricing-JSON; Sonnet = scouts/sweeps/grounding; Opus = asymmetry, red-team, synthesis only.
- **Worker/extractor split:** heavy web+writer agents get NO schema; a Haiku extractor reads the file and emits JSON.
- **Tool-call caps + stop-and-write** with `coverage_notes`/`gaps`. No unbounded search.
- **Pipeline over barrier;** proceed with what returns (`.filter(Boolean)`); drop stragglers.
- **Sized waves** (~cores−2 concurrent), not one 30-agent blast; both tracks share the concurrency pool.
- **Compress** large outputs; sub-agents return distilled verdicts, not raw dumps. Pass node *slices* inline, not the fat map to every agent.
- **Incremental reporting** after every wave — never silo.
