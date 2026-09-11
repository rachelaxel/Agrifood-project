# Workflow: Pest/Disease Triage Case Flow

Operationalises `opportunities/horticulture-pest-disease-detection.md`.
This is the "how does AI actually enter the process" layer (README layer 5)
— the AI opportunity card says what the AI does; this says what happens to
its output.

```
FARMER
  │
  │ uploads photo (existing phone habit)
  ↓
AI ASSESSMENT
  │  interprets image + weather + crop stage + this block's own history
  │
  ├── High confidence
  │       ↓
  │   recommendation returned directly to farmer,
  │   with the confidence score shown
  │       ↓
  │   farmer action (treat / monitor)
  │       ↓
  │   outcome logged against the case (feeds Review & plan next season)
  │
  └── Low confidence, OR high potential impact even if confidence is
      moderate (e.g. a listed biosecurity risk)
          ↓
      case created, routed to agronomist
          ↓
      agronomist reviews (photo + AI's reasoning + block history)
          ↓
      agronomist recommendation issued to farmer
          ↓
      farmer action
          ↓
      outcome logged against the case, AND fed back to improve the
      AI's confidence calibration for this block/crop
```

## Design notes

- **Confidence threshold is a governance decision, not just a modelling
  one** — see the organisational adoption fields on the opportunity card.
  Bias toward escalation at launch; only relax the threshold once there's
  a track record of high-confidence calls being correct.
- **Every case gets an outcome logged**, high- or low-confidence, so the
  end-of-season review (the last journey stage) has real data to work
  from — this is the mechanism that closes the "Review & plan next season"
  gap identified in `journeys/horticulture-tree-crop-journey.md`.
- **The agronomist's queue is the one operational bottleneck to watch.** If
  the AI escalates too often (threshold too conservative, or genuinely high
  disease pressure), the agronomist becomes the new bottleneck this
  opportunity was meant to relieve. Case volume/SLA against agronomist
  capacity should be tracked once this moves past Idea maturity.
- This is a small enough case flow to prototype without a dedicated
  workflow/case-management platform. It becomes a candidate for one (per
  README layer 5, e.g. Pega) once there are multiple opportunity cards
  across commodities all creating cases into the same agronomist/adviser
  queue, needing shared SLAs, audit trail, and routing rules rather than
  a one-off script.

## Sources

Case-flow shape (high/low confidence branching with human escalation) is
this project's own design applying the AI opportunity card, not sourced
from an existing case study — flagged `[VALIDATE]` until tested in a
scenario prototype with a real or simulated agronomist.
