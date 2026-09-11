# Journey: Horticulture Tree-Crop Grower (Prototype)

> **Status: Hypothesis draft**, companion to
> `personas/horticulture-tree-crop-grower.md`. Grounded where noted by
> sources in `research/sources.md`, but not yet interview-validated — to be
> corrected against real interviews (`research/interview-guide.md`) before
> use in opportunity/workflow design downstream. Supersedes the earlier
> "workflow map" version of this file, which is now split across this
> journey map, the friction table below, and standalone AI Opportunity
> Cards in `opportunities/`.

## Purpose

Map this persona onto the standard journey spine from `README.md`, then
locate the friction points objectively (problem + current behaviour) before
naming any AI intervention. AI opportunities and their operational
workflows are deliberately kept out of this file — see `opportunities/` and
`workflow/` — so this map stays a description of the *current state*, not a
proposed future one.

## The journey spine, instantiated for this persona

```
PLAN
  - Season plan set with agronomist: nutrition, spray, irrigation program,
    labour/harvest timing targets. `[VALIDATE]` how formal this is and how
    far ahead it's set.
  ↓
MONITOR CONDITIONS
  - Daily walk: canopy, fruit set, irrigation lines, pest/disease signs.
    Observational, pattern-matched against "normal for this block, this
    time of year," not instrumented.
  - Phone calls to agronomist for a quick check when something looks off.
  ↓
MAKE PRODUCTION DECISIONS
  - Informal triage on anything unusual: urgent enough to call now, or
    monitor? Decision made from memory/experience, not a recorded baseline.
  - Reactive decisions: irrigation adjustment, spot spraying, labour
    reallocation for the day.
  ↓
PROCURE INPUTS
  - Water allocation, chemicals, nutrition products, sometimes cartage/
    packing contracts. `[VALIDATE]` — supplier relationships and price/
    availability shopping behaviour not yet mapped for this persona.
  ↓
MANAGE LABOUR/EQUIPMENT
  - Permanent staff plus seasonal labour at pruning/harvest; irrigation and
    spray equipment maintained/contracted. `[VALIDATE]` on breakdown/
    equipment-failure behaviour specifically.
  ↓
HARVEST
  - Coordinated around labour availability and packing-shed/marketer
    scheduling. `[VALIDATE]` on how harvest timing decisions are actually
    made (maturity testing vs. gut feel vs. shed capacity).
  ↓
SELL/OUTPUT
  - Output goes to a packing shed/marketer against quality specs;
    `[VALIDATE]` grower's visibility into market timing and price at point
    of sale.
  ↓
MANAGE FINANCE/COMPLIANCE
  - Compliance records for chemical use and QA schemes (e.g. Freshcare/
    SQF) — largely manual paperwork. `[VALIDATE]` real record-keeping
    method (paper/phone note/nothing beyond memory) — this determines
    whether there's any existing structured data to build on.
  ↓
REVIEW & PLAN NEXT SEASON
  - Informal end-of-season review: "did this block perform well or not,"
    rarely tied back systematically to what was recommended vs. done at
    the PLAN stage. This closes the loop back to PLAN, and is where the
    biggest information loss in the whole journey currently occurs.
```

The agronomist enters at PLAN (season program), at MONITOR/DECIDE (ad hoc
calls plus periodic scheduled visits every 2–6 weeks in-season,
`[VALIDATE]` cadence), and implicitly at REVIEW (though the review is
rarely structured enough to actually feed back to the agronomist).
Suppliers/packing-shed/marketer sit at PROCURE and SELL. Banks/insurers not
yet mapped — `[VALIDATE]` in interviews.

## Friction & opportunity map

| Journey stage | Farmer problem | Current behaviour |
|---|---|---|
| Monitor conditions | No structured record of what was observed; season-over-season comparison depends on memory | Daily walk, no logging beyond memory or occasional paper/phone note |
| Monitor → Decide | Deciding whether a deviation is urgent enough to call the agronomist, with no baseline to check against | Informal triage from experience; call agronomist or wait |
| Decide (synthesis) | Too many disparate information sources (weather, visual inspection, past experience) to combine into a clear read | Phone call to agronomist functions as the de facto synthesis step (QUT finding, see `research/sources.md`) |
| Plan → Monitor (handoff) | Agronomist's plan is a document/verbal summary that never resurfaces during the daily walk/decision routine | Grower relies on memory to track whether they're "on plan"; follow-through is inconsistent, not from disagreement but lack of a trigger |
| Manage finance/compliance | Compliance records (chemical use, QA schemes) are manual paperwork, disconnected from the daily observation that could have generated them | Reconciled after the fact, separately from the walk |
| Review & plan next season | No systematic link between what was recommended, what was actually done, and the season's outcome | Informal, subjective review; learning is tacit and slow |

This table intentionally names problems and current behaviour only — it's
the input to `opportunities/`, not a proposal in itself.

## Next steps to validate this map

1. Run interviews against `research/interview-guide.md`, specifically
   walking through *yesterday*, not a generalised "typical day" — for every
   stage above, not just Monitor/Decide (Procure, Labour/Equipment, Harvest,
   Sell, and Finance/Compliance are still largely `[VALIDATE]`).
2. Check whether the journey differs meaningfully between almonds, citrus,
   and wine grapes before generalising this map across "horticulture" — it
   may need to fork into crop-specific variants. Note ABARES data suggests
   many growers run more than one of these crops on the same farm (see
   `research/sources.md`), so the journey may be shared across blocks of
   different crops rather than being crop-specific at the grower level.
3. Get direct access to the Hort Innovation almond adoption program reports
   (AL16001/AL19001/AL22001, see `research/sources.md`) — blocked by this
   session's network proxy — for real precedent on where this journey
   breaks down, without needing to run fresh interviews first.

## Sources

See `research/sources.md`. Directly relevant here: ABARES irrigated
horticulture / Murray-Darling Basin grape farm data (multi-crop pattern);
QUT Darling Downs digital AgTech case study (agronomist as synthesis point,
trust); Hort Innovation almond adoption program listings (candidate
real-world precedent for the plan-handoff breakdown described above, not
yet read in full).
