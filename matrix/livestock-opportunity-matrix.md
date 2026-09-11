# AI Opportunity Matrix — Livestock (Beef/Sheep Grazier)

Rolls up the opportunity cards in `opportunities/` for this persona, per
Step 5 of `research/persona-build-flow.md`. Only one card exists so far —
this persona is one build-flow pass behind horticulture (see the status
table in that file) — but every persona gets a matrix even with a single
row, so it stays comparable once more cards and a second persona's-worth
of maturity exist.

| Opportunity | Journey stage | Farmer value | AI potential | Workflow complexity | Adoption likelihood | Priority |
|---|---|---|---|---|---|---|
| Sale timing & channel advisor | Sell/output | Very high — targets the highest-stakes, most volatile-income decision point identified for this persona | Medium-high (synthesis/prediction across feed, condition, and market data) | Low (standing decision-support view; no case/escalation logic — see the card's own Step 4 reasoning) | Low-medium — highest trust bar of any card across both personas so far, and the "who validates this" anchor is unresolved (see below) | ⭐⭐⭐ |

## Reading this matrix

- **Farmer value is rated very high** because the persona's own economics
  data (ABARES income volatility, see `research/sources.md`) points at
  sale timing as plausibly the single largest lever in this persona's
  year — a stronger economic case than either horticulture card can make
  with sourced data alone.
- **Adoption likelihood is rated lower than any horticulture card**,
  deliberately. Horticulture's two highest-value cards (plan
  operationalisation, pest detection) both have a named, sourced trust
  anchor — the agronomist. This card's simulated-interview signal
  suggests the stock agent is the closest analogue, but only for this
  specific decision, and that's still unconfirmed. A wrong recommendation
  here also has higher stakes (per the persona's income volatility) than
  a wrong pest-ID call. High value with a shakier trust foundation is
  exactly why this card is rated ⭐⭐⭐ on the strength of its value case,
  not because its adoption risk is settled — the matrix intentionally
  doesn't average these into a false middle score.

## Gaps in this matrix (larger than horticulture's, and why)

- Only 1 opportunity card exists for this persona vs. 3 for horticulture.
  The friction table in `journeys/livestock-grazier-journey.md` names
  several more `[VALIDATE]`-tagged rows (feed procurement, NLIS/compliance
  data reuse, review & planning) that don't yet have cards — feed
  procurement in particular was sharpened by the simulated interview
  (see `research/interviews/livestock-grazier-simulated-01.md`) as
  entangled with the sale-timing decision itself, and may be worth a card
  of its own or a scope expansion of the existing one (see that card's
  "Related opportunity" note) rather than being left out.
- No cross-commodity comparison yet — this matrix and horticulture's only
  cover two of the five target personas listed in `README.md`.
- Scores are unvalidated judgement calls, same caveat as the horticulture
  matrix — treat every score above as `[VALIDATE]`.
