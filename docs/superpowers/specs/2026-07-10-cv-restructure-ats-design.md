# Design: Master CV Restructure + ATS PDF Targeting

**Date:** 2026-07-10  
**Status:** Approved in brainstorm (Approach A)  
**Scope:** Restructure `cv.md` toward `examples/cv-example.md`; keep depth for career-ops evaluations; generate ATS resumes via existing PDF mode only.

## Goals

1. Make `cv.md` the long master academic style CV in example-shaped format (summary + bullets + projects + skills), deeper than a 1-page ATS resume.
2. Preserve work-history detail via MECE mapping (each fact in exactly one home; nothing important lost).
3. Keep ATS output as PDF-only through existing `modes/pdf.md` + `generate-pdf.mjs` (no intermediate tailored markdown CVs).
4. Consolidate Publications, Funding, Projects, Open Source, and Skills as master-only sections spanning all roles.

## Non-goals

- Creating a separate short markdown ATS CV file per application
- Archetype tags on bullets (`[ds]` / `[ml]` / etc.)
- Reworking the Canva PDF path
- Inventing new achievements or metrics

## Approach

**A — Example-shaped master** (selected): mirror the example’s section rhythm; drop EXECUTIVE SUMMARY / KEY METRICS / ACCOMPLISHMENTS wrappers; fold the strongest DS/ML/BI Manager metrics into experience bullets; leave PDF mode to select/reorder/trim.

## Master `cv.md` structure

1. Header — name, location, email, LinkedIn, GitHub (portfolio if present in `config/profile.yml`)
2. Professional Summary — 4–6 lines; DS/ML/BI Manager framing; hero metrics retained
3. Skills — one consolidated section (categories such as ML/AI, Analytics/BI, Infra, Languages)
4. Work Experience — WADOC → UW I-LABS → CHOP; each role: company, location, title, dates, **5–8 metric-rich bullets**
6. Education — unchanged content, example formatting
7. Publications — consolidated master-only (full list below + agency white papers)
8. Funding — consolidated master-only across roles
9. Projects — 3–5 flagship items (e.g. NLP classifier, OOC pipeline, MNE-BIDS, key research predictors)
10. Open Source — consolidated master-only (e.g. MNE-BIDS)

**Removed wrappers:** `#### EXECUTIVE SUMMARY`, `#### KEY METRICS`, `#### ACCOMPLISHMENTS`, per-role `#### TECHNICAL SKILLS DEMONSTRATED`, per-role publications/funding subsections.

## MECE content mapping

| Bucket | Owns | Does not own |
|--------|------|--------------|
| Experience bullets | Role actions + proving metrics | Paper titles, grant names, tool laundry lists |
| Projects | Named artifacts that deserve standalone framing | Day-to-day ops already covered under a role |
| Publications | Citable outputs only | Methods narrative already in bullets |
| Funding | Award/sponsor lines only | “Managed $X” impact language (stays in bullets) |
| Open Source | Repo/community contributions | Findings published as papers |
| Skills | Capability inventory once | Per-role skill dumps |

### Per-role theme partitions (for bullet curation)

Within Experience, partition current accomplishments into non-overlapping themes; keep 1–2 bullets per theme (5–8 total per role).

**WADOC example themes:** Leadership/Agile · BI/Power BI · NLP/ML · Geospatial/ops analytics · Healthcare/APCD · Governance/DevOps  

**UW / CHOP:** analogous MECE themes from existing accomplishment blocks (pipelines, methods, cohorts, open source handoff → Open Source section, pubs → Publications).

### Exhaustiveness check (required before considering rewrite done)

Build a checklist mapping every current KEY METRICS line and accomplishment block → one of: bullet / project / publication / funding / open source / skills / *intentionally cut* (duplicate or non-DS/ML/BI noise only).

## Publications section (required contents)

The master Publications section **must include all** of the following peer-reviewed / indexed items (APA-style as provided). Order: reverse chronological by year, then author.

1. Bosseler, A. N., Clarke, M., Tavabi, K., Larson, E. D., Hippe, D. S., Taulu, S., & Kuhl, P. K. (2021). Using magnetoencephalography to examine word recognition, lateralization, and future language skills in 14-month-old infants. *Developmental Cognitive Neuroscience, 47*, 100901. https://doi.org/10.1016/j.dcn.2020.100901
2. Bosseler, A., Clarke, M., Tavabi, K., & Kuhl, P. K. (2021). Using MEG to assess the neural mechanisms of phonetic distributional learning and future language growth in 2- and 6-month-old infants. *The Journal of the Acoustical Society of America, 150*(4), A111–A111. https://doi.org/10.1121/10.0007797
3. Joo, S. J., Tavabi, K., Caffarra, S., & Yeatman, J. D. (2021). Automaticity in the reading circuitry. *Brain and Language, 214*, 104906. https://doi.org/10.1016/j.bandl.2020.104906
4. Clarke, M., Larson, E., Tavabi, K., & Taulu, S. (2020). Effectively combining temporal projection noise suppression methods in magnetoencephalography. *Journal of Neuroscience Methods, 341*, 108700. https://doi.org/10.1016/j.jneumeth.2020.108700
5. Appelhoff, S., Sanderson, M., Brooks, T., van Vliet, M., Quentin, R., Holdgraf, C., Chaumon, M., Mikulan, E., Tavabi, K., Höchenberger, R., Welke, D., Brunner, C., Rockhill, A., Larson, E., Gramfort, A., & Jas, M. (2019). MNE-BIDS: Organizing electrophysiological data into the BIDS format and facilitating their analysis. *Journal of Open Source Software, 4*(44), 1896. https://doi.org/10.21105/joss.01896
6. Bosseler, A., Tavabi, K., Clarke, M., Larson, E., Taulu, S., & Kuhl, P. (2019). Word recognition and future language skills in 14-month-old infants. *The Journal of the Acoustical Society of America, 146*(4), 2955–2955. https://doi.org/10.1121/1.5137262
7. Roberts, T. P. L., Cannon, K. M., Tavabi, K., Blaskey, L., Khan, S. Y., Monroe, J. F., Qasmieh, S., Levy, S. E., & Edgar, J. C. (2011). Auditory Magnetic Mismatch Field Latency: A Biomarker for Language Impairment in Autism. *Biological Psychiatry, 70*(3), 263–269. https://doi.org/10.1016/j.biopsych.2011.01.015
8. Tavabi, K., Embick, D., & Roberts, T. P. L. (2011a). Spectral–temporal analysis of cortical oscillations during lexical processing. *NeuroReport, 22*(10), 474–478. https://doi.org/10.1097/WNR.0b013e3283476b84
9. Tavabi, K., Embick, D., & Roberts, T. P. L. (2011b). Word repetition priming-induced oscillations in auditory cortex: A magnetoencephalography study. *NeuroReport, 22*(17), 887–891. https://doi.org/10.1097/WNR.0b013e32834ca576
10. Tavabi, K., Elling, L., Dobel, C., Pantev, C., & Zwitserlood, P. (2009). Effects of Place of Articulation Changes on Auditory Neural Activity: A Magnetoencephalography Study. *PLoS ONE, 4*(2), e4452. https://doi.org/10.1371/journal.pone.0004452
11. Tavabi, K., Obleser, J., Dobel, C., & Pantev, C. (2007). Auditory evoked fields differentially encode speech features: An MEG investigation of the P50m and N100m time courses during syllable processing. *European Journal of Neuroscience, 25*(10), 3155–3162. https://doi.org/10.1111/j.1460-9568.2007.05572.x
12. Villablanca, J. R., Schmanke, T. D., Crutcher, H. A., Sung, A. C., & Tavabi, K. (2000). The growth of the feline brain from fetal into adult life: II. A morphometric study of subcortical nuclei. *Developmental Brain Research, 122*(1), 21–33. https://doi.org/10.1016/S0165-3806(00)00047-X

**Also include (agency / technical deliverables, MECE from WADOC):**

- WADOC Recidivism Measure White Paper (2026)
- Women's Mental Health Research Paper (2025)

Do not duplicate publication titles inside Experience bullets; bullets may cite impact (e.g. “published in Biological Psychiatry”) without reprinting the full citation.

## ATS PDF generation

- **Deliverable:** PDF only via existing pipeline (`modes/pdf.md` → HTML template → `generate-pdf.mjs` → `output/`).
- **Source:** restructured `cv.md`.
- **Behavior:**
  - Rewrite Professional Summary (3–4 lines) with JD keywords + narrative (truth-only).
  - Build Core Competencies (6–8) from Skills + JD.
  - Reorder/trim Experience bullets by JD relevance; never invent.
  - Select top 3–4 Projects.
  - Always include Education.
  - **Publications / Funding / Open Source:** omit from PDF by default; sample 1–3 lines only if the JD clearly values research or open source.
- **Process tweak:** document the above master-only skip/sample rule in `modes/pdf.md`. No new ATS markdown layer; no bullet tagging system.

## Implementation outline (for planning skill)

1. Inventory current `cv.md` → MECE destination checklist.
2. Rewrite `cv.md` to the structure above (preserve facts; compress wording).
3. Verify all 12 listed publications + 2 agency deliverables appear under Publications.
4. Update `modes/pdf.md` with master-only section handling.
5. Spot-check: one sample `/career-ops pdf` dry-run against a DS/ML JD (optional verification).
6. Align `config/profile.yml` proof points / narrative if summary wording changes materially.

## Success criteria

- `cv.md` follows example section rhythm and is substantially shorter than 591 lines while remaining deeper than a 1-pager.
- MECE checklist shows no orphaned KEY METRICS / accomplishment content except intentional cuts.
- All required publications present and not duplicated in bullets.
- PDF mode still runs from `cv.md` without requiring a second CV file.
- Evaluations can still pull proof points from master bullets + Projects + Publications.
