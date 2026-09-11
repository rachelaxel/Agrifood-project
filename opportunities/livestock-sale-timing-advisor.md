# AI Opportunity Card — Sale Timing & Channel Advisor

**Opportunity name**: Sale timing and channel decision support

**Persona**: `personas/livestock-grazier.md`

**Journey stage**: Sell/output

**Problem** (from `journeys/livestock-grazier-journey.md` friction table):
Sale timing/channel decision (saleyard, over-the-hook, direct to
feedlot/processor, store vs. finished) carries real income-volatility
stakes for this persona — ABARES data shows beef farm cash income swinging
from $238,000 (2022-23) down substantially in the following drought/low-
price year (see `research/sources.md`) — without necessarily having clear,
synthesised market-timing signals to act on.

**Current behaviour** (hypothesised — `[VALIDATE]`): Grower checks several
separate sources (stock agent, saleyard reports, weather/season outlook,
neighbour conversations) and makes a judgement call, likely under time
pressure if feed is running out or an agent's window is closing. **Now
partly grounded** (see `research/sources.md`): the market-data half of
this isn't actually fragmented at the source — MLA's National Livestock
Reporting Service already centrally collects and publishes current
saleyard/price data across ~70 markets/week with an interactive online
tool. This shifts the real opportunity away from "aggregate scattered
market sources" and toward **combining that already-good market feed with
the grower's own feed/condition data**, which nothing currently does
(reframes the AI intervention below accordingly). Separately, CSIRO
drought-resilience research found producer destocking decisions are driven
more by local knowledge/pragmatism than structured data, with a documented
tendency to rely on drought subsidies over proactive destocking — a
sourced version of the "decided from the gut under pressure" pattern this
card was already designed around.

**AI intervention**: *Predict* + *summarise* + *recommend*. Combine
current stock condition/weight trajectory (from the grazier's own
monitoring), local feed/season outlook, and market price signals across
channels into a synthesised view of "sell now vs. hold," with reasoning
shown, not just a number.

**Workflow intervention**: Lower complexity than a diagnostic escalation
case — this is a standing decision-support view the grower checks
periodically (likely weekly-to-fortnightly as a sale window approaches)
rather than an event-triggered case. No human-in-the-loop escalation logic
needed in the baseline version, since the grower retains the sale decision
entirely; a workflow diagram would only be needed if this evolves into
something that also books/coordinates the sale itself.

**Human role**: Stock agent remains the transaction/negotiation party and
likely a cross-check on the AI's read of the market — this opportunity
supports the grower's own decision, not the agent relationship, and
shouldn't be framed as a replacement for the agent's role.
**Simulated-interview signal** (see
`research/interviews/livestock-grazier-simulated-01.md`, not confirmed):
the stock agent may be the closest thing this persona has to
horticulture's agronomist, but specifically for sale/market matters — so
this opportunity should be framed as *extending the agent relationship*
(similar in spirit to the horticulture pest-detection card's "extends the
agronomist" framing), not as a generic decision-support tool competing
with it. The simulated agent also named a concrete gap worth designing
around directly: **poor visibility into the grazier's own feed position**
when advising on timing — suggesting the AI intervention may need to
combine the grazier's feed/pasture data with market data *for the agent's
benefit as much as the grower's*, not just present a recommendation to the
grower alone.

**Adoption barrier — farmer**: This is arguably the single
highest-stakes, most consequence-loaded decision in the persona's year
(per the economics volatility finding) — a wrong or untrusted
recommendation here is a much bigger deal than a wrong pest-ID
recommendation in the horticulture pest-detection card. Trust bar is
correspondingly high, and `[VALIDATE]`: it's unclear from current sourcing
whether this persona has a single trusted human they'd want any
recommendation cross-checked against (see the unresolved "no single
advisor" hypothesis in the persona/journey files) — if true, this
opportunity may have a weaker trust anchor available than the horticulture
persona's agronomist relationship gives its pest-detection card.

**Adoption mechanism — farmer**: Show reasoning and the underlying data
(condition trend, feed outlook, price signals across channels) rather than
a single recommendation, so the grower can apply their own judgement on
top rather than being asked to trust a black box on the highest-stakes
call of their year; frame explicitly as "here's what the data says," not
"here's what to do."

**Adoption barrier — organisational** (if a livestock advisory body or
MLA-adjacent service operates this): Market/price data licensing and
currency (stale price signals would be actively harmful here, unlike a
slower-moving pest-detection recommendation); who's accountable if a
grower sells at a loss having relied on the tool's read of the market.

**Adoption mechanism — organisational**: Source price/market data directly
from the same channels the grower already checks (saleyard reports,
processor grids) rather than a proprietary model, so the tool's credibility
rests on data currency and synthesis quality, not a novel prediction claim
it would need to prove out over time. Concretely, this means integrating
with MLA's NLRS data (see `research/sources.md`) rather than building a
competing market-data source — MLA/Integrity Systems already carries the
credibility and coverage a new entrant would need years to replicate.
CSIRO's own destocking-tool research program (Future Drought Fund-funded)
is close enough to this card and
`opportunities/livestock-feed-position-tracking.md` that a build-vs-
partner decision with that program specifically should happen before
either card matures past Idea.

**Potential value**:
- Avoiding forced/distressed sales at depressed prices (e.g. drought
  destocking) is plausibly the single largest economic lever available in
  this persona's year, given the income volatility already evidenced.
- Time saved checking multiple disconnected sources.
- `[VALIDATE]` — no figure yet for how much of the beef income volatility
  shown in ABARES data is attributable to sale-timing decisions
  specifically vs. externally-driven price/seasonal conditions the grower
  couldn't have avoided regardless of information quality; this matters
  for how much value to credibly claim for this opportunity.

**Maturity**: Idea. Commercial grazing tools (Grazing Charts, AgriWebb,
Atlas Grazing, Farming Forecaster — see `research/sources.md`) already
address adjacent pasture/feed-budgeting decision support, so there may be
existing products to learn from (or partner with) rather than building
from zero.

**Related opportunity**: the simulated interview suggests the sale-timing
decision and a feed-availability/procurement decision may not be
separable in practice — the grazier reported holding both in his head
simultaneously and losing track of one while working the other. Rather
than expanding this card's own scope, that gap now has its own card —
`opportunities/livestock-feed-position-tracking.md` — designed as an
enabling input into this one (the same "infrastructure card feeds the
higher-value card" pattern as horticulture's observation-capture card
feeding its plan-operationalisation and pest-detection cards). If a real
interview confirms the entanglement, this card's AI intervention should
explicitly consume that card's feed-position estimate rather than treating
feed availability as an external unknown.

**Sources**: ABARES Financial performance of livestock farms (income
volatility grounding the stakes claim); commercial grazing tools as
evidence of adjacent existing products. The core adoption-trust hypothesis
(whether this persona has an equivalent trusted-advisor anchor to
horticulture's agronomist) is `[VALIDATE]` and should be resolved before
this card moves past Idea maturity.
