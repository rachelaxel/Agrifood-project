# Workflow Map: Horticulture Tree-Crop Grower (Prototype)

> **Status: Hypothesis draft**, companion to
> `personas/horticulture-tree-crop-grower.md`. To be corrected against real
> interviews before use in persona/scenario work downstream.

## Purpose

This map exists to answer the README's core discovery question for this
persona: **where in the observe → decide → act loop is there room for an AI
agent to create value without asking the grower to change how they operate?**

## The loop, as currently hypothesised

```
[Morning walk/observation]
   soil, canopy, fruit set, pest/disease signs, irrigation state
        |
        v
[Mental pattern match against "normal for this block, this time of year"]
        |
        +--> matches expectation --> no action, walk continues
        |
        +--> deviation noticed
                |
                v
        [Informal triage: is this urgent / who do I call?]
                |
        +-------+--------+
        |                |
        v                v
 [Phone: irrigation/     [Phone or wait for scheduled
  labour contractor —     visit: agronomist]
  immediate logistics]         |
        |                      v
        |              [Agronomist diagnoses on walk,
        |               leaves plan: nutrition/spray/
        |               irrigation program]
        |                      |
        v                      v
 [Same-day action]     [Plan sits disconnected from
                        grower's daily loop --> partial
                        or inconsistent follow-through]
                               |
                               v
                     [End of season: informal review,
                      rarely tied back to the plan]
```

## Where information gets lost

1. **Observation → record**: what the grower sees on the walk is rarely
   captured in any structured, retrievable form. It lives in memory, so
   season-over-season comparison depends on the grower's recall, not data.
2. **Agronomist plan → daily loop**: the plan is handed over as a document or
   verbal summary at the visit, but there's no mechanism that resurfaces it
   during the grower's actual daily walk/decision points. This is the single
   biggest "adoption" gap named in the README's thesis (task #2).
3. **Action → outcome**: even when the grower does follow the plan, there's
   no lightweight way to attribute a season's performance back to what was
   actually done vs. recommended, so learning is slow and mostly tacit.

## Where repetitive/low-value work occurs

- Re-explaining block history to the agronomist at each visit (rather than
  the agronomist having persistent context).
- Re-deciding urgency/triage manually every time something looks off,
  without a running baseline of "normal for this block."
- Manually reconciling compliance records (chemical use, QA scheme
  requirements) that could double as a structured observation log if
  captured at the point of the walk instead of after the fact.

## Candidate points for an AI agent to sit (to test in scenarios)

| Point in loop | Candidate AI role | Why it fits without changing behaviour |
|---|---|---|
| During the walk | Voice-note capture of observations, tagged to block/date, no new app screen required | Matches existing phone-based habit; turns tacit observation into a retrievable record |
| Deviation noticed | Pattern comparison against the block's own history (not a generic regional model) | Directly extends the grower's existing pattern-recognition skill rather than replacing it |
| Triage | Suggest whether this looks like something to call the agronomist about now vs. monitor | Reduces cognitive load on "who do I call," doesn't remove grower's judgement |
| Agronomist plan handoff | Convert the plan into check-ins that surface during the grower's normal walk/phone routine, rather than a static document | This is the core "operationalise the advice" gap from README task #2 |
| End of season | Auto-summarise what was observed/recommended/done/outcome per block | Creates the learning loop that's currently missing, at near-zero added effort |

## Economics lens on each candidate (to quantify per README task #4)

- **Voice-note capture**: near-zero added time (reuses the walk), main cost
  is trust/privacy concerns and reliability of capture (connectivity in
  paddocks). `[VALIDATE]`
- **Pattern comparison**: value is in earlier detection of deviation →
  reduced yield/quality loss; needs enough historical data per block to be
  credible, which is a cold-start problem worth flagging.
- **Triage support**: value is agronomist time saved (fewer unnecessary
  call-outs) and faster response on real issues; risk is under- or
  over-triaging and eroding trust quickly if wrong.
- **Plan operationalisation**: highest potential value (this is the named
  adoption gap) but highest complexity — depends on structured plan input
  from the agronomist side too, not just the grower side.
- **End-of-season summary**: low cost, moderate value, mainly a trust- and
  retention-building feature rather than a direct economic lever on its own.

## Next steps to validate this map

1. Run 2-3 real interviews against the "open questions" list in the persona
   file, specifically walking through *yesterday*, not a generalised
   description of "a typical day."
2. Check whether the loop differs meaningfully between the three candidate
   crops (almonds/citrus/wine grapes) before generalising this map across
   "horticulture" — it may need to fork into crop-specific variants.
3. Once validated, use this map as the input to a scenario prototype (per
   README task #5) — e.g. simulate the grower saying "this block isn't
   performing like it normally does" and test the candidate AI roles above
   against that scenario.
