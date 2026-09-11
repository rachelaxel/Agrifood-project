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

- **QUT Centre for Agriculture and the Bioeconomy — "A Case Study of Human
  Factors of Digital AgTech Adoption: Condamine Plains, Darling Downs"**
  [QUT ePrints record](https://eprints.qut.edu.au/227177/),
  [full PDF](https://research.qut.edu.au/cab/wp-content/uploads/sites/364/2024/09/Report-CP-digital-AgTech-Case-Study-FINAL-TO-PUBLISH62.pdf)
  (PDF and eprints domain both blocked by this session's network egress
  proxy — findings below are reconstructed from search-indexed excerpts,
  not a full read; re-pull directly once network access allows).
  — *Primary/qualitative.* Qualitative case study of a cotton farm in
  Condamine Plains (Darling Downs, QLD) adopting Wi-Fi/LoRaWAN
  connectivity, water and crop sensors, moisture probes, and satellite
  imagery. Took an **ecosystem approach** — interviewing not just the
  farmer but agronomists, technology providers, and suppliers — to
  understand how community-level dynamics enable or constrain on-farm
  adoption, not just individual farmer traits. Companion paper: "Critical
  factors of digital AgTech adoption on Australian farms: from digital to
  data divide," *Information, Communication & Society* Vol 25 No 6 (2022),
  [tandfonline.com](https://www.tandfonline.com/doi/full/10.1080/1369118X.2022.2056712).
  **Key findings directly relevant to this project's personas:**
  - Coined the **"data divide"**: a capability gap between technology
    providers supplying devices/software that generate data, and farmers'
    ability to manage, implement, use, and maintain those tools
    independently. This is a sharper, evidenced version of this project's
    own working hypothesis that "the issue isn't information, it's
    operationalising it" — reframe as: the issue is a data-generation-to-
    data-use capability gap, not raw data availability.
  - **Agronomists were rated the most trusted information source** by
    surveyed farmers, ahead of technology vendors or generic data
    dashboards — attributed to deep regional expertise, local ties, and
    ability to tailor advice to the specific farm. Directly supports this
    project's "AI extends the agronomist" framing (README task #6) over
    an "AI replaces the agronomist" framing.
  - Farmers and their agronomists reported being **"drowning in apps and
    data,"** with no good way to combine disparate datasets into something
    actionable — i.e. the bottleneck observed in the field is synthesis,
    not collection. One agronomist, on why growers don't adopt more: *"I
    don't think they [growers] understand what is available to them."*
    That's a trust/awareness-stage barrier (stage 1-2 in this project's
    adoption model in `README.md`), distinct from the economic-fit barrier
    at later stages — worth keeping these separate in any persona rather
    than lumping all "won't adopt" reasons together.

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

- **McKinsey — "Agtech: Breaking down the farmer adoption dilemma"** (global
  farmer survey, most recently 2024 edition — "Voice of the Global Farmer")
  [mckinsey.com](https://www.mckinsey.com/industries/agriculture/our-insights/agtech-breaking-down-the-farmer-adoption-dilemma),
  [PDF](https://www.mckinsey.com/~/media/mckinsey/industries/agriculture/our%20insights/agtech%20breaking%20down%20the%20farmer%20adoption%20dilemma/agtech-breaking-down-the-farmer-adoption-dilemma.pdf)
  — *Primary/quantitative, global (not Australia-specific — use for
  corroboration/pattern-matching, not as an AU-specific figure).* Surveyed
  farmers globally name **unclear ROI and high implementation/maintenance
  cost** as the top pain points for agtech adoption (North America: 52%
  cite high cost, 40% cite unclear ROI as biggest barriers). Also names
  **ease of use** and **data-sharing trust** as recurring barriers. Global
  adoption is uneven: Europe/North America ~61% using or planning to adopt
  at least one agtech product within two years, vs. ~9% in Asia. Recommends
  agtech vendors lead with **personalisation and science-backed,
  measurable ROI/KPIs** to build trust — directly corroborates both the
  AgriFutures PTUP finding above (ROI as a top-three barrier) and this
  project's core thesis that economics has been under-weighted relative to
  the technology pitch.

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
  (site blocked by this session's network egress proxy — content below is
  from search-indexed summaries, not the primary pages; re-pull directly
  once network access allows).
  — *Program/industry.* Multi-phase, ongoing levy-funded program
  specifically about **adoption** of R&D into almond growing practice
  (irrigation, pollination, pest/disease, food safety, spray application,
  biosecurity, new production systems), run 2020-2023 (AL19001 phase) by a
  small industry development team with established grower networks.
  Delivered mostly via extension/communication channels rather than
  research per se: grower notices and factsheets on seasonal issues, a
  grower survey, and an industry-wide investigation into **bud dieback on
  the Monterey variety** (a concrete example of a real, specific,
  block/variety-level production issue the industry considered important
  enough to survey growers on — a good candidate scenario to build a
  persona interaction around). The program model itself — human industry
  development officers translating R&D into grower-facing advice via
  regular short-form updates — is effectively the human-only version of
  the "operational assistant" this project is exploring replacing/
  augmenting with AI; worth treating this program's own before/after
  adoption data (if published) as a natural baseline. **Grower-level
  survey results themselves not yet located — still a priority follow-up**
  once direct site access is available.

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

1. ~~Read the QUT human-factors AgTech case study~~ — done via
   search-indexed excerpts (see entry above); direct PDF/eprints access is
   blocked by this session's network proxy, so **re-pull the full document
   directly** once that's available to confirm the excerpts above and look
   for additional direct grower quotes.
2. Pull current (not 2014-15) ABARES horticulture farm income/cost figures
   for the "farm economics snapshot" section — ideally split by almonds,
   citrus, and wine grapes separately rather than the "irrigated
   horticulture" aggregate used above.
3. Get direct access to horticulture.com.au (blocked this session) to pull
   the actual AL16001/AL19001 grower survey results and bud-dieback
   investigation findings, rather than relying on search-indexed summaries.
4. The Darling Downs cotton study's interview/ecosystem methodology
   (interviewing agronomists and suppliers alongside farmers, not just
   farmers) looks directly reusable for this project's own grower
   interviews (README task #1) — reflected in `research/interview-guide.md`.
