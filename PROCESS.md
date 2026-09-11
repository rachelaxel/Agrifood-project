# How This Actually Runs Right Now

This is the current, entirely manual, pre-platform process for this
project — written down explicitly so that when this becomes a platform,
it's clear exactly what's being automated/replicated, by whom, and what
breaks if a step is skipped. `research/persona-build-flow.md` is the
content pipeline *within* a persona (Step 0-8 there). This document is one
level up: the actors, the trigger, the tooling, and where a human is
currently required versus where a platform could take over.

## The actors, today

- **The user (Rachel)**: sets direction, asks for a persona/opportunity/
  correction, reviews output, decides what to build next. Every step below
  is initiated by a request from the user in conversation — nothing in
  this project currently runs on its own schedule or trigger.
- **Claude (this AI assistant)**: does the desk research, writes every
  file, runs the simulated interviews, commits and pushes to git. There is
  no separation yet between "the researcher," "the writer," and "the
  reviewer" — one model does all of it in one pass, which is a real
  limitation noted below.
- **GitHub repo (`rachelaxel/agrifood-project`)**: the only system of
  record. Every artifact is a markdown file in git. There is no database,
  no structured data store, no UI — a human (or another AI) reading this
  project today reads it by opening files in the repo.

## The end-to-end loop, as it runs today

```
1. USER REQUEST (in chat)
   "build the livestock persona" / "run the simulated interview" /
   "close the source gap" — always a specific, scoped ask, never the
   system pulling its own next task.
        ↓
2. CLAUDE: DESK RESEARCH
   WebSearch calls (this session's tool), sometimes WebFetch (frequently
   blocked by this session's network egress proxy — a real, current
   limitation, not hypothetical). Results are read and judged for
   credibility by the model, not by any structured pipeline.
        ↓
3. CLAUDE: WRITE / EDIT MARKDOWN FILES
   research/sources.md updated first (every source logged with a
   confidence tier), then personas/journeys/opportunities/workflow/matrix
   files created or edited by hand (Write/Edit tool calls), following the
   structure in research/persona-build-flow.md. Every claim is either
   cited or tagged `[VALIDATE]` — this convention is enforced by the model
   remembering to do it, not by any schema or lint check.
        ↓
4. CLAUDE: SIMULATED INTERVIEW (when requested)
   A persona is role-played by the model itself against
   research/interview-guide.md, informed by everything already in the
   persona/journey files. Output is a transcript file, banner-marked as
   synthetic, in research/interviews/.
        ↓
5. CLAUDE: FEED FINDINGS BACK
   The model re-reads its own earlier files and edits them in place to
   annotate `[VALIDATE]` tags with new signal — from either desk research
   or the simulated interview. This is manual cross-referencing: the model
   has to remember which files reference which claims and go update each
   one. Nothing enforces that every downstream file actually got updated.
        ↓
6. CLAUDE: GIT COMMIT + PUSH
   Every change lands in git with a descriptive commit message. This is
   the only durable, versioned record of the work — the commit history is
   effectively the project's audit log today.
        ↓
7. USER REVIEWS, REDIRECTS, OR ASKS FOR THE NEXT STEP
   Back to step 1. There is no autonomous continuation — the loop always
   waits for the next human request.
```

## What this means concretely, right now

- **Every "matrix" is a hand-typed markdown table.** Nothing calculates a
  priority score from the opportunity cards' fields — the model reads the
  cards and writes numbers/stars it judges to be reasonable. Reordering
  the matrix requires manually re-reading and re-editing it.
- **Every cross-reference is a manual markdown link and a promise to keep
  it in sync.** When `opportunities/livestock-sale-timing-advisor.md`
  needed to point at the new `opportunities/livestock-feed-position-tracking.md`,
  that edit had to be made by hand, in that specific file, by the model
  remembering to do it. Nothing would have caught it if it had been
  missed.
- **"Confidence tier" is a convention, not an enforced structure.** A
  source is primary/program/secondary/simulated because the text says so
  in prose, not because it's a field in a schema. Nothing currently
  prevents two files from disagreeing about the same fact.
- **There is no persona/opportunity registry.** Knowing "which personas
  exist" or "how many opportunity cards livestock has" means listing
  files in the repo (which is what actually happened earlier in this
  project — a claim of parity between personas turned out to be wrong
  until the files were actually counted).
- **Real interviews have no intake path yet.** `research/interview-guide.md`
  exists, but there is no mechanism for an actual grower's answers to
  enter this system other than someone manually writing a markdown file
  in `research/interviews/` the same way a simulated one is written.

## What a platform would need to take over from this process

Mapped directly against the loop above, so it's clear what each future
platform component replaces:

| Manual step today | Platform equivalent |
|---|---|
| Step 2: ad hoc web search, judged by the model | A structured source ingestion pipeline: fetch, tag confidence, store as data, not prose — queryable rather than re-read every time |
| Step 3: hand-written markdown files per persona/journey/opportunity | A data model (persona, journey stage, friction point, opportunity card, adoption fields as actual schema fields, not prose sections) with markdown/UI as a rendered *view* of that data, not the source of truth |
| Step 4: model role-plays an interview and writes a transcript | A structured simulation/interview module that outputs the same schema fields directly (not a narrative transcript to be re-read and manually mined for findings), clearly flagged by a `confidence: simulated` field rather than a written banner |
| Step 5: manual re-reading and cross-file editing to propagate a finding | Findings attach to the specific data node they affect (a friction point, an opportunity card field) with a confidence/source citation — updating it once updates everywhere it's referenced, the way a database foreign key would, instead of a human/model finding every markdown mention |
| Step 6: git commit as the audit trail | A versioned data store with the same "who changed what, when, citing what" guarantee git already gives, but queryable (e.g. "show me every claim sourced only from a simulated interview, across all personas") rather than requiring someone to grep through file text |
| The matrix (hand-scored table) | A computed view: score opportunity cards from their own structured fields (value, complexity, adoption signals) with the scoring logic visible and consistent, not re-judged by hand each time |
| "Which personas/cards exist" (currently: list files) | A registry/dashboard — this is essentially the "select commodity → select persona → interactive journey" front end already sketched in this project's conversation history, sitting on top of the same data model above |
| Real interview intake (currently: none) | An actual intake path — even a structured form that outputs the same schema the simulated interviews target — so real data can start overwriting `confidence: simulated` fields as it comes in |

## The honest limitation of the current process

Everything in this project so far has been produced by one model, in one
pass, checking its own work. There is no independent verification step —
when this document says "the model has to remember to update cross-
references," that's also true of this document's own claims about the
process. The clearest evidence this matters: the earlier claim that
horticulture and livestock personas were "at parity" was wrong, and was
only caught because someone asked to verify it against the actual files.
A platform should assume the same failure mode will recur wherever a
human isn't checking, and should build the registry/schema layer above
specifically to make that kind of drift structurally impossible to miss,
rather than something a re-read might happen to catch.
