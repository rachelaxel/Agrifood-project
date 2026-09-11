# AI Opportunity Card — Predictive Pest/Disease Detection

**Opportunity name**: Predictive pest/disease detection and triage

**Persona**: `personas/horticulture-tree-crop-grower.md`

**Journey stage**: Monitor conditions → Make production decisions

**Problem** (from `journeys/horticulture-tree-crop-journey.md` friction
table): No structured record of what was observed on the walk, and no
baseline to check a deviation against; deciding whether something is urgent
enough to call the agronomist is informal triage from memory.

**Current behaviour** (hypothesised — `[VALIDATE]`): Grower notices unusual
symptoms on the walk → describes it over the phone or takes a photo to send
to the agronomist → waits for a response → decides on treatment once
diagnosed.

**AI intervention**: *Interpret* + *detect anomalies* + *recommend*.
Grower uploads a photo (reusing an existing phone habit, no new device) →
AI identifies the likely issue → combines it with weather, crop stage, and
that specific block's own history (not a generic regional model, per the
persona's trust triggers) → recommends next steps, with a confidence score.

**Workflow intervention**: See `workflow/horticulture-pest-disease-triage.md`
— high-confidence cases return a recommendation directly; low-confidence or
high-impact cases open an investigation case routed to the agronomist.

**Human role**: Agronomist validates and resolves low-confidence or
high-impact cases; retains final authority on treatment decisions.

**Adoption barrier — farmer**: Trust in an automated diagnosis is the core
risk — a wrong call on pest ID could mean real crop loss. Also: does this
replace or route around the agronomist relationship, which the persona
treats as the most trusted information source (QUT finding, see
`research/sources.md`)? **Simulated-interview signal** (see
`research/interviews/horticulture-simulated-01.md`, not confirmed): the
simulated grower named block-specific history — specifically a known
salinity issue in one block — almost unprompted as the thing that would
make her trust or distrust a recommendation, reinforcing that
"block-specific, not regional" isn't just a nice-to-have but the core
trust condition for this opportunity.

**Adoption mechanism — farmer**: Explainable recommendation with a visible
confidence score; automatic escalation to the human agronomist below a
confidence threshold, positioned explicitly as "gets your agronomist the
right information faster," not as a replacement for the call. Fits the
existing phone-photo habit rather than requiring a new device or app
session.

**Adoption barrier — organisational** (if an agronomy business or RDC
operates this as a service): Who is accountable if a high-confidence
recommendation is wrong and the grower acts on it without agronomist
review? What crop-image and outcome data is needed to make the
block-specific comparison credible, and who owns/governs it?

**Adoption mechanism — organisational**: Confidence threshold tuned
conservatively at launch (biased toward escalation), with an audit trail
of every recommendation and outcome to support liability and to retrain
the model — this is the operational role a workflow/case-management layer
would need to own (see `README.md` layer 5).

**Potential value**:
- Reduced crop loss from earlier detection than the current wait-for-
  agronomist-response cycle.
- Reduced unnecessary agronomist call-outs on issues within the
  high-confidence band (agronomist time saved).
- Faster intervention on real issues.
- Possible reduced chemical usage if earlier detection allows more
  targeted treatment. `[VALIDATE]` — plausible, not yet quantified.

**Maturity**: Idea (no local prototype or pilot yet; pattern is well
established elsewhere in agtech, so technical risk is lower than adoption
risk here).

**Sources**: QUT Darling Downs digital AgTech case study (agronomist trust,
data/synthesis burden — see `research/sources.md`). Cold-start problem
(needs enough block-level history to be credible) and specific value
figures are `[VALIDATE]` — not yet grounded in a source or interview.
