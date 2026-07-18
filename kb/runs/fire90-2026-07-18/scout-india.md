# Scout: India geography — Fire 90 (2026-07-18)

Ring cursor #3. Prior India-focused pass was Fire 67 (2026-07-11, commit 4bb0749,
"India round 9, 13th consecutive [clean-negative]") plus a GreyOrange/Addverb/Midwest
disambiguation note. Task brief claimed "idle ~80 fires" — actual gap per git history
is ~23 fires (Fire 67 -> Fire 90), but still worth a genuinely fresh check since 4
concrete open threads existed (REPM deadline, Midwest/Entellus DRHP, Tonbo listing,
Addverb DRHP). Dedup pass run first against KILL-LIST.md and dead-ends.md (see grep
output below) — no new company here overlaps a killed name.

## 1. REPM (₹7,280cr sintered-magnet scheme) tender status
- Deadline **still not resolved**. Confirmed via multiple sources (PMO release, ANI,
  Angel One, Swarajya, IANS) that MHI extended bid due date to **2026-07-29** (technical
  bids open 2026-07-30) — matches KB's existing note exactly, no further slippage or
  early resolution found.
- No vendor shortlist/allocation announced (expected: scheme allocates capacity to 5
  beneficiaries via global competitive bid on GeM/CPP Portal, decision necessarily
  post-July 30).
- **STILL-IDLE, NO CHANGE.** Do not recheck before ~Aug 2026 (post technical-bid-opening).
  Even a winning bidder would very likely still fail Gate 2 (no named humanoid/AV OEM
  buyer — it's a generic magnet-manufacturing subsidy, not tied to a robotics program)
  per the existing KB reasoning; only relevant if a winning bidder turns out to be an
  *already-listed* small-cap with a robotics story, which none of the known bidders are.

## 2. Midwest Advanced Materials / Entellus Industries — DRHP check
- **Midwest Advanced Materials**: still private. Real business (₹1,000cr 3-yr investment
  plan, Sri Lankan monazite supply, targeting Dec-2026 production start per Business
  Standard 2025-06-08 and Bharat Innovates listing) but **no DRHP found**, no listed
  vehicle. Confirms KB disambiguation note still holds (do not confuse with listed
  Midwest Ltd/MIDWESTLTD granite-quartz co).
- **Entellus Industries**: still private, still tiny (₹50cr / ~$5.5M Series A round,
  Chennai-based, founded 2022, targeting 2,000 tonnes/yr magnet capacity). No DRHP.
  Even if it filed one tomorrow it's presently too early-stage/small to matter.
- **STILL-IDLE, NO CHANGE** on both. Recheck trigger unchanged: actual DRHP filing.

## 3. Tonbo Imaging — listing status + named buyer check
- **Update since last check**: SEBI approved the IPO 2026-06-06; DRHP → RHP progressed;
  subscription window opened and closed **2026-07-04** (100% offer-for-sale, no fresh
  issue, ~1.81cr shares, BRLMs JM Financial + IIFL Capital, registrar KFin). This is
  materially further along than the prior "DRHP filed, no listing date" status.
- Listing date itself is **ambiguous across sources**: some IPO-tracker pages state a
  listing date of 2026-07-06; a live-data portal (finology/ticker) explicitly still
  flags "currently not listed and is under IPO" with placeholder price data. Given the
  conflicting/stale-cache signals, actual live-trading status could not be confirmed
  with confidence in this pass — flagging for a follow-up direct NSE/BSE symbol lookup
  next fire rather than asserting either way.
- **Business/buyer check, unchanged from prior fires**: still a defense electro-optics/
  thermal-imaging OEM-components generalist (weapon sights, missile seekers, fire
  control, UGV/aerial payload imaging cores). Company's own marketing mentions
  "automotive drivers navigating fog" as a use-case class, not a named AV/robotaxi/
  humanoid OEM. **No named robotics or AV-OEM buyer found anywhere** (company site,
  press, IPO prospectus summaries). FY25 revenue ₹469cr; pre-IPO Series-D valuation
  ~₹1,500cr (~$175M), i.e. comfortably under the $500M cap gate — but fails Gate 2
  (named-buyer) and Gate-0 business-model-fit is borderline-pass (sells OEM cores/
  subsystems, is at least a component seller) so this is a **Gate-2 fail**, not
  business-model disqualification.
- **STILL-IDLE, NO CHANGE in verdict** (Gate-2 fail persists) — but log the listing
  progression as a state update so the next scout doesn't re-derive it from scratch.

## 4. Addverb Technologies — DRHP check
- **No DRHP filed.** Instead raised **$100M in an undisclosed round dated 2026-06-10**
  (Reliance/Ambani-backed, ~54% owned), explicitly earmarked for humanoid + quadruped
  robot development, AI systems, and import-substitution of proprietary components.
  Current-year revenue guide ~₹1,300cr (~$150M) on an order book of ~$200M.
  IPO remains explicitly gated on hitting ₹40-50bn revenue, company's own guidance
  ~2 years out.
- **STILL-IDLE, NO CHANGE.** (Also: even once listed, Addverb builds its OWN robots —
  Elixis-W wheeled humanoid — so it would need re-screening against the "not a company
  building its own competing robot" business-model-fit rule; it may end up disqualified
  on Gate-0 rather than qualifying outright even post-DRHP. Worth flagging explicitly
  for whoever picks this up post-listing.)

## 5. Fresh broad BSE/NSE small-cap screen (named Hyundai/Boston Dynamics/humanoid-OEM/
   robotaxi-fleet/world-model buyer)
- Ran multiple broad queries (lidar/radar + humanoid named customer; harmonic-drive/
  actuator manufacturers "listed NSE/BSE robotics"; "robotaxi OR autonomous vehicle
  India component supplier stock 2026 named order").
- Zero India-listed hits with a named humanoid/AV-OEM buyer. Global robotaxi supply-
  chain news (Hesai-Mercedes, Uber-Rivian-Lucid-Nuro, Pony.ai-Chenqi) has literally no
  Indian component-supplier presence in any hit.
- One only-tangential find: xTerra Robotics (IIT Kanpur-incubated quadruped/robot-dog
  startup, SVAN-M2) — UN-WFP warehouse pilot, not humanoid, not AV, no listed vehicle,
  not a BOM-component seller (builds its own end-product robot) — fails business-model-
  fit and is private regardless. Not logging as a new dead-end name (too far off-thesis
  to be worth a KILL-LIST line; noting here only for scout continuity).
- Actuator-manufacturer directory searches returned only generic/aggregator content
  (Stocks Mantra "147 companies, 43 listed" style directory pages) with no specific
  named-buyer story — not independently verifiable, not actionable, did not chase
  further given time-box.

## 6. Sanity check for a genuinely new entrant
- No new entrant surfaced beyond the already-tracked 4 threads (REPM/Midwest-Entellus/
  Tonbo/Addverb) plus the already-logged GreyOrange/Sona-BLW/Bharat-Forge/MTAR/Zen/etc.
  kill set. The structural conclusion from dead-ends.md rounds 5-9 (Indian AV/humanoid
  BOM supply chain is not yet visible in primary filings or credible press — the chain
  remains China/Japan/US/Korea-dominated) is **reconfirmed, not contradicted**, by this
  fresh pass.

## Dedup grep run (pre-check, before any candidate reported)
- `grep -i` for: Tonbo, Addverb, Midwest, Entellus, REPM, Sona, Bharat Forge, GreyOrange,
  MTAR, Zen Technologies, Craftsman, Paras, Centum, Motherson, Cyient, Azad, Kaynes,
  Syrma, Suprajit, xTerra — all either already present in KILL-LIST.md/dead-ends.md or
  (xTerra) newly checked-and-rejected in this pass, not previously logged and not now
  promoted.

## Overall recommendation
India stays **IDLE**, cadence unchanged. No promote, no new WATCH, no new KILL-LIST
entries needed (nothing here is new enough to be worth a formal KILL-LIST line — these
are all re-confirmations of already-logged dead-end threads). Only two things could flip
this: (a) REPM technical-bid outcome / vendor shortlist post 2026-07-30, if a winner
turns out to already be a listed small-cap with a plausible robotics story (currently
looks unlikely — known bidders are large diversified miners/magnet-only plays); (b) a
definitive Tonbo Imaging live-trading confirmation plus discovery of an actual named
AV/robotics buyer in its RHP/prospectus disclosures (not yet found, RHP financial/
customer-concentration tables not pulled in this pass — could be worth one direct pull
of the RHP itself next time, since IPO prospectuses often disclose top-customer tables
that press coverage omits).
