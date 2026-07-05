# Proposed Diligence Agents (pre-scanner vetting)

*2026-07-05. These agents VET the thesis before we spend compute on full scanners + name-level diligence. Each has a mission, the crux it resolves, inputs, outputs, and the go/no-go decision it feeds. Ordered by leverage. Agents 1–4 are the core kill-or-confirm set; 5–6 build the universe once the thesis survives.*

---

## Agent 1 — Spend Decomposition ("where do the dollars actually go?")
**Crux:** Assumption 1 + the mechanism problem. Of the freshly-raised world-model capital, what fraction is spendable on *investable small/mid-cap suppliers* vs. mega-cap compute (Nvidia/hyperscalers/memory) vs. talent/opex?
**Method:** Build a bottoms-up allocation model per funded lab (compute %, talent %, physical data-collection %, sensors/robots %, real estate/power %). Cross-check against stated capex plans (e.g., Luma's 2-GW cluster), cloud commitments (CoreWeave, AWS Trainium), and comparable AI-lab burn structures.
**Output:** A dollar-weighted funnel: "$X raised → $Y reaches investable-supplier layer over 6–12 mo." Plus a verdict on whether the addressable pool is big enough to matter.
**Feeds:** Whether Thesis A is viable at all, or we must pivot to Thesis B.

## Agent 2 — Customer Attribution / Follow-the-PO ("who is actually buying?")
**Crux:** Assumption 3. For the names that ALREADY exploded (VPG, Ouster, Aeva, Teradyne, Vertiv, Micron/Hynix), trace the *actual* customers behind the order surge — world-model labs vs. humanoid OEMs vs. hyperscalers vs. defense.
**Method:** Earnings-call customer commentary, 10-Q/10-K customer-concentration disclosures, named design wins, channel/partner announcements, supply-chain databases. Explicitly test each attribution rather than assume.
**Output:** A per-name attribution table (demand source, % of surge, confidence). Confirms/kills the "world-model customer" claim empirically, and defines the *real* demand taxonomy.
**Feeds:** Which demand vector the scanner should key on; prevents building a scanner on a false premise (the VPG lesson).

## Agent 3 — Revenue-Multiplication Sizing ("does the spend dwarf the base?")
**Crux:** Assumption 4 — the actual source of asymmetry. For a candidate supplier, is the addressable incremental spend large vs. its *current* revenue base?
**Method:** For each supply-chain node, estimate content-per-unit (e.g., $ of force/torque sensors per humanoid) × plausible unit-volume ramp scenarios (bear/base/bull), divided by the incumbent supplier's current revenue in that segment. Flag only nodes where a credible scenario yields >2–3x revenue on the exposed segment.
**Output:** Ranked list of supply-chain *nodes* (not yet names) by revenue-multiplication potential, with the unit-economics math and the scenario that has to be true.
**Feeds:** The screen's core filter — separates "marginal bump" names from genuine "revenue multiplies" names.

## Agent 4 — Red Team / Disconfirmation ("try to kill it")
**Crux:** Intellectual honesty gate. Actively argue the thesis is wrong before we spend on it.
**Method:** Marshal the strongest bear case for each pillar: synthetic data collapses physical-data-hardware demand; spend concentrates in mega-caps; the move is already priced (VPG at 270x, above target); momentum/narrative risk; funding-cycle slippage pushes capex out; humanoid ramp disappoints (prototype ≠ production); Nvidia vertical-integrates the sensing/sim layer and disintermediates suppliers.
**Output:** A ranked list of thesis-killers with the evidence for each, and — critically — the *observable* that would confirm or refute each one. What would have to be false for us to lose.
**Feeds:** The go/no-go gate + the monitoring dashboard (Agent below reuses these observables).

## Agent 5 — Supply-Chain Map + Investable Universe ("build the board")
**Crux:** Assumption 2 (predictability) operationalized. Enumerate the full bill-of-materials for world-model + physical-AI buildout, and every public supplier per node, tagged by re-rating status.
**Method:** Node taxonomy (compute, memory/HBM, optics/interconnect, power/cooling, force/torque sensors, tactile, IMU/MEMS, actuators/reducers, cameras/lidar, motion-capture/teleoperation, sim software). Populate public names per node; tag each: already-run / partially-run / not-moved; note where the only players are private (a gap, not a buy).
**Output:** The full investable board with a "not-yet-moved but logically exposed" shortlist (early candidates: Novanta/ATI force-torque, Cognex vision, ADI IMUs, Harmonic Drive/Nabtesco reducers, plus laggard nodes).
**Feeds:** The scanner's universe definition.

## Agent 6 — Leading Indicators / Watchability ("make it deterministic")
**Crux:** Assumption 2 — the user's requirement that the thesis be *verifiable and watchable*, and that re-rating is triggered deterministically by reported earnings/order signals.
**Method:** Define the leading-indicator set that preceded the moves we've already seen (book-to-bill inflection, backlog step-change, first named design win, guidance raise, index inclusion), and the *upstream* signals (lab capex announcements, robot production milestones, cloud-capacity deals). Establish the typical lag from signal → stock move.
**Output:** A monitoring spec: for each candidate, the exact metric + threshold + data source + cadence that would flag "pre-explosion." This is what makes it a *watchable* thesis rather than a one-shot bet.
**Feeds:** The scanner's trigger logic + an ongoing monitoring dashboard.

---

## How they compose
- **Kill-or-confirm first (parallel):** Agents 1, 2, 4 run together — they can independently sink the thesis. Agent 3 (sizing) runs alongside using their outputs where available.
- **Gate:** If 1/2/3/4 survive, run Agents 5 + 6 to build the universe and trigger logic.
- **Only then** commit compute to the full scanner + name-level deep diligence.

## Open scope question for the user (blocks final design)
Do we vet **Thesis A** (world-model *labs* as the demand engine — the literal thesis, evidence weak) or reframe to **Thesis B** (physical-AI / humanoid + compute buildout, labs as one input — evidence strong but more crowded), or run both and let attribution data decide? This changes the framing of Agents 1, 2, and 5.
