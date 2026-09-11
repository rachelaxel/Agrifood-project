# AgriFood AI Adoption Project

## What this project is

A dynamic platform for **understanding**, not solving. Its job is to help innovators
(agtech builders, RDCs, agronomists, investors) see the real landscape of Australian
agriculture — the operating reality of farmers, the gap between how advice is given
and how it's actually used, and where AI could plausibly fit — before anyone builds
a solution.

It is explicitly **not** a recommendation engine, a farm-management SaaS, or a
sales tool for a specific agtech product. It's a discovery and sense-making layer:
persona-driven, scenario-based, economics-aware.

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
or removes the reasons they stall at any one of them. That reframes the core research
question from "what AI feature should we build?" to **"where in this six-stage
progression are Australian growers currently getting stuck, for each commodity and
farm type, and why?"**

## Core thesis

> Build AI around the farmer's existing operating system, rather than asking the
> farmer to adopt another technology system.

The product is an **operational/advisory layer** that sits between observation and
action (and often between grower and agronomist), not another standalone platform
competing for the farmer's attention.

## Key tasks to build this out

### 1. Map the farmer's current operating system
Interview a small number of growers per target commodity and document a "day in the
life": what's observed, what's recorded, what happens on the phone, what decisions
get made, who's consulted, where the agronomist enters, where information gets lost,
where repetitive work happens, where an AI agent could plausibly sit.

**Output:** a workflow map per persona (inputs → decision points → actions → who's
involved → where friction/loss occurs).

### 2. Build 4–6 farmer personas
Anchor on commodity and farm-type diversity, e.g.: horticulture grower, broadacre
farmer, livestock producer, larger commercial operation, smaller family farm,
early-adopter vs. technology-resistant grower.

For each persona, document: jobs-to-be-done, pain points, decision-making style,
language/trust triggers, current tech stack, and farm economics profile.

**Output:** a structured persona template (see below) populated per commodity.

### 3. Identify AI-native workflows per persona
For each persona: "what could an AI agent actually do for this person tomorrow?"
Prioritise concrete operational tasks (e.g. "flag when a paddock's growth pattern
deviates from historical norm and draft a question to send the agronomist") over
generic "AI insights."

### 4. Model the economics of adoption
For each candidate use case, quantify: cost of adoption (time, money, learning
curve), labour saved, cash-flow impact, yield/margin impact, input savings, risk
reduction. This economic model is a first-class artifact of the platform, not an
afterthought — it's what turns "interesting AI feature" into "worth a grower's time."

### 5. Prototype the adviser/agent interaction
Build mock scenarios where a grower states something naturally (e.g. "this block
isn't performing like it normally does") and map what the AI should do: ask
clarifying questions → access farm information → identify patterns → explain the
issue → recommend an action → decide whether to loop in a human agronomist →
track the outcome.

### 6. Explore the "AI agronomist + human agronomist" model
Test AI as reach-extension for agronomists (continuous monitoring, first-line
support, retaining context, operationalising advice) rather than a replacement —
this shapes how the platform frames trust and where it draws the human-in-the-loop
line per persona.

### 7. Connect to existing RDC / AgriFutures research
Before generating new primary research, inventory what already exists: prior farmer
interviews, situational analyses, and persona work from RDCs/AgriFutures that could
be repurposed rather than re-collected. AI may also change the *methodology* here —
enabling situational analysis via simulated personas/scenarios rather than relying
solely on static interviews.

## Information needed (data inputs to the platform)

- **Commodity landscape data**: production systems, regional variation, typical farm
  sizes, seasonal cycles, existing input/output economics per commodity.
- **Grower interview data**: day-in-the-life transcripts, workflow diagrams, direct
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

## Immediate next step

Turn this into a small discovery project with one concrete guiding question:

> If we followed 5–10 growers through their actual workflows, where could an AI
> agent create measurable economic value without asking them to fundamentally
> change how they farm?

That bridges the conceptual thesis → real farmer behaviour → AI use cases →
product proposition → commercial case.

## Suggested repo structure (next commits)

```
/personas/            - one file per persona, using the template above
/research/            - interview notes, RDC/AgriFutures source material, findings
/workflows/            - day-in-the-life maps and workflow diagrams per persona
/economics/            - adoption cost/benefit models per use case and persona
/scenarios/            - mock adviser/agent interaction scripts for testing
/platform/            - the actual dynamic-platform product spec, once informed by
                         the above
```
