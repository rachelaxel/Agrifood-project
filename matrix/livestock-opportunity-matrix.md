# AI Opportunity Matrix — Livestock (Beef/Sheep Grazier)

Rolls up the opportunity cards in `opportunities/` for this persona, per
Step 5 of `research/persona-build-flow.md`.

| Opportunity | Journey stage | Farmer value | AI potential | Workflow complexity | Adoption likelihood | Priority |
|---|---|---|---|---|---|---|
| Feed & pasture position tracking | Monitor conditions → Procure inputs | Medium on its own; high as the enabling input the sale-timing card is missing | Low-medium (structured estimation from existing observations, not novel prediction — functionally overlaps existing commercial tools) | Very low (background estimate, no case logic) | Medium — lower trust bar than sale-timing since it only structures an estimate the grazier already makes, but competes with existing commercial grazing tools for the "why build this" case | ⭐⭐ |
| Sale timing & channel advisor | Sell/output | Very high — targets the highest-stakes, most volatile-income decision point identified for this persona | Medium-high (synthesis/prediction across feed, condition, and market data) | Low (standing decision-support view; no case/escalation logic — see the card's own Step 4 reasoning) | Low-medium — highest trust bar of any card across both personas so far, and the "who validates this" anchor is unresolved (see below) | ⭐⭐⭐ |

## Reading this matrix

- **Feed & pasture position tracking** is rated lower priority than the
  card it feeds, unlike horticulture's observation-capture card (which
  scored ⭐⭐⭐ as enabling infrastructure). The difference: horticulture's
  observation-capture card had no real competing product in the sourced
  material, while this card functionally overlaps existing commercial
  grazing tools (Grazing Charts, AgriWebb, Atlas Grazing, Farming
  Forecaster — see `research/sources.md`), which weakens its own
  standalone case even though it's still valuable as an input. Its
  priority should probably rise if a build-vs-partner-vs-integrate
  decision resolves in favour of building rather than partnering — see
  the card's own adoption-mechanism field.
- **Sale timing & channel advisor** carries very high farmer value because
  the persona's own economics data (ABARES income volatility, see
  `research/sources.md`) points at sale timing as plausibly the single
  largest lever in this persona's year — a stronger economic case than
  either horticulture card can make with sourced data alone. Adoption
  likelihood is rated lower than any horticulture card, deliberately:
  horticulture's two highest-value cards (plan operationalisation, pest
  detection) both have a named, sourced trust anchor — the agronomist.
  This card's simulated-interview signal suggests the stock agent is the
  closest analogue, but only for this specific decision, and that's still
  unconfirmed; a wrong recommendation here also has higher stakes than a
  wrong pest-ID call. High value with a shakier trust foundation is
  exactly why this card is rated ⭐⭐⭐ on the strength of its value case,
  not because its adoption risk is settled — the matrix intentionally
  doesn't average these into a false middle score.

## Gaps in this matrix (larger than horticulture's, and why)

- 2 opportunity cards now exist for this persona vs. 3 for horticulture —
  closer to parity, but the friction table in
  `journeys/livestock-grazier-journey.md` still names more `[VALIDATE]`-
  tagged rows (NLIS/compliance data reuse, review & planning) without
  cards.
- No cross-commodity comparison yet — this matrix and horticulture's only
  cover two of the five target personas listed in `README.md`.
- Scores are unvalidated judgement calls, same caveat as the horticulture
  matrix — treat every score above as `[VALIDATE]`.
