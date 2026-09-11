# AgriFood AI Adoption Project

## What this project is

A dynamic platform for **understanding**, not solving. Its job is to help innovators
(agtech builders, RDCs, agronomists, investors) see the real landscape of Australian
agriculture — the operating reality of farmers, the gap between how advice is given
and how it's actually used, and where AI could plausibly fit — before anyone builds
a solution.

It is explicitly **not** a recommendation engine, a farm-management SaaS, or a
sales tool for a specific agtech product. It's a discovery and sense-making layer:
persona-driven, journey-based, economics-aware.

## Working definition of "AI adoption" for this project

Adoption is not "a farmer uses an AI tool." It's a multi-stage shift in how a farm
operates day to day:

1. **Awareness** — the grower knows AI-assisted options exist and roughly what they do.
2. **Trust** — the grower believes the system understands their context (soil, region,
   commodity, risk tolerance) well enough to listen to it.
3. **Fit** — the recommendation slots into existing workflows (phone calls, paddock
   walks, agronomist visits) without demanding a new one.
4. **Economic viability** — the time/labour/cash-flow cost of adopting is clearly
   smaller than the margin, risk, or time benefit, on a timeframe the farm can absorb.
5. **Action** — the grower actually does something differently, not just receives
   information.
6. **Retention/learning** — the system (and the farmer) improves from the outcome,
   so the next cycle is easier, cheaper, or more trusted.

A platform "increases AI adoption" if it moves growers through these stages faster,
or removes the reasons they stall at any one of them.

## Core thesis

> Build AI around the farmer's existing operating system, rather than asking the
> farmer to adopt another technology system.

The product is an **operational/advisory layer** that sits between observation and
action (and often between grower and agronomist), not another standalone platform
competing for the farmer's attention.

## The operating model: 6 layers, not a list of AI use cases

The wrong question is "where can we put AI?" The right sequence is
persona → journey → friction → AI opportunity → workflow → adoption → value.
Skipping straight to "AI opportunity" produces a pile of disconnected features;
working the full sequence produces a platform that can be prioritised and
defended.

```
┌─────────────────────────────────────────────┐
│  1. FARMER PERSONAS                          │
│  Who are we designing for?                   │
└─────────────────────┬─────────────────────────┘
                       ↓
┌─────────────────────────────────────────────┐
│  2. FARMER JOURNEYS                          │
│  What are they trying to accomplish?         │
└─────────────────────┬─────────────────────────┘
                       ↓
┌─────────────────────────────────────────────┐
│  3. FRICTION & OPPORTUNITY MAP               │
│  Where are the operational problems?         │
└─────────────────────┬─────────────────────────┘
                       ↓
┌─────────────────────────────────────────────┐
│  4. AI OPPORTUNITY LIBRARY                   │
│  Where can AI augment/predict/automate?      │
└─────────────────────┬─────────────────────────┘
                       ↓
┌─────────────────────────────────────────────┐
│  5. WORKFLOW & OPERATING MODEL               │
│  How does AI actually enter the process?     │
└─────────────────────┬─────────────────────────┘
                       ↓
┌─────────────────────────────────────────────┐
│  6. ADOPTION & VALUE                         │
│  Will people use it, and does it deliver?    │
└─────────────────────────────────────────────┘
```

Adoption is a **design criterion for every opportunity**, assessed alongside
it — not a training exercise bolted on at the end. Every AI Opportunity Card
(layer 4, see below) carries its own adoption barrier and mechanism.

### The three loops

Read top-to-bottom, the six layers are a pipeline. Read as a system, they're
three connected loops that feed back into each other:

- 🔵 **Discover**: Persona → Journey → Friction → Opportunity
- 🟢 **Operationalise**: AI → Workflow → Human → Action → Outcome
- 🟠 **Adopt**: Trust → Behaviour → Capability → Usage → Value

Outcomes from the Adopt loop feed back into Discover: a better understanding
of what actually got used (and what didn't) sharpens the next round of
personas, journeys, and opportunity cards. That feedback loop is what makes
this a platform rather than a one-off ideation exercise.

## Layer-by-layer: what each one is and produces

### 1. Farmer personas
"What does this farmer actually have to do to run their business?" — not
demographics, but their operating environment and decisions. See
`personas/` and the persona template below.

**Interview-style discovery is part of building the persona, not a
separate step afterward** — see `research/interview-guide.md` for the
question set used to fill and correct each persona.

### 2. Farmer journeys
The major stages a farmer's business moves through in a cycle, independent
of commodity:

```
PLAN
  ↓
Monitor conditions
  ↓
Make production decisions
  ↓
Procure inputs
  ↓
Manage labour/equipment
  ↓
Harvest
  ↓
Sell/output
  ↓
Manage finance/compliance
  ↓
Review & plan next season
```

Layer the farmer's interactions with government, agribusinesses, suppliers,
banks, and insurers onto this spine — that combination is the experience
map. See `journeys/` for commodity-specific instances of this spine.

### 3. Friction & opportunity map
For each journey stage, capture: the farmer's actual problem, and their
current behaviour/workaround. A table, not a diagram — see the friction
table in each `journeys/*.md` file. This is what turns a journey map into
opportunity territory, without yet naming an AI solution.

### 4. AI opportunity library
For each friction point, ask what AI could do: predict, summarise,
interpret, recommend, automate, coordinate, generate, interact
conversationally, or detect anomalies. Each credible answer becomes one
**AI Opportunity Card** in `opportunities/` — a consistent, comparable unit
covering persona, journey stage, problem, AI intervention, workflow
intervention, human role, adoption barrier/mechanism, potential value, and
maturity. See `opportunities/TEMPLATE.md`.

### 5. Workflow & operating model
An AI opportunity is intelligence; a workflow is what operationalises it.
For each opportunity with any conditional logic (e.g. "escalate to a human
when confidence is low"), map the actual case flow: who/what handles it,
what triggers escalation, what the human role is. See `workflow/`. Where an
opportunity needs real case management, orchestration, human-in-the-loop
review, rules, SLAs, integrations, or auditability, this is the layer where
a workflow/case-management platform (e.g. Pega) would become the
operational backbone — a decision made *after* the journey work identifies
the need, not before it.

### 6. Adoption & value
Assessed per opportunity card, not as a final phase:

**Farmer adoption** — clear benefit? saves time? reduces risk? improves
yield/margin? fits existing behaviour without a new app? trustable and
overridable? human fallback? works with poor connectivity?

**Organisational adoption** (if an organisation is providing the service)
— who owns the AI? who reviews exceptions? what data is required? who's
accountable when it's wrong? what governance, systems integration, and
workforce skills are required?

Once several commodities have opportunity cards, roll them into an
**AI opportunity matrix** (`matrix/`) scoring farmer value, AI potential,
workflow complexity, and adoption likelihood — the artifact that lets a
sponsor say "here are the opportunities discovered, here are the ones
worth pursuing, here are the ones to pilot first," instead of "we used
Claude to write some personas."

## Persona template (to populate per commodity/type)

- Commodity / production system / typical farm size / region
- A day in the life (observation → decision → action loop)
- Current tools and information sources (phone, paper, specific apps, agronomist
  cadence)
- Jobs-to-be-done (what "success" looks like day to day and season to season)
- Pain points and where advice currently fails to convert to action
- Decision-making style (gut/pattern-based vs. analytical; risk appetite)
- Trust triggers (what would make them believe an AI system) and rejection
  triggers (what would make them dismiss it)
- Language and framing that resonates vs. alienates
- Farm economics snapshot (margin sensitivity, cash-flow rhythm, labour
  constraints)
- Where an agronomist currently gets involved, and what that relationship looks
  like

## Target personas (5 commodities, in build order)

1. **Horticulture grower** (perennial tree/vine crop) — prototype built, see
   `personas/horticulture-tree-crop-grower.md`.
2. **Livestock grazier** (beef/sheep) — prototype built, see
   `personas/livestock-grazier.md`. Heavily `[VALIDATE]`-tagged pending
   interviews; the biggest open structural question is whether this
   persona has a single trusted advisor relationship the way horticulture
   has its agronomist, or a more distributed model (vet/agent/group
   extension) — see the persona and journey files.
3. **Grain farmer** (broadacre) — not yet built.
4. **Dairy farmer** — not yet built.
5. **Cotton producer** — not yet built.

Each should get the full stack: persona → journey → friction table →
opportunity cards → workflow diagrams for any high-complexity opportunity
→ its own row(s) in the cross-commodity opportunity matrix.

## Information needed (data inputs to the platform)

- **Commodity landscape data**: production systems, regional variation, typical farm
  sizes, seasonal cycles, existing input/output economics per commodity.
- **Grower interview data**: day-in-the-life transcripts, journey maps, direct
  quotes on trust/rejection triggers.
- **Existing agtech adoption research**: RDC/AgriFutures reports, published adoption
  studies, agtech vendor case studies (including failures — why tools got dropped).
- **Economic benchmarks**: typical margins, labour costs, cash-flow cycles per
  commodity/farm size, so the platform can sanity-check "is this economically
  worthwhile" for a given use case and persona.
- **Agronomist perspective**: how plans are currently built and handed off, and
  where they see follow-through break down.
- **Technology adoption curve data**: which growers/regions/commodities are
  early adopters vs. resistant, and observable correlates (age, farm size,
  succession status, connectivity, prior tech experience).

## Immediate next step

Turn this into a small discovery project with one concrete guiding question:

> If we followed 5–10 growers through their actual journeys, where could an AI
> agent create measurable economic value without asking them to fundamentally
> change how they farm?

That bridges the conceptual thesis → real farmer behaviour → AI opportunities →
workflow design → adoption case → commercial case.

## Repo structure

```
/personas/       - one file per persona, using the template above
/journeys/       - the PLAN...Review journey spine, instantiated per persona,
                   with a friction table (journey moment / problem / current
                   behaviour)
/opportunities/  - AI Opportunity Cards (see TEMPLATE.md), one per credible
                   AI intervention identified from a friction point
/workflow/       - case-flow diagrams for opportunities that need orchestration,
                   escalation, or human-in-the-loop review
/matrix/         - cross-opportunity prioritisation matrices, one per commodity
                   plus an eventual cross-commodity roll-up
/research/       - interview guide, source log, RDC/AgriFutures material
```

## Sourcing discipline

Every persona, journey, and opportunity-card claim should trace back to a
cited source or be explicitly flagged as an unvalidated hypothesis. All
external sources found while researching this project are logged in
`research/sources.md`, with a confidence rating (primary/quantitative,
program/industry, or secondary/commentary) and notes on how each was used.
Downstream files should link back to that log rather than restating claims
without attribution — this keeps it clear what's grounded in real research
(RDC/AgriFutures/ABARES/ABS/McKinsey data, published studies) versus what
still needs a grower interview to confirm.
