# AI Opportunity Card — Feed & Pasture Position Tracking

**Opportunity name**: Structured tracking of the grazier's own feed/pasture
position

**Persona**: `personas/livestock-grazier.md`

**Journey stage**: Monitor conditions → Procure inputs (feeds the Sell/
output stage — see relationship to
`opportunities/livestock-sale-timing-advisor.md` below)

**Problem** (from `journeys/livestock-grazier-journey.md` friction table):
Two related but distinct gaps. First, feed procurement in a dry season
carries high uncertainty on availability/price exactly when it matters
most. Second — and the more foundational gap — there is **no structured
record of the grazier's own feed position** (how much pasture/feed is
actually on hand, how many weeks it will carry current stock numbers) to
reason from when either buying feed or deciding whether to sell or hold
stock.

**Current behaviour**: `[VALIDATE]`, sharpened by a simulated interview
(see `research/interviews/livestock-grazier-simulated-01.md`,
Simulated/synthetic tier, not confirmed): the grazier estimates pasture
availability from the same regular vehicle/horseback checks used for
stock condition ("how much is actually there versus how much I think is
there... I get that wrong more than I'd like to admit"), holds a rough
running estimate in his head, and — when actually procuring feed in a dry
run — worked the phone across five separate contacts while the price moved
against him twice during the search. The feed-position estimate and the
procurement search are currently two disconnected activities, not one
workflow.

**AI intervention**: *Interpret* + *summarise* + *predict*. Turn the
grazier's existing pasture observations (from the same walk/vehicle check
already happening under Monitor Conditions) into a running, structured
feed-position estimate — "X weeks of grazing at current stock numbers,
given recent growth and no further rain" — rather than a mental estimate
reconstructed from memory each time it's needed. This is the same pattern
as `opportunities/horticulture-observation-capture.md`: build on an
existing observation habit rather than asking for a new one.

**Workflow intervention**: Minimal, like the horticulture observation-
capture card — a background estimate that updates from existing check-in
data, not an event-triggered case. Becomes an input feed into
`opportunities/livestock-sale-timing-advisor.md` (which explicitly
identified "poor visibility into the grazier's own feed position" as a
gap named by the simulated stock agent) rather than a standalone decision
tool.

**Human role**: None required for the baseline estimate; the stock agent
benefits as a secondary consumer of this data when advising on sale
timing, addressing the specific gap the simulated agent named.

**Adoption barrier — farmer**: Estimating pasture/feed accurately from
observation alone is acknowledged (in the simulated interview) as
something the grazier already gets wrong sometimes — an AI estimate built
on the same inputs inherits that same uncertainty unless it adds something
beyond what the grazier's own eye already does (e.g. combining rainfall
data or satellite pasture-growth signals, which starts to look like the
commercial tools already in market — Grazing Charts, AgriWebb, Atlas
Grazing, Farming Forecaster, see `research/sources.md`). Also: this
persona's rejection trigger around "another platform to log into" applies
here as much as to the sale-timing card.

**Adoption mechanism — farmer**: Anchor the estimate in the grazier's
existing check, adding structure rather than requiring new data entry;
be explicit about uncertainty (a range, not a false-precise number) so it
doesn't overclaim accuracy the underlying observation doesn't support;
position as "helping you check the number you're already carrying in your
head," not replacing the grazier's own judgement.

**Adoption barrier — organisational**: This overlaps functionally with
existing commercial grazing/pasture tools *and* with a live, credible
research program — CSIRO/UNE/CQUniversity's Future Drought Fund-funded
work combining pasture growth models with herd economic models for
destocking/restocking decisions (see `research/sources.md`) is close
enough to this card's core idea that it should be treated as prior art to
connect with, not independently discovered competition. Worth explicitly
deciding whether this is a build-vs-partner-vs-integrate decision — with
either the commercial tools or the CSIRO program — before treating it as
a from-scratch opportunity, more so than any other card across either
persona so far.

**Adoption mechanism — organisational**: Scope the differentiation
narrowly — the value-add here isn't pasture measurement itself (existing
tools already do this) but **feeding that measurement directly into the
sale-timing decision alongside market data**, which is the specific,
sourced gap the simulated stock agent named and which existing standalone
grazing tools don't appear to address (per the commercial-tools source
entries, which frame themselves around pasture/feed budgeting alone, not
combined with market/sale timing).

**Potential value**:
- Directly closes the gap named by the simulated stock agent in
  `opportunities/livestock-sale-timing-advisor.md` — makes that
  higher-value card more deliverable rather than competing with it.
- Plausible reduction in the "ringing five contacts while price moves"
  pattern in a dry season, if the structured estimate gives enough lead
  time to procure feed before the crunch rather than during it.
  `[VALIDATE]` — not yet quantified.
- Lower adoption risk than the sale-timing card alone, since it doesn't
  ask the grazier to trust a market call — only a structured version of
  an estimate he's already making.

**Maturity**: Idea. Lower technical novelty than the sale-timing card
(existing commercial tools already do pasture/feed estimation), so the
real work is the integration/partnership decision named above, not new
modelling.

**Sources**: Entirely from the simulated interview
(`research/interviews/livestock-grazier-simulated-01.md`, Simulated/
synthetic tier, below secondary/commentary) plus the commercial grazing
tools already logged in `research/sources.md` as evidence such
functionality exists in market. Not yet grounded in a real interview —
confirming whether graziers actually want a structured feed-position
estimate (versus trusting their own eye, which several sourced adoption
barriers suggest may be a real preference, not just habit) should be an
early real-interview question.
