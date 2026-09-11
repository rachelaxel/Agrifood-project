# AI Opportunity Card — Season Plan Operationalisation

**Opportunity name**: Turning the agronomist's season plan into daily
check-ins

**Persona**: `personas/horticulture-tree-crop-grower.md`

**Journey stage**: Plan → Monitor conditions (the handoff between them)

**Problem** (from `journeys/horticulture-tree-crop-journey.md` friction
table): The agronomist's plan is a document/verbal summary that never
resurfaces during the daily walk/decision routine — follow-through is
inconsistent not from disagreement but because there's no trigger that
reconnects the plan to the day-to-day loop. This is the single biggest
adoption gap identified in the source thesis for this project.

**Current behaviour** (hypothesised — `[VALIDATE]`): Plan is set at a
scheduled agronomist visit; grower carries it forward from memory (or an
occasional re-read of notes) with no structured prompting during the
season.

**AI intervention**: *Summarise* + *coordinate* + *interact
conversationally*. Convert the agronomist's plan into a small number of
block-and-date-tagged check-ins that surface naturally during the grower's
existing walk/phone routine (e.g. "it's about time to check block 4's
nitrogen program — here's what was planned"), rather than sitting as a
static document.

**Workflow intervention**: Lower complexity than pest/disease triage — no
branching/escalation logic needed for the baseline case, since it's a
scheduled prompt, not a diagnosis. Complexity increases if a check-in
reveals the plan isn't being followed and needs to route back to the
agronomist for a revised plan — that branch would need a workflow diagram
once specified further.

**Human role**: Agronomist authors the original plan and any revision;
grower confirms/adjusts each check-in; no AI-only decision path.

**Adoption barrier — farmer**: Anything that reads as "another platform to
log into" is a rejection trigger for this persona. Also requires the
agronomist's plan to arrive in a structured-enough form to convert into
check-ins — today it's often a verbal or loosely structured document.

**Adoption mechanism — farmer**: Delivered through the channel the grower
already uses (phone notification/voice, not a new app screen); framed as
"reminding you what your agronomist recommended," preserving grower
authorship of the decision rather than issuing instructions.

**Adoption barrier — organisational**: Depends on structured plan input
from the agronomist side, not just the grower side — if agronomists keep
authoring plans as unstructured documents, this opportunity has a
data-capture dependency upstream of it. Also raises the question of who
maintains the check-in schedule if the agronomist doesn't use the system
themselves.

**Adoption mechanism — organisational**: Could be seeded manually at
first (someone transcribes the plan into check-ins after each visit) to
prove grower-side value before asking agronomists to change how they
produce plans — an important sequencing point given how highly this
persona weights agronomist trust.

**Potential value**:
- Directly targets the adoption gap named as the core thesis of this
  project — plausible highest-value opportunity in this set.
- Creates the missing outcome data (what was recommended vs. done) needed
  to close the loop into `Review & plan next season`.
- Low direct cost once the plan is structured (mostly a scheduling/
  notification problem, not a modelling problem).

**Maturity**: Idea. Named as the central hypothesis in the source
conversation for this project, but not yet prototyped even as a scenario
script — see next steps below.

**Sources**: This card's problem framing is central to the project's
founding thesis (see conversation context in git history of `README.md`);
no external source yet directly validates the check-in mechanism itself —
flagged `[VALIDATE]` until tested against a real agronomist plan and grower
reaction.
