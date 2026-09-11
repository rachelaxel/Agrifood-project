# Persona: Livestock Grazier — Beef/Sheep (Prototype)

> **Status: Hypothesis draft.** Built from domain knowledge, the framing in
> `README.md`, and the sources logged in `research/sources.md`, but not yet
> validated against a real grower interview. Sections still resting on
> domain-knowledge guesswork are flagged `[VALIDATE]`; sections that cite a
> source are grounded but still not interview-tested. Use
> `research/interview-guide.md` (livestock-specific prompts should be added
> to it once the first interview happens) to correct this file.

## Snapshot

- **Commodity / production system**: extensive beef cattle and/or sheep
  grazing (specialist beef, specialist sheep, or mixed cattle/sheep — all
  three are common enough to be worth deciding on before running
  interviews). ABARES counted 22,100 specialist beef, 8,900 specialist
  sheep, and 3,000 mixed cattle/sheep broadacre farms nationally in
  2022-23 (see `research/sources.md`) — specialist beef is the largest
  single group, so it's the reasonable pilot choice within this persona
  unless there's a reason to prioritise sheep or mixed.
- **Typical farm size**: `[VALIDATE]` — no hectare figure sourced yet;
  extensive grazing properties vary enormously by region (higher-rainfall
  finishing country vs. large rangeland breeding country), so a single
  "typical size" is likely the wrong framing — this may need a
  region/production-system split similar to how the horticulture persona
  splits by crop.
- **Region**: not commodity-specific in the way horticulture is tied to
  irrigation districts — beef and sheep grazing spans most of Australia's
  agricultural land. `[VALIDATE]` — needs a decision on which region(s) to
  pilot interviews in (e.g. northern beef breeding country vs. southern
  mixed farming/grazing zones behave very differently).
- **Structure**: owner-operator, often with family labour, plus contract
  musterers/shearers/contractors at peak times (weaning, marking,
  shearing, sales). `[VALIDATE]` — staffing pattern is a domain-knowledge
  estimate, not sourced.
- **Financial profile (grounded, current)**: average farm cash income for
  beef cattle producers was $238,000 in 2022-23 (a strong year), but beef
  income is **highly volatile year to year** — it fell substantially in
  2023-24 on drought and lower cattle prices before recovering in
  2024-25, with the 3-year average to 2024-25 sitting just below the
  longer-term average of $155,300. Average equity ratio 94%, average farm
  cash debt ~$570,000 against average liquid assets ~$247,000. Sheep
  producers had the highest equity ratio of any surveyed farm type (95%)
  and the lowest business debt (~$329,000) (ABARES, see
  `research/sources.md`). This income volatility is likely a bigger
  factor in this persona's decision-making and risk appetite than
  anything comparable in the horticulture persona, where multi-crop
  diversification smooths income more.

## A day in the life (hypothesised observation → decision → action loop)

1. **Daily/regular stock and pasture check** — by vehicle, on horseback, or
   increasingly via ute-mounted or drone/camera checks on larger
   properties. Observing: stock condition and behaviour, water point
   levels, fence integrity, pasture cover/growth stage, signs of
   illness/injury/predation. `[VALIDATE]` — frequency almost certainly
   varies hugely by property size (daily on a small finishing block vs.
   multi-day rotation on a large rangeland property).
2. **Phone/radio calls** — to contractors, neighbours, stock agents, vet,
   sometimes an advisor. `[VALIDATE]` cadence and typical content.
3. **Reactive decisions** — moving stock between paddocks, treating an
   animal, adjusting supplementary feeding, calling a vet or agent.
   Decisions are pattern-based: "this mob looks lighter than usual for
   this time of year," compared against experience rather than a
   recorded baseline — directly analogous to the horticulture persona's
   "normal for this block" pattern-matching, but applied to a mobile,
   living asset instead of a fixed block.
4. **Record-keeping**: mandatory National Livestock Identification System
   (NLIS) movement records exist regardless of the grower's own
   preference, so — unlike horticulture, where compliance records are the
   *only* structured data — there is likely already some structured
   digital data trail here purely from regulatory requirement.
   `[VALIDATE]` whether the grower actually uses that NLIS data for
   anything beyond the minimum compliance requirement, or whether it's
   pure box-ticking disconnected from day-to-day decisions.
5. **Advisor/vet involvement (periodic, likely less frequent than
   horticulture's agronomist cadence)**: `[VALIDATE]` — MLA's adoption
   model is built around structured group extension (Profitable Grazing
   Systems, EDGEnetwork, BeefUp/MeatUp forums; see
   `research/sources.md`) rather than the recurring one-on-one
   agronomist-walks-the-block relationship the horticulture persona has.
   If confirmed in interviews, this is a significant structural
   difference: the "AI extends the agronomist" framing from the
   horticulture persona may need to become "AI extends the
   advisor/extension network" here, since there may be no single trusted
   individual playing the same role.
6. **Muster/weighing/marking/shearing events**: periodic, labour-intensive,
   heavily logistics-dependent (contractors, weather, yard/shed
   capacity). `[VALIDATE]` decision process for timing these.
7. **Sale decisions**: when and where to sell (saleyard, over-the-hook,
   direct to feedlot/processor, store vs. finished), heavily influenced by
   season, feed availability, and market price signals. `[VALIDATE]` —
   likely a high-stakes, infrequent decision point analogous to the
   horticulture persona's harvest/sell stage but with more optionality on
   timing and channel.

## Jobs-to-be-done

- Keep livestock alive, healthy, and in acceptable condition given
  seasonal feed/water availability.
- Manage pasture/paddock condition as a long-term asset (ground cover,
  species composition, erosion risk) while making short-term stocking
  decisions — the same long-horizon-investment-vs-immediate-survival
  tension named in this persona's horticulture counterpart, but the asset
  being protected is land/pasture condition rather than rootstock/trellis
  infrastructure.
- Time sales to the market and season rather than being forced to sell
  under duress (e.g. destocking in drought at depressed prices) — given
  the income volatility noted above, this is plausibly the single highest-
  stakes recurring decision in this persona's year. `[VALIDATE]`.
- Manage a mobile, living asset across (often) a much larger and more
  variable-condition land area than a horticulture block, with less
  ability to directly instrument every animal individually.
- Meet regulatory/compliance obligations (NLIS, biosecurity) with minimum
  friction.

## Pain points where advice fails to convert to action

- `[VALIDATE]` — this section is the least grounded of the persona so far
  and should be a top priority in interviews. Hypotheses to test:
  - Extension/group learning (MLA's model) may deliver good general
    practice knowledge but, unlike a one-on-one agronomist visit, may not
    translate into a specific, property-level plan the way the
    horticulture persona's agronomist relationship does — worth directly
    testing whether this persona experiences the same "plan → daily loop"
    gap, or a different failure mode entirely (e.g. "I know the general
    principle but not how it applies to my specific paddock/season").
  - Commercial grazing software (Grazing Charts, AgriWebb, Atlas Grazing,
    Farming Forecaster — see `research/sources.md`) already exists and is
    marketed on consolidating scattered data sources, which may mean this
    persona has already been sold (and possibly already rejected or
    partially adopted) more standalone software than the horticulture
    persona has — worth asking directly what's been tried and dropped.

## Decision-making style

Hypothesised as pattern/observation-based, similar to the horticulture
persona, but applied to mobile livestock and often larger, more variable
land areas — meaning the "baseline" being pattern-matched against may be
harder to hold in memory reliably (a mob's condition across a large
paddock vs. a fixed block's visual state). `[VALIDATE]` whether this makes
graziers more or less receptive to instrumented/recorded baselines than
the horticulture persona.

## Trust triggers `[VALIDATE — none of this section is sourced yet]`

- Likely similar to horticulture: property-specific rather than generic
  regional advice, low time cost, fitting existing habits (ute/phone use
  in the paddock), and an identifiable trusted human validator — though
  who that validator is (vet? agent? extension officer? no single person?)
  needs confirming, since MLA's model suggests it may not be a single
  recurring relationship the way the horticulture agronomist is.

## Rejection triggers `[VALIDATE]`

- Hypothesised, by analogy with horticulture: generic advice ignoring
  property-specific conditions; "another platform to log into," especially
  if this persona has already tried and abandoned grazing-management
  software; anything that reduces perceived control over livestock
  welfare decisions, which likely carry more emotional/animal-welfare
  weight than a pest/disease call on a tree crop.

## Language and framing `[VALIDATE]`

Hypothesised to resonate: "mob," "condition," "season," "paddock," concrete
and observational, similar register to horticulture's "block"/"walk"
language but centred on livestock condition and seasonal feed outlook
rather than plant/soil state.

## Farm economics snapshot

- **Grounded, current:** average farm cash income for beef cattle
  producers was $238,000 in 2022-23, average equity ratio 94%, average
  farm cash debt ~$570,000 against average liquid assets ~$247,000; sheep
  producers had a 95% equity ratio and ~$329,000 average business debt —
  both are in a much stronger equity position on average than the
  horticulture persona's `[VALIDATE]`-tagged, decade-old economics
  snapshot (ABARES, see `research/sources.md`).
- **Volatility is the defining feature, not the average**: beef incomes
  fell substantially in 2023-24 before recovering in 2024-25, with the
  3-year average sitting just below the longer-term average — any
  adoption-cost model for this persona needs to account for a farmer
  whose income in a bad year can be a fraction of a good year, unlike the
  horticulture persona's comparatively steadier (if still seasonal)
  cash-flow rhythm.
- Feed and water availability (rainfall-dependent) are likely the
  dominant variable "input cost" equivalent — largely uncontrollable,
  unlike horticulture's irrigation water which is at least partly a
  purchased/allocated input. `[VALIDATE]`.
- The same top-three national adoption barriers (agritech performance,
  producer digital capability, ROI — AgriFutures PTUP) and the McKinsey
  global finding on unclear ROI/high cost as top adoption barriers (see
  `research/sources.md`) should be assumed to apply here too unless
  interviews say otherwise — these weren't commodity-specific findings.

## Where the advisor/vet/agent gets involved

Likely more distributed than the horticulture persona's single recurring
agronomist relationship: a vet for animal health issues, a stock agent for
sale decisions and market information, and structured group
extension/training (MLA's EDGEnetwork, BeefUp/MeatUp forums, Producer
Demonstration Sites) for general practice knowledge, rather than one
person who "knows this property." `[VALIDATE]` directly — if true, this
changes where an AI layer would sit relative to the horticulture persona:
there may be no single human relationship to extend, but rather a need to
aggregate/personalise generic extension content to the specific property,
which is a different kind of AI opportunity (interpretation/personalisation
of general knowledge) than the horticulture persona's
"extend-the-agronomist" framing.

**Simulated-interview signal (not confirmed — see
`research/interviews/livestock-grazier-simulated-01.md`, Simulated/synthetic
tier):** the distributed-advisor hypothesis held up, but with the **stock
agent as the closest single analogue**, specifically for sale-timing
decisions — vet for animal health, group extension for general practice,
agent for anything market/sale-related, no one role covering all of it.
The simulated agent also named a concrete gap: poor visibility into the
grazier's actual feed position when advising on sale timing. Still needs a
real interview to confirm or overturn — a different real grazier could
easily name a vet, accountant, or neighbour instead.

## Open questions for real interviews

1. Who is this grazier's most trusted source of property-specific advice
   (if anyone) — vet, agent, neighbour, extension officer — and how often
   do they actually speak?
2. What grazing/livestock software (if any) have they tried, and what
   made them keep using it or drop it?
3. Walk through the last time they made a sale timing decision — what
   information did they use, and what would have made them more
   confident?
4. How is NLIS/compliance record-keeping actually used day to day, if at
   all, beyond the minimum requirement?
5. What was the last drought/dry-season decision (destock, feed, hold)
   that stands out as the hardest call of the year, and how was it made?
6. How does the answer to any of the above change between a specialist
   beef, specialist sheep, and mixed operation — is one persona actually
   enough, or does this need to split the way horticulture's multi-crop
   finding suggested?

## Sources

See `research/sources.md` for full entries. Directly used here: ABARES
Financial performance of livestock farms (farm counts by type, income and
equity figures, volatility); MLA Producer Adoption R&D and Digital
Agriculture programs (extension/group-learning adoption model, distinct
from horticulture's one-on-one agronomist model); commercial grazing
decision-support tools (Grazing Charts, AgriWebb, Atlas Grazing, Farming
Forecaster) as a secondary signal of existing scattered-data-source
behaviour, not yet interview-confirmed. AgriFutures PTUP and McKinsey
global farmer survey findings (cited in the horticulture persona) are
carried over here as general, non-commodity-specific adoption barriers.
