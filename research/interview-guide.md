# Grower Interview Guide (Prototype)

Purpose: fill in and correct the `[VALIDATE]` gaps in personas and journey
maps with real grower behaviour, not domain-knowledge guesses. Structured
around the journey spine in `README.md` so answers map directly onto a
journey file's stages and friction table.

Methodology note: the QUT Darling Downs digital AgTech case study (see
`research/sources.md`) used an *ecosystem* approach — interviewing
agronomists, suppliers, and technology providers alongside the farmer, not
just the farmer in isolation — to understand community-level adoption
dynamics, not just individual traits. Recommend the same here: pair every
grower interview with at least one interview of their agronomist where
possible, using the agronomist-side questions at the end of this guide.

## Before the interview

- Confirm commodity, region, and farm size/structure so the transcript can
  be filed against the right persona (or flagged as needing a new one).
- Ask permission to record, and confirm whether findings can be attributed
  by name, by farm type only, or must stay fully anonymous.
- Bring the persona's current "open questions" list (see the bottom of
  `personas/*.md`) as a checklist, but don't read it as a script — the goal
  is *yesterday*, in the grower's own words, not a generalised description
  of "a typical day."

## Core interview: walk through yesterday

Open with: **"Talk me through yesterday, start to finish — what you did,
what you noticed, who you spoke to."** Let them talk before steering into
the structured questions below; note anything that doesn't fit the journey
spine, since that's a sign the spine itself needs correcting for this
persona.

### Plan
- How far ahead do you plan (season, multi-season)? What's actually
  written down vs. in your head?
- Who's involved in setting the plan — agronomist, family, contractor,
  bank?
- What would make you deviate from the plan mid-season?

### Monitor conditions
- What do you actually look at/for on a typical walk or check? (Push for
  specifics: which blocks, what signs, what order.)
- What do you check that isn't in-person — apps, weather services, sensors?
  How many separate sources, and do you trust them equally?
- When something looks different than expected, what's the first thing you
  do?

### Make production decisions
- What was the last thing you decided based on something you noticed,
  without calling anyone? What made you confident enough to act alone?
- What was the last time you called the agronomist about something you
  noticed? What made it worth the call?
- Have you ever been given a plan or recommendation you didn't follow
  through on? What happened, and why?

### Procure inputs
- How do you decide what to buy and from whom — price, relationship,
  availability, recommendation?
- Where does uncertainty (price, supply) cause you the most trouble?

### Manage labour/equipment
- How do you handle unexpected equipment failure — who do you call, how
  fast can you get a fix?
- How do you find/coordinate seasonal labour, and what's the hardest part
  of that?

### Harvest
- How do you decide when to start harvest? Whose input matters most?
- What logistics (labour, contractors, shed capacity) cause the most
  last-minute scrambling?

### Sell/output
- How much visibility do you have into price/market timing at the point of
  sale? Do you feel you're selling at the right time?

### Manage finance/compliance
- How do you currently keep the records compliance requires (chemical use,
  QA schemes)? Paper, phone, app, nothing until it's needed?
- Does that record-keeping ever help you make a decision, or is it purely
  for compliance?

### Review & plan next season
- At the end of the season, how do you assess whether it went well? What
  do you compare it against?
- Do you go back and check whether you followed the plan/advice you were
  given during the season?

## Trust and rejection (ask directly, don't infer)

- What would it take for you to trust a system telling you something's
  wrong with a block, without you seeing it yourself first?
- Tell me about a piece of technology or software you tried and stopped
  using. What went wrong?
- What's the difference between advice you trust and advice you dismiss?

## Economics (ask for specifics, not general agreement)

- What's the real cost — time, money, hassle — of your current way of
  doing [the specific journey stage just discussed]?
- If something saved you an hour a week, would you notice? What about
  saving you a bad decision once a season?
- Whose money/time would this need to save to be worth adopting — yours,
  the business's, your labour's?

## Companion questions for the agronomist

- What's the most common reason a grower doesn't follow through on a plan
  you've given them?
- How much of your job is diagnosis vs. helping them operationalise
  something you've already told them?
- What do you wish growers recorded or told you that they currently don't?
- If an AI tool pre-triaged grower questions before they reached you, what
  would need to be true for you to trust its judgement?

## After the interview

- File the transcript/notes under a new entry in this repo (suggest
  `research/interviews/<persona>-<date>.md`, not yet created — create the
  directory when the first real interview happens).
- Go back to the relevant `personas/*.md` and `journeys/*.md` files and
  replace `[VALIDATE]` tags with findings, citing the interview by date
  rather than leaving claims unsourced.
- Flag anything that contradicts an existing `[VALIDATE]` guess loudly —
  a correction is more valuable than a confirmation.
