# Persona: Horticulture Tree-Crop Grower (Prototype)

> **Status: Hypothesis draft.** Built from domain knowledge, the framing in
> `README.md`, and the sources logged in `research/sources.md`, but not yet
> validated against a real grower interview. Every claim below should be
> tested and corrected against 2-3 actual interviews before this is treated
> as reliable. Sections still resting on domain-knowledge guesswork (no
> external source behind them) are flagged inline with `[VALIDATE]`; sections
> that now cite a source are grounded but still not interview-tested.

## Snapshot

- **Commodity / production system**: perennial tree crop — almonds, citrus, or
  wine grapes (pick one region/crop for the pilot interviews; almonds in the
  Riverina/Sunraysia or citrus in the Riverland are reasonable starting points
  given scale and existing agronomy support networks). Almonds are a
  reasonable pilot choice on current scale alone: national almond production
  was valued at ~$1.3B in 2024-25, up 19.6% on the prior year (ABS, see
  `research/sources.md`).
- **Typical farm size**: family-owned, 50–500 ha under trellis/orchard, often
  with a mix of owned and leased blocks of different ages. `[VALIDATE]` —
  no source pinned down yet for a typical hectare range specifically; ABARES
  farm survey data (see sources log) should give an actual distribution
  rather than this estimate.
- **Region**: irrigated inland horticulture belt (MIA, Sunraysia, Riverland).
- **Multi-crop reality**: don't assume a single-commodity grower — ABARES
  data on the Murray-Darling Basin found ~86% of grape-growing farms carried
  3+ crops, most commonly wine grapes + citrus + one other horticulture crop
  (ABARES, 2014-15 figures — dated, but the diversification pattern itself
  is a real finding worth testing directly rather than a guess). This
  persona should probably be reframed as "irrigated tree/vine crop grower"
  running more than one commodity, not a single-crop specialist.
- **Structure**: owner-operator plus 1–3 permanent staff, seasonal labour at
  pruning/harvest, contracted agronomist (visits every 2–6 weeks depending on
  season), possible packing-shed/marketer relationship for output.
  `[VALIDATE]` — staffing structure and visit cadence are still domain-
  knowledge estimates, not sourced.

## A day in the life (hypothesised observation → decision → action loop)

1. **Morning paddock/orchard walk** — visual inspection of canopy, fruit set,
   irrigation lines, pest/disease signs. This is observational, not
   instrumented: the grower is pattern-matching against "how this block
   normally looks at this time of year."
2. **Phone calls** — to irrigation contractor, packing shed, casual labour
   coordinator, sometimes the agronomist for a quick check. `[VALIDATE]`
   whether this happens before or after the walk, and how many calls/day is
   typical.
   Adjacent finding worth testing directly: a QUT case study of a Darling
   Downs cotton farm found farmers rated **agronomists as their most
   trusted information source**, ahead of tech vendors or dashboards, and
   that both farmers and agronomists reported being "drowning in apps and
   data" with no good way to combine disparate sources into something
   actionable (QUT, see `research/sources.md`) — i.e. the phone call to the
   agronomist may function as the grower's actual synthesis step today.
3. **Reactive decisions** — irrigation scheduling adjustments, spot spraying,
   labour allocation for the day, based on what was observed that morning
   plus a mental model of the season so far.
4. **Record-keeping** — often minimal and informal: notes on paper, a phone
   note, or nothing beyond memory, except where required for compliance
   (chemical use records, food safety/quality assurance schemes like
   Freshcare or SQF). `[VALIDATE]` — this is the single highest-value thing
   to confirm, since it determines whether there's any existing structured
   data to build on.
5. **Agronomist visit (periodic)** — walks the block with the grower,
   diagnoses issues, leaves a written or verbal plan (nutrition program,
   spray schedule, irrigation recommendation). The grower's actual
   follow-through on this plan is inconsistent — not from disagreement, but
   because the plan doesn't map cleanly onto the grower's day-to-day
   decision loop above.
6. **End-of-season review** — informal, often just "did this block perform
   well or not," rarely tied back systematically to what was recommended vs.
   what was actually done.

## Jobs-to-be-done

- Keep trees/vines alive, healthy, and producing at expected yield and quality
  grade this season.
- Protect a 15–25 year capital investment (rootstock, trellis, irrigation
  infrastructure) against long-term degradation (salinity, disease,
  root health) while making short-term survival decisions.
- Hit packing-shed/marketer quality specs to secure price.
- Manage water allocation and cost — often the single biggest variable input
  cost and risk.
- Reduce reliance on memory/gut-feel as the grower ages or as the operation
  scales, without giving up the pattern-recognition skill that took years to
  build.

## Pain points where advice fails to convert to action

- The agronomist's plan is comprehensive but arrives as a document/verbal
  summary disconnected from the grower's actual daily workflow (the walk +
  phone calls above) — there's no natural point in the day where the grower
  is prompted to check "am I on track with the plan?"
- Record-keeping is not structured enough to let the grower (or an
  agronomist) see season-over-season patterns without manual effort.
- Multiple blocks of different ages/varieties compound complexity — a
  generic recommendation doesn't account for the grower's mental model of
  "block 4 always behaves differently to block 7."
- Financial pressure pushes attention toward this week's cash flow
  (harvest, labour cost, water bill) over the agronomist's longer-horizon
  recommendations (rootstock health, soil amendment programs).

## Decision-making style

Primarily observational and pattern-based, built from years of walking the
same blocks. Analytical only when forced (compliance records, bank/finance
reporting, packing-shed quality data). Risk appetite is generally
conservative on capital decisions (replanting, new varieties) and more
reactive/tactical on day-to-day inputs (irrigation, spray timing).

## Trust triggers

- A system that references the *specific block's* history, not a generic
  regional model.
- Being shown the "why" behind a recommendation in observational terms
  (matches what a good agronomist would say on a walk), not a black-box
  score.
- Low time cost to interact — ideally fits inside the existing walk/phone
  routine rather than requiring a new app session.
- Endorsement or use by their existing agronomist, rather than being sold as
  a replacement for that relationship — grounded, not just hypothesised:
  agronomists were the single most trusted information source in the QUT
  Darling Downs study (see `research/sources.md`), so a system positioned
  as competing with that relationship starts from a trust deficit.

## Rejection triggers

- Generic advice that ignores known block-level variation.
- Anything that reads as "another platform to log into and enter data."
- Recommendations that don't map to an achievable action given current
  cash-flow/labour constraints — i.e., ignoring the economics.
- Loss of control/authorship over the decision — being told what to do
  rather than being given information to decide with.

## Language and framing

Resonates: "block," "this season vs. last season," "walk," "what the
agronomist would look for," concrete and observational.
Alienates: "model confidence," "optimize," "platform," abstract
data-science language without a concrete action attached.

## Farm economics snapshot

- **Grounded anchor (dated — needs refresh):** ABARES reported average farm
  cash income for irrigated horticulture farms in the Murray-Darling Basin
  at ~$105,800 in 2014-15, rising ~15% to ~$122,000 in 2015-16; only ~16% of
  horticulture farms achieved a rate of return above 10% in 2015-16, and
  those were mostly larger, multi-crop operations spanning citrus, wine
  grapes, stone fruit, pome fruit and almonds (ABARES, see
  `research/sources.md`). These figures are over a decade old — treat as an
  order-of-magnitude anchor only, not a current number, and prioritise
  pulling a recent ABARES horticulture survey release before this goes into
  any real economics model.
- Water is typically the largest controllable variable cost; margin is highly
  sensitive to water price and allocation in a given season. `[VALIDATE]` —
  plausible from domain knowledge, not yet backed by a specific figure.
- Labour (permanent + seasonal at harvest/pruning) is the second major cost
  and a persistent availability risk. `[VALIDATE]`
- Cash-flow is highly seasonal (concentrated around harvest/sale), so any
  adoption cost incurred outside that window competes with tight off-season
  cash. `[VALIDATE]`
- Capital decisions (replant, irrigation upgrade) are financed over many
  years; the grower is used to thinking in multi-year payback, but day-to-day
  tools need to justify themselves within a season. `[VALIDATE]`
- The named top-three barriers to agtech adoption in Australia generally
  (not horticulture-specific) are agritech performance, producer digital
  capability/capacity, and **return on investment** (AgriFutures Producer
  Technology Uptake Program, see `research/sources.md`) — supporting the
  README's insistence that economics modelling is core to this project, not
  a bolt-on. Corroborated globally: McKinsey's global farmer survey finds
  unclear ROI and high implementation/maintenance cost are the top-cited
  agtech adoption barriers (North America: 52% cite cost, 40% cite unclear
  ROI), with ease-of-use and data-sharing trust as secondary barriers (see
  `research/sources.md`).

## Where the agronomist gets involved

Periodic scheduled visits (every 2–6 weeks in-season), plus ad hoc phone
calls when the grower notices something concerning on the morning walk. The
agronomist is the primary trusted analytical voice; any AI layer likely needs
to position itself as extending or supporting that relationship (per
README task #6), not competing with it.

## Open questions for real interviews

1. What, if anything, does this grower currently record digitally vs. on
   paper vs. not at all?
2. How much of the phone-call activity is actually agronomist contact vs.
   logistics/labour/market calls?
3. What was the last piece of agronomist advice they didn't follow through
   on, and why?
4. What would need to be true for them to trust a system's read on "this
   block isn't performing like it normally does"?
5. What's the real dollar/time cost of their current workflow that an AI
   layer would need to beat?

## Sources

See `research/sources.md` for full entries. Directly used here:
AgriFutures Producer Technology Uptake Program (adoption barriers); ABARES
horticulture farm survey program and Murray-Darling Basin grape farm data
(farm economics, multi-crop diversification); ABS Australian Agriculture:
Horticulture 2024-25 (almond sector scale). Hort Innovation's almond
industry innovation and adoption program (AL16001/AL19001/AL22001) and the
QUT human-factors AgTech case study are logged as priority follow-up reads
— they likely contain grower-level qualitative findings that should replace
several `[VALIDATE]` tags above once reviewed.
