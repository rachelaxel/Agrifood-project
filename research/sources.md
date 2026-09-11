# Source Log

Running log of external sources found and used while building personas,
workflow maps, and economics models. Every persona/workflow file should cite
back to entries here (by short name) rather than restating claims without
attribution. Entries are dated by when they were found, not published.

Confidence key:
- **Primary/quantitative** — survey or government data, treat as reliable.
- **Program/industry** — RDC or industry-body program description, credible
  on scope and intent, less reliable on specific on-farm behaviour claims.
- **Secondary/commentary** — news, blog, or vendor commentary; useful for
  framing and leads, not for hard numbers.

---

## Adoption behaviour & barriers (general)

- **AgriFutures Australia — Producer Technology Uptake Program (PTUP)**
  [agrifutures.com.au](https://agrifutures.com.au/resource/putting-the-power-of-ai-into-the-hands-of-every-farmer/)
  — *Program/industry.* Started 2021 to help producers overcome on-farm
  technology adoption barriers. Producer feedback names the top three
  adoption barriers as: **agritech performance, producer digital
  capability/capacity (knowledge, skills, confidence, attitude), and
  return on investment.** This directly supports README's economics-first
  framing (task #4) — ROI is named explicitly as a top-three barrier, not
  an afterthought.
  Used in: `README.md` (adoption definition), to be cited in future
  economics model.

- **AgriFutures Australia — "From hesitation to innovation: Driving
  agritech adoption in Australia"**
  [agrifutures.com.au](https://agrifutures.com.au/news/from-hesitation-to-innovation-driving-agritech-adoption-in-australia/)
  — *Program/industry.* Companion piece to PTUP; frames adoption as a
  behavioural/trust problem, not just a technology-availability problem —
  consistent with the source conversation's thesis.

- **QUT Centre for AgTech — "A Case Study of Human Factors of Digital
  AgTech Adoption"**
  [research.qut.edu.au (PDF)](https://research.qut.edu.au/cab/wp-content/uploads/sites/364/2024/09/Report-CP-digital-AgTech-Case-Study-FINAL-TO-PUBLISH62.pdf)
  — *Primary/qualitative.* Case study on human factors in digital agtech
  adoption. **Not yet read in full — flagged as a priority follow-up read**
  since it looks like the closest existing analogue to the persona/workflow
  interviews the README proposes running from scratch (task #7: don't
  start from zero if this exists already).

- **"Technology Acceptance, Adoption and Workforce on Australian Cotton
  Farms"** (MDPI *Agriculture*, 2022)
  [doi.org/10.3390/agriculture12081180](https://doi.org/10.3390/agriculture12081180)
  — *Primary/academic.* Cotton-specific, but methodologically relevant:
  studies acceptance/adoption plus workforce factors together, which maps
  onto the labour/capacity dimension in README's economics checklist.

- **Case study — cotton farmers, Darling Downs QLD** (referenced via search,
  underlying study not yet pulled) — examines water sensors, satellite
  imagery, and IoT plant probes; interviewed agronomists and suppliers
  alongside farmers on how community-level norms enable/constrain adoption.
  *Primary/qualitative — follow up for full citation.*

- General barrier synthesis (secondary commentary, treat as leads not
  fact): cost, connectivity/digital divide, and a shift "from a digital
  divide to a data divide" (gap between data generation and data use on
  farm) recur across multiple sources — worth testing directly in grower
  interviews rather than taking as given.

---

## Horticulture / tree-crop specific (used for the pilot persona)

- **ABARES — Australian horticulture farm survey program**
  [agriculture.gov.au/abares](https://www.agriculture.gov.au/abares/research-topics/surveys/farm-definitions-methods)
  and [data.gov.au listing](https://data.gov.au/data/organization/abares?tags=horticulture&organization=abares&_tags_limit=0)
  — *Primary/quantitative.* ABARES surveys ~3,000 horticulture farms
  nationally; this is the right source to pull for the persona's
  "farm economics snapshot" section instead of the current `[VALIDATE]`
  placeholders.

- **ABARES — irrigated agriculture / grape farms, Murray-Darling Basin**
  [agriculture.gov.au/abares/.../grapes](https://www.agriculture.gov.au/abares/research-topics/surveys/irrigation/grapes)
  — *Primary/quantitative.* Reports ~86% of grape-growing farms carry 3+
  crops (commonly wine grapes + citrus + another horticulture crop) as of
  2014-15 — i.e. the "single commodity grower" is often not accurate even
  within one region; multi-crop diversification should be reflected in the
  persona rather than assumed away.
  Average farm cash income for irrigated horticulture farms in the
  Murray-Darling Basin: **~$105,800 (2014-15), rising ~15% to ~$122,000
  (2015-16).** These are old figures (a decade+) — need a current-year pull
  before using in an actual economics model, but useful as an order-of-
  magnitude anchor.
  ~16% of horticulture farms had rate of return above 10% in 2015-16,
  mostly large multi-crop operations (citrus, wine grapes, stone fruit,
  pome fruit, almonds) — supports splitting the persona template by farm
  scale, not just commodity.

- **ABS — Australian Agriculture: Horticulture, 2024-25 financial year**
  [abs.gov.au](https://www.abs.gov.au/statistics/industry/agriculture/australian-agriculture-horticulture/latest-release)
  — *Primary/quantitative, current.* Almond production local value ~$1.3B,
  up $217.9M (19.6%) in 2024-25 — good current anchor for scale/growth of
  the almond sub-sector chosen for the pilot persona.

- **Hort Innovation — Almond industry innovation and adoption program**
  (AL16001 → AL19001 → AL22001, 2017-ongoing)
  [horticulture.com.au/AL16001](https://www.horticulture.com.au/growers/help-your-business-grow/research-reports-publications-fact-sheets-and-more/al16001/),
  [AL19001](https://www.horticulture.com.au/growers/help-your-business-grow/research-reports-publications-fact-sheets-and-more/al19001),
  [AL22001](https://www.horticulture.com.au/growers/help-your-business-grow/research-reports-publications-fact-sheets-and-more/al22001/)
  — *Program/industry.* Multi-phase, ongoing levy-funded program
  specifically about **adoption** of R&D into almond growing practice
  (irrigation, pollination, pest/disease, food safety, spray application,
  biosecurity, new production systems). This is a direct precedent for the
  README's task #7 (connect to existing RDC research before starting from
  scratch) — these program reports likely already contain grower
  interview/survey data relevant to the persona's pain points and
  decision-making sections. **Not yet read — priority follow-up.**

- **Hort Innovation — National Tree Crop Intensification Program (AS18000)**
  [horticulture.com.au/AS18000](https://www.horticulture.com.au/growers/help-your-business-grow/research-reports-publications-fact-sheets-and-more/as18000/),
  background via [Future Food Systems](https://www.futurefoodsystems.com.au/fruit-and-nut-crops/)
  — *Program/industry.* $28M, 5-year program covering almonds, avocados,
  citrus, macadamias, mangoes; includes on-farm demonstrations and
  crop-specific advisory groups feeding back grower insight to researchers.
  Relevant as both a data source and as a possible real-world analogue for
  how the grower ↔ agronomist ↔ researcher loop currently works at
  industry scale (useful context for the "where the agronomist gets
  involved" section of the persona).

---

## Priority follow-ups (not yet done)

1. Read the QUT human-factors AgTech case study in full and extract any
   direct grower quotes/behavioural findings into the persona file,
   replacing `[VALIDATE]` tags with citations where they match.
2. Pull current (not 2014-15) ABARES horticulture farm income/cost figures
   for the "farm economics snapshot" section — ideally split by almonds,
   citrus, and wine grapes separately rather than the "irrigated
   horticulture" aggregate used above.
3. Locate and skim at least one Hort Innovation almond adoption program
   final report (AL16001 or AL19001) for grower-level qualitative findings.
4. Find the primary Darling Downs cotton digital-agtech case study
   directly (currently only known via secondary summary) and assess
   whether its interview methodology is reusable for this project's own
   grower interviews (README task #1).
