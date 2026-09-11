# AI Opportunity Card — Structured Observation Capture from Existing Photos

**Opportunity name**: Turning existing phone-camera habit into a
structured, retrievable observation record

**Persona**: `personas/horticulture-tree-crop-grower.md`

**Journey stage**: Monitor conditions

**Problem** (from `journeys/horticulture-tree-crop-journey.md` friction
table): No structured record of what was observed on the walk;
season-over-season comparison depends on memory.

**Current behaviour**: `[VALIDATE]`, but sharpened by a simulated
interview (see `research/interviews/horticulture-simulated-01.md`,
Simulated/synthetic tier, not confirmed): the grower already takes
phone-camera photos during the walk "more for my own memory than
anything," but they simply accumulate unused in her camera roll unless
something has already gone wrong and she wants to show the agronomist.
This is a materially easier starting point than assuming zero capture
behaviour exists — the habit is already there; it's just not structured
or retrievable.

**AI intervention**: *Summarise* + *interpret*. Tag existing phone photos
by block/date/what's visible (automatically, from the photo and location/
timestamp metadata, or a one-word voice tag at the moment of taking it) so
they become a searchable, block-specific timeline instead of an
undifferentiated camera roll — no new capture behaviour required, only
structure added to an existing one.

**Workflow intervention**: Minimal — no case/escalation logic. This is
closer to a background service than a workflow: photos get tagged and
filed automatically, surfaced later when relevant (e.g. feeding the
plan-operationalisation check-ins in
`opportunities/horticulture-plan-operationalisation.md`, or as historical
context for the pest/disease detection card).

**Human role**: None required for the baseline capture/tagging step; the
agronomist benefits as a secondary user if given access to the resulting
timeline during visits or calls, replacing "let me find that photo" with a
searchable record.

**Adoption barrier — farmer**: Requires trust that photos (potentially
including sensitive property information) are stored/used appropriately;
also requires the tagging to genuinely require zero or near-zero extra
effort, or it becomes exactly the kind of standalone-app friction that
sank the simulated grower's soil-moisture-probe system (see
`research/interviews/horticulture-simulated-01.md`).

**Adoption mechanism — farmer**: Build entirely on top of an existing
habit (the phone camera) rather than introducing a new one; automatic
tagging wherever possible (location/timestamp) rather than manual data
entry; value shows up passively over time (a season's worth of block 4
photos, browsable) rather than requiring the grower to "use a feature."

**Adoption barrier — organisational**: Photo storage/privacy handling;
this opportunity's value depends on how well it feeds the higher-value
opportunities above it (pest detection, plan operationalisation) rather
than standing alone — it's plausibly foundational infrastructure more
than a standalone product.

**Adoption mechanism — organisational**: Treat this as shared
infrastructure underneath the other two horticulture opportunity cards
rather than a separate product decision — de-risks it since it doesn't
need to independently prove its own adoption case.

**Potential value**:
- Lowest-friction opportunity identified for this persona so far —
  reuses an existing habit rather than asking for a new one.
- Directly enables the "block's own history" data that both other
  horticulture opportunity cards depend on for trust and accuracy.
- Creates the missing season-over-season comparison data referenced
  throughout the persona and journey files.

**Maturity**: Idea. Simplest of the three horticulture opportunity cards
to prototype, and arguably a prerequisite for the other two rather than a
competing priority.

**Sources**: Entirely from the simulated interview
(`research/interviews/horticulture-simulated-01.md`) — Simulated/synthetic
tier, below secondary/commentary. Not yet grounded in any external source
or real interview; the existence of the underlying habit (growers already
taking phone photos on the walk) should be one of the first things
confirmed or corrected in a real interview.
