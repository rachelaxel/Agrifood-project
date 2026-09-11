# Persona: Horticulture Tree-Crop Grower (Prototype)

> **Status: Hypothesis draft.** Built from domain knowledge and the framing in
> `README.md`, not yet validated against a real grower interview. Every claim
> below should be tested and corrected against 2-3 actual interviews before
> this is treated as reliable. Sections most likely to be wrong on first pass
> are flagged inline with `[VALIDATE]`.

## Snapshot

- **Commodity / production system**: perennial tree crop — almonds, citrus, or
  wine grapes (pick one region/crop for the pilot interviews; almonds in the
  Riverina/Sunraysia or citrus in the Riverland are reasonable starting points
  given scale and existing agronomy support networks).
- **Typical farm size**: family-owned, 50–500 ha under trellis/orchard, often
  with a mix of owned and leased blocks of different ages.
- **Region**: irrigated inland horticulture belt (MIA, Sunraysia, Riverland).
- **Structure**: owner-operator plus 1–3 permanent staff, seasonal labour at
  pruning/harvest, contracted agronomist (visits every 2–6 weeks depending on
  season), possible packing-shed/marketer relationship for output.

## A day in the life (hypothesised observation → decision → action loop)

1. **Morning paddock/orchard walk** — visual inspection of canopy, fruit set,
   irrigation lines, pest/disease signs. This is observational, not
   instrumented: the grower is pattern-matching against "how this block
   normally looks at this time of year."
2. **Phone calls** — to irrigation contractor, packing shed, casual labour
   coordinator, sometimes the agronomist for a quick check. `[VALIDATE]`
   whether this happens before or after the walk, and how many calls/day is
   typical.
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
  a replacement for that relationship.

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

## Farm economics snapshot `[VALIDATE — needs real figures]`

- Water is typically the largest controllable variable cost; margin is highly
  sensitive to water price and allocation in a given season.
- Labour (permanent + seasonal at harvest/pruning) is the second major cost
  and a persistent availability risk.
- Cash-flow is highly seasonal (concentrated around harvest/sale), so any
  adoption cost incurred outside that window competes with tight off-season
  cash.
- Capital decisions (replant, irrigation upgrade) are financed over many
  years; the grower is used to thinking in multi-year payback, but day-to-day
  tools need to justify themselves within a season.

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
