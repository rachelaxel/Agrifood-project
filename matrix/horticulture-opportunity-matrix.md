# AI Opportunity Matrix — Horticulture (Tree-Crop Grower)

Rolls up the opportunity cards in `opportunities/` for this persona. Scores
are first-pass judgement calls by this project team, not survey data —
treat as a prioritisation starting point to test with real growers and
agronomists, not a finished scorecard. As more commodities get their own
cards, this file's structure should be repeated per commodity and then
rolled up into a single cross-commodity matrix.

| Opportunity | Journey stage | Farmer value | AI potential | Workflow complexity | Adoption likelihood | Priority |
|---|---|---|---|---|---|---|
| Season plan operationalisation | Plan → Monitor | Very high — targets the project's core named adoption gap | Medium (mostly summarisation/scheduling, not novel prediction) | Low (no branching logic needed for the baseline case) | Medium — depends on agronomists producing structured-enough plans | ⭐⭐⭐ |
| Predictive pest/disease detection & triage | Monitor → Decide | High | High | Medium (confidence-based escalation, agronomist queue management) | Medium — hinges on trust in automated diagnosis and fit with existing agronomist relationship | ⭐⭐⭐ |

## Reading this matrix

- **Season plan operationalisation** scores highest on farmer value because
  it directly addresses the named adoption gap from the source thesis, and
  lowest on workflow complexity because the baseline version needs no
  branching logic — a strong first pilot candidate precisely because it's
  cheap to build and tests the core hypothesis directly.
- **Pest/disease detection** has the highest raw "AI potential" (it's the
  kind of capability most agtech AI pitches lead with) but also the highest
  workflow complexity and a real trust hurdle, since a wrong high-confidence
  call could cause real crop loss — a stronger second-wave candidate once
  there's a working agronomist-escalation workflow to route into (which the
  plan-operationalisation pilot doesn't need to build).

## Gaps in this matrix (to fill before it's useful for real prioritisation)

- Only 2 opportunity cards exist for this persona so far. The friction
  table in `journeys/horticulture-tree-crop-journey.md` names several more
  unaddressed friction points (input procurement, labour/equipment,
  harvest timing, finance/compliance paperwork, output/market timing) that
  don't yet have opportunity cards.
- No cross-commodity comparison yet — this matrix only covers one of the
  five target personas listed in `README.md`.
- Scores are unvalidated judgement calls, not derived from interviews or a
  quantified economics model (README layer 6/README task #4) — treat
  every score above as `[VALIDATE]`.
