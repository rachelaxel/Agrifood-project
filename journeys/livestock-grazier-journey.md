# Journey: Livestock Grazier — Beef/Sheep (Prototype)

> **Status: Hypothesis draft**, companion to
> `personas/livestock-grazier.md`. Grounded where noted by sources in
> `research/sources.md`, but not yet interview-validated. Follow the same
> journey spine as `journeys/horticulture-tree-crop-journey.md` for
> cross-commodity comparability, per `README.md`.

## Purpose

Same as the horticulture journey file: describe current-state reality only.
AI opportunities and workflows live in `opportunities/` and `workflow/`.

## The journey spine, instantiated for this persona

```
PLAN
  - Season/year plan around joining, weaning, marking, shearing, sale
    timing, set against expected feed/season outlook. `[VALIDATE]` how
    formal vs. informal this is, and how far ahead it's actually set given
    beef/sheep income volatility (see persona economics section).
  ↓
MONITOR CONDITIONS
  - Regular stock and pasture checks (vehicle/horseback/drone), observing
    stock condition and behaviour, water point levels, fence integrity,
    pasture cover/growth stage, signs of illness/injury/predation.
    `[VALIDATE]` frequency — plausibly ranges from daily (small finishing
    block) to multi-day rotation (large rangeland property), unlike the
    horticulture persona's more consistent daily-walk pattern.
  ↓
MAKE PRODUCTION DECISIONS
  - Pattern-based judgement on stock condition against experience/season
    ("this mob looks lighter than usual for this time of year") — same
    structure as the horticulture persona's block pattern-matching, but
    applied to a mobile, living asset rather than a fixed block.
  - Reactive decisions: move stock between paddocks, treat an animal,
    adjust supplementary feeding, call a vet/agent.
  ↓
PROCURE INPUTS
  - Supplementary feed, animal health products, water infrastructure
    maintenance. `[VALIDATE]` — procurement behaviour not yet mapped;
    feed procurement in a dry season is plausibly a much higher-stakes,
    higher-uncertainty version of this stage than the horticulture
    persona's routine input buying.
  ↓
MANAGE LABOUR/EQUIPMENT
  - Family labour plus contract musterers/shearers at peak events.
    `[VALIDATE]` on equipment-failure behaviour (vehicles, yards, water
    infrastructure) specifically.
  ↓
HARVEST  (→ muster/weighing/marking/shearing, the closest equivalent to
           horticulture's "harvest" stage)
  - Periodic, labour-intensive, weather- and contractor-dependent events.
    `[VALIDATE]` how timing decisions are actually made.
  ↓
SELL/OUTPUT
  - Sale timing and channel decision (saleyard, over-the-hook, direct to
    feedlot/processor, store vs. finished) — heavily influenced by season,
    feed availability, and market price signals. Given the income
    volatility noted in the persona file, this is hypothesised as the
    single highest-stakes recurring decision in the year — a materially
    different risk profile to the horticulture persona's sell stage, which
    is more constrained by a packing-shed relationship and quality specs
    than by open market-timing choice. `[VALIDATE]`.
  ↓
MANAGE FINANCE/COMPLIANCE
  - NLIS (National Livestock Identification System) movement records are
    mandatory regardless of the grower's own preference — unlike
    horticulture, where compliance records are the *only* structured
    data that exists, this persona likely already has some structured
    digital data trail purely from regulation. `[VALIDATE]` whether that
    data is used for anything beyond minimum compliance.
  ↓
REVIEW & PLAN NEXT SEASON
  - `[VALIDATE]` — informal seasonal review hypothesised, similar to
    horticulture, but should be tested for whether MLA's structured group
    extension model (BeefUp/MeatUp forums, Producer Demonstration Sites)
    creates a more structured review/learning mechanism than horticulture
    growers get from an individual agronomist relationship.
```

Advisor/vet/agent involvement is hypothesised as **more distributed** than
horticulture's single recurring agronomist: a vet for animal health, a
stock agent for sale decisions, and structured group extension (MLA's
EDGEnetwork, BeefUp/MeatUp, Profitable Grazing Systems) for general
practice knowledge — see `research/sources.md` and the persona file's
"Where the advisor/vet/agent gets involved" section. This is the single
biggest structural hypothesis to validate against horticulture: **is there
a "the agronomist" equivalent for this persona, or not?**

## Friction & opportunity map

| Journey stage | Farmer problem | Current behaviour |
|---|---|---|
| Monitor conditions | Harder to hold a reliable "normal" baseline in memory for a mobile mob across large/variable land than for a fixed block | Regular checks by vehicle/horseback/drone, pattern-matched from experience |
| Plan → advice | No single recurring, property-specific advisor relationship (hypothesised) — general practice knowledge comes from group extension, not a walk-the-property visit | Structured group learning (EDGEnetwork, BeefUp/MeatUp forums) rather than one-on-one visits |
| Procure inputs (feed, in a dry season) | High uncertainty on feed availability/price exactly when it matters most, and no structured record of the grazier's own feed position to reason from | **Simulated signal** (see `research/interviews/livestock-grazier-simulated-01.md`, not confirmed): grazier described "ringing five different contacts trying to find anything within cartage distance" in a dry run, with the price moving against him twice while he searched — and separately, holds his own paddock's feed position ("do I have six weeks of feed") in his head with no record to check it against |
| Sell/output | Sale timing/channel decision under real income-volatility stakes, tangled together with a feed-availability decision the grower is holding simultaneously (simulated-interview signal — see `research/interviews/livestock-grazier-simulated-01.md`) | Checks saleyard reports and calls the stock agent, but reported losing track of the feed question while working the market question, and vice versa (simulated, not confirmed) |
| Manage finance/compliance | NLIS data exists from regulatory requirement but may be pure box-ticking, disconnected from day-to-day decisions | Compliance recording done to the minimum required, not used operationally (hypothesised) |
| Review & plan next season | `[VALIDATE]` — may or may not be more structured than horticulture's informal review, given MLA's group-extension model |

This table is more heavily `[VALIDATE]`-tagged than the horticulture
journey's friction table — appropriate, since this persona is one
research pass behind horticulture. Priority for the first livestock
interviews should be confirming or correcting rows above, not generating
opportunity cards from unvalidated guesses.

## Next steps to validate this map

1. Run interviews using `research/interview-guide.md`, adding
   livestock-specific prompts (see the persona file's "open questions")
   before using it — the current guide's stage prompts (Plan, Monitor,
   Procure, etc.) are commodity-neutral and reusable, but the "Core
   interview: walk through yesterday" opener should surface whatever
   idiosyncrasies this persona has (mob movement, water checks, etc.)
   naturally.
2. Resolve whether specialist beef, specialist sheep, and mixed
   cattle/sheep operations need separate personas/journeys, the way
   horticulture's multi-crop finding suggested tree-crop growers often
   aren't single-commodity either.
3. Directly test the "no single trusted advisor" hypothesis — this is the
   most consequential unanswered question for opportunity design, since
   it determines whether the AI framing here is "extend a human
   relationship" (as in horticulture) or "personalise generic extension
   content to this specific property" (a materially different AI
   opportunity shape).

## Sources

See `research/sources.md`. Directly relevant here: ABARES Financial
performance of livestock farms (income volatility, farm counts); MLA
Producer Adoption R&D and Digital Agriculture programs (extension/group-
learning adoption model); commercial grazing decision-support tools as an
unconfirmed secondary signal of existing scattered-data-source behaviour.
