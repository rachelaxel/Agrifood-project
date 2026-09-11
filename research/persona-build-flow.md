# The Build Flow (canonical process for every persona)

This is the exact, ordered sequence used to build both personas so far
(horticulture, livestock), written down so it's followed the same way for
every future persona rather than reconstructed ad hoc each time. It
operationalises the 6-layer model in `README.md` into concrete steps and
file outputs.

```
STEP 0 — Desk research
  Search for real sources (RDCs, ABARES/ABS, academic, industry, global
  corroboration). Log every source in research/sources.md with a
  confidence rating, whether or not it ends up used yet.
  Output: entries in research/sources.md
      ↓
STEP 1 — Draft the persona
  Populate the template in README.md's "Persona template" section.
  Every claim either cites a Step 0 source or is tagged `[VALIDATE]`.
  Output: personas/<persona>.md
      ↓
STEP 2 — Draft the journey
  Instantiate the PLAN...Review spine from README.md for this persona,
  then build the friction table (journey stage | farmer problem | current
  behaviour) — describing current state only, no AI proposals yet.
  Output: journeys/<persona>-journey.md
      ↓
STEP 3 — Draft opportunity cards
  For each friction-table row worth pursuing, fill out
  opportunities/TEMPLATE.md: AI intervention, workflow intervention, human
  role, and BOTH adoption fields (farmer + organisational) are mandatory.
  Output: opportunities/<persona>-<opportunity>.md (one file per card,
  as many as the friction table justifies — not a fixed count)
      ↓
STEP 4 — Draft workflow diagrams (only where needed)
  For any opportunity card with branching/escalation/case logic, diagram
  the actual case flow.
  Output: workflow/<persona>-<opportunity>.md
  (Skipped for opportunities that are simple/linear — not every card
  needs one, but check every card and record the decision either way.)
      ↓
STEP 5 — Roll into a matrix
  Score every opportunity card for this persona on farmer value / AI
  potential / workflow complexity / adoption likelihood, with reasoning.
  Every persona gets a matrix file even with only one row — this is what
  makes the persona comparable to others later, not just documented.
  Output: matrix/<persona>-opportunity-matrix.md
      ↓
STEP 6 — Run a simulated interview
  Per research/simulated-interview-methodology.md: construct an invented,
  clearly-labeled grower, role-play them through research/interview-guide.md
  against the Step 1-2 gaps specifically.
  Output: research/interviews/<persona>-simulated-NN.md
      ↓
STEP 7 — Feed simulated findings back
  Go back through Steps 1-5's files and add "Simulated-interview signal"
  annotations wherever the transcript sharpens a `[VALIDATE]` tag or
  suggests a new opportunity/friction point. Never delete the original
  `[VALIDATE]` tag or overwrite it as confirmed — simulated signal is a
  sharper hypothesis, not evidence. Add new opportunity cards / matrix
  rows if the simulation surfaced something not yet captured in Step 3.
  Output: edits across Steps 1-5's files, tagged inline; matrix updated
  if a new card was added
      ↓
STEP 8 — (Future) Real interview replaces simulated tier
  When real grower access exists, run research/interview-guide.md for
  real, file under research/interviews/<persona>-real-NN.md, and repeat
  Step 7 — this time actually resolving `[VALIDATE]` tags with citations,
  since real-interview confidence outranks simulated.
```

## Why the order matters

- Steps 1-5 must happen **before** Step 6, because a simulated interview is
  only useful for sharpening gaps that are already named — it can't
  substitute for having done the desk research and framework-building
  first (see the limits section in
  `research/simulated-interview-methodology.md`).
- Step 5 (matrix) happens **before** Step 6 (simulation) deliberately: it
  forces prioritisation judgement calls to be made and recorded from the
  grounded material first, so the simulated interview is tested against a
  committed structure rather than shaping it from scratch.
- Step 7 is not optional cleanup — a persona isn't "done" until its
  simulated-interview findings have been written back into every earlier
  file they touch. A simulated interview transcript that never gets fed
  back is wasted effort.

## Current status against this flow

| Step | Horticulture | Livestock |
|---|---|---|
| 0. Desk research | Done — 8 sources logged | Done — 3 source entries logged |
| 1. Persona | Done | Done |
| 2. Journey | Done | Done |
| 3. Opportunity cards | 3 cards | 2 cards |
| 4. Workflow diagrams | 1 (pest/disease triage) | 0 — checked for both cards; neither needs one (both are standing views/background estimates, not event-triggered cases) |
| 5. Matrix | Done | Done |
| 6. Simulated interview | Done (01) | Done (01) |
| 7. Feedback | Done | Done |

Livestock is now at the same step-count as horticulture (this file's own
gap analysis triggered `matrix/livestock-opportunity-matrix.md` and
`opportunities/livestock-feed-position-tracking.md`), though with one
fewer opportunity card overall and a materially thinner desk-research base
(3 vs. 8 sources). Closing that source-count gap, or starting a third
persona, are the two live options rather than a forced next step.

## What this flow does NOT include (yet)

Economics quantification (README layer 6 / task #4) hasn't been built as
its own step for either persona — adoption fields on each opportunity card
are qualitative so far. This should probably become **Step 5.5** once
there's real or simulated data specific enough to quantify against,
rather than being invented now.
