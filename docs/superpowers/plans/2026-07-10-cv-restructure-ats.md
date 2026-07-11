# Master CV Restructure + ATS PDF Targeting Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Restructure `cv.md` into an example-shaped, MECE master CV (deeper than a 1-page ATS resume) and document how `modes/pdf.md` samples it for ATS PDFs.

**Architecture:** `cv.md` becomes the single source of truth in example format (Header → Summary → Skills → Experience → Projects → Education → Publications → Funding → Open Source). Experience bullets own role actions + metrics; Publications/Funding/Open Source/Skills are consolidated master-only sections. ATS resumes remain PDF-only via existing `pdf` mode (select/reorder/trim; skip master-only sections unless JD signals research/OSS).

**Tech Stack:** Markdown (`cv.md`), YAML (`config/profile.yml`), mode docs (`modes/pdf.md`), Node PDF pipeline (`generate-pdf.mjs` — unchanged).

**Spec:** `docs/superpowers/specs/2026-07-10-cv-restructure-ats-design.md`

---

## File map

| File | Responsibility |
|------|----------------|
| `docs/superpowers/plans/mece-cv-inventory.md` | Exhaustiveness checklist (source block → destination). Created in Task 1; updated as rewrite proceeds. |
| `cv.md` | Master CV rewrite (user layer — primary deliverable). |
| `modes/pdf.md` | Document master-only section skip/sample rules for ATS PDFs. |
| `config/profile.yml` | Align headline/proof points if summary wording changes (user layer). |
| `examples/cv-example.md` | Format reference only — do not modify. |

---

### Task 1: MECE inventory checklist

**Files:**
- Create: `docs/superpowers/plans/mece-cv-inventory.md`
- Read: `cv.md` (full), `docs/superpowers/specs/2026-07-10-cv-restructure-ats-design.md`

- [ ] **Step 1: Create the inventory file**

Write `docs/superpowers/plans/mece-cv-inventory.md` with this exact content:

```markdown
# MECE CV Inventory — Kambiz Tavabi

Map every major block in the pre-rewrite `cv.md` to exactly one destination.
Status: `pending` until Task 2–3 complete; then mark `done` or `cut` with reason.

## WADOC (May 2023 – Present)

| Source | Destination | Status |
|--------|-------------|--------|
| Exec summary (4 VA, 63 features, team of 5, 20+ PBI, NLP metrics) | Experience bullets (Leadership + BI + NLP) + Summary | pending |
| Metrics: 4 VA / 63 features / team 5 | Experience — Leadership bullet | pending |
| Metrics: 20+ Power BI / cadences | Experience — BI bullet | pending |
| Metrics: NLP 75.6% F1 / 88.3% prec / 30x / 110K / 73 labels | Experience — NLP bullet + Projects | pending |
| Metrics: OOC 123K / 39 counties | Experience — Geospatial bullet + Projects | pending |
| Metrics: APCD / release cohort 2016–2022 | Experience — Healthcare bullet | pending |
| Metrics: Recidiviz / CSG partners | Experience — Leadership or Governance (partners) | pending |
| Accomp: Agile / product ownership / 60+ features | Experience — Leadership | pending |
| Accomp: Power BI / SAS→SQL / Scorecard | Experience — BI | pending |
| Accomp: NLP classifier pipeline details | Experience — NLP + Projects (NLP classifier) | pending |
| Accomp: OOC geospatial / cooperation score | Experience — Geospatial + Projects (OOC) | pending |
| Accomp: APCD healthcare linkage | Experience — Healthcare | pending |
| Accomp: BI governance / Git / IDE | Experience — Governance | pending |
| Pubs: Recidivism white paper 2026 | Publications (agency) | pending |
| Pubs: Women's MH paper 2025 | Publications (agency) | pending |
| Per-role skills dump | Skills (consolidated) — cut per-role dump | pending |
| Funding: CSG | Funding | pending |

## UW I-LABS (2011 – 2023)

| Source | Destination | Status |
|--------|-------------|--------|
| Exec summary (pipelines, 4 pubs, $2M+) | Experience bullets + Summary | pending |
| Metrics: 12y tenure / 4 pubs / MNE-BIDS | Experience + Open Source + Publications | pending |
| Metrics: N=42 reading / N=27 infant / r=0.73 / r=0.67 | Experience — Infant + Reading bullets + Projects | pending |
| Metrics: ~10 dB noise floor | Experience — Signal quality bullet | pending |
| Metrics: $2M+ grants | Experience — one funding-impact phrase; details → Funding | pending |
| Accomp: MNE-BIDS co-architect | Open Source + Projects one-liner | pending |
| Accomp: MEG preprocessing (tSSS/OTP/SSP) | Experience — Pipelines bullet | pending |
| Accomp: OTP+tSSS validation / ANOVA | Experience — Signal quality | pending |
| Accomp: Infant IFC / vocabulary prediction | Experience — Infant + Projects | pending |
| Accomp: Reading STG automaticity | Experience — Reading + Projects | pending |
| Accomp: BIDS standardization / HFO | Experience — Pipelines (trim HFO into signal quality) | pending |
| Per-role pubs (4) | Publications (canonical APA list) | pending |
| Per-role skills dump | Skills — cut dump | pending |
| Funding list (NIH/NSF/foundations/etc.) | Funding | pending |

## CHOP (2008 – 2011)

| Source | Destination | Status |
|--------|-------------|--------|
| Exec summary (AUC 0.86, 3 pubs, 96+ participants) | Experience + Summary | pending |
| Metrics: AUC 0.86 / d=3.11 / 51ms / sens/spec | Experience — Biomarker bullet + Projects | pending |
| Metrics: N=51 ASD / N=27 NT | Experience — Biomarker | pending |
| Accomp: ROC biomarker validation | Experience — Biomarker | pending |
| Accomp: Blinded / LMM methods | Experience — Methods bullet | pending |
| Accomp: Theta-alpha / gamma oscillatory findings | Experience — Oscillatory bullet | pending |
| Accomp: Cross-paper program | Experience — Program bullet (trim) | pending |
| Per-role pubs (3) | Publications | pending |
| Per-role skills dump | Skills — cut dump | pending |
| Funding: R01-DC008871 / NLMFF / PA DOH | Funding | pending |

## Pre-CHOP publications (not separate jobs in master)

| Source | Destination | Status |
|--------|-------------|--------|
| Tavabi 2009 PLoS ONE | Publications | pending |
| Tavabi 2007 EJN | Publications | pending |
| Villablanca 2000 Dev Brain Res | Publications | pending |
| Bosseler 2019/2021 JASA abstracts | Publications | pending |

## Intentionally cut (noise / pure duplication)

| Source | Reason |
|--------|--------|
| Repeated Quarto/R skill lines in WADOC skills dump | Duplicate within dump → Skills once |
| Full grant narrative repeated inside accomplishment + funding | Funding owns names; bullets keep "$2M+" once |
| Full citation blocks under each job | Publications owns citations |
```

- [ ] **Step 2: Commit inventory**

```bash
git add docs/superpowers/plans/mece-cv-inventory.md
git commit -m "docs: add MECE inventory checklist for CV restructure"
```

---

### Task 2: Rewrite `cv.md` to example-shaped master

**Files:**
- Modify: `cv.md` (replace entire file)
- Read: `examples/cv-example.md`, `docs/superpowers/plans/mece-cv-inventory.md`

- [ ] **Step 1: Backup current CV**

```bash
cp cv.md cv.md.pre-restructure-backup
```

Expected: file `cv.md.pre-restructure-backup` exists (do **not** commit the backup; keep local only or delete after Task 3 verification).

- [ ] **Step 2: Replace `cv.md` with the restructured master**

Overwrite `cv.md` with **exactly** the following content (preserve metrics; do not invent):

```markdown
# CV -- Kambiz Tavabi

**Location:** Seattle, WA
**Email:** ktavabi@gmail.com
**LinkedIn:** https://www.linkedin.com/in/kambiz-tavabi-93255326b/
**GitHub:** https://github.com/ktavabi

## Professional Summary

Principal Data Scientist and BI Manager with a PhD in Neuroscience and 15+ years spanning academic neuroimaging (UW, CHOP), open-source ML infrastructure (MNE-BIDS / MNE-Python), and public-sector AI deployment. At Washington DOC, lead a 5-person team across 4 Agile value areas (63 features), deliver 20+ Power BI dashboards, and own a production multi-label NLP classifier (75.6% micro-F1, 88.3% precision, 30x random baseline) over 110K+ incident records. Research track record includes an ASD language-impairment MEG biomarker (AUC 0.86, Cohen's d = 3.11), infant brain–language prediction (r = 0.73, p = 0.001), and reading-automaticity modeling (r = 0.67, p = 1×10⁻⁶), published in Biological Psychiatry, Developmental Cognitive Neuroscience, Brain and Language, and JOSS. Bridges rigorous statistics, production Python pipelines, and stakeholder communication across clinical, government, and open-science domains.

## Skills

- **ML / AI:** scikit-learn, TF-IDF, multi-label classification, NLP pipelines, model validation, ROC/AUC, experiment design
- **Statistics:** linear mixed models, growth curves, ANOVA, chi-square / Cramer's V, effect sizes (Cohen's d), spatiotemporal cluster permutation, A/B testing
- **Analytics / BI:** Power BI (semantic models, gateway refresh), SQL / T-SQL, ETL, SAS→SQL migration, Quarto / R Markdown reporting
- **Neuroimaging / scientific Python:** MNE-Python, MNE-BIDS, MEG preprocessing (tSSS, OTP, SSP), dSPM, BEM, FreeSurfer, MATLAB
- **Geospatial / networks:** GeoPandas, NetworkX, US Census TIGER/Line, composite scoring
- **Infra / delivery:** Azure DevOps, Git, Agile product ownership, Oracle/OMNI, pandas / NumPy / SciPy
- **Languages:** Python, R, SQL, MATLAB

## Work Experience

### Washington State Department of Corrections -- Tumwater, WA
**Manager, Business Intelligence & Operations Surveillance (BIOS)** | Research & Data Analytics Division
**May 2023 – Present**

- Lead 4 Agile value areas (63 features) and a 5-analyst team delivering BI products, applied research, and ML prototypes for Prisons, Health Services, Reentry, Security, and executive stakeholders; partner with Recidiviz and the Council of State Governments (CSG) Justice Center
- Ship 20+ Power BI dashboards and automated daily-to-annual reports (Reception, WAONE risk, DAT, staffing, recidivism, PEAR misconduct, STG, restrictive housing, fentanyl task force) via SQL ETL, semantic models, and gateway refresh; led SAS→SQL migration that removed recurring manual analyst intervention
- Own production multi-label NLP classification for IMRS incident narratives: 73 labels, 110,928 training records, 75.6% micro-F1 / 88.3% precision / 30x random baseline on 27,700 held-out incidents (scikit-learn TF-IDF + MultiOutputClassifier / LogisticRegression OvR) with human-in-the-loop deployment design
- Built end-to-end Python analytics on 123,291 OOC records (2019–2025, 39 counties): data-quality profiling, county cooperation scores (0–100), and NetworkX transport-flow maps; resolved apparent 45% agency-name missingness to a true 0.8% structural gap via chi-square / Cramer's V (V = 0.859)
- Directed APCD claims linkage for the DOC release cohort (2016–2022): opioid prescribing, coverage, PTSD/opioid intervention and post-release treatment outcomes in reproducible Quarto notebooks for population-health policy
- Established RDA-wide Power BI governance (landing page, QA standards, templates, permissions) plus Git/Azure DevOps standards (README/CHANGELOG, PR review), cutting onboarding time and standardizing delivery quality

### Institute for Learning & Brain Sciences, University of Washington -- Seattle, WA
**Research Science Engineer**
**2011 – 2023**

- Architected scalable Python/MATLAB MEG pipelines across a 12-year pediatric speech, reading, and language program; supported $2M+ NIH/NSF/foundation-funded work with reproducible, BIDS-oriented workflows
- Co-developed MNE-BIDS conversion and metadata tooling (hours→minutes prep; CI on Windows/macOS/Linux); deployed production MEG preprocessing (tSSS, OTP, SSP, head-position compensation, autoreject) for infant through school-age cohorts
- Validated combined OTP + tSSS noise suppression (~10 dB empty-room noise-floor reduction; single-trial localization F(1,31) = 32.54, p < 0.001), informing parameter guidance for multichannel MEG and HFO-relevant clinical use cases
- Delivered first MEG source-modeling study of 14-month-olds during word processing: right IFC activity predicted vocabulary growth (beta = 0.51, p = 0.001); longitudinal brain–vocabulary correlation r = 0.73 (p = 0.001) at 27 months (N = 22; 5 CDI follow-ups)
- Isolated cross-task reading-skill biomarker in N = 42 children (ages 7–12): word-selective STG responses correlated with skill at r = 0.67 (p = 1×10⁻⁶) across lexical decision and fixation tasks using dSPM + spatiotemporal cluster permutation (2000 permutations)

### Children's Hospital of Philadelphia, Department of Radiology -- Philadelphia, PA
**Post-Doctoral Researcher** | Lurie Family Foundations MEG Imaging Center
**2008 – 2011**

- Validated MEG mismatch-field latency as a language-impairment biomarker in ASD: AUC 0.86, sensitivity 82.4%, specificity 71.2%, Cohen's d = 3.11 (~51 ms group delay) in N = 78 children (51 ASD, 27 controls) with blinded scoring and Bonferroni-controlled contrasts
- Built regulatory-minded analysis practices: pre-specified bilateral STG source model, blinded MMF scoring, linear mixed models across 301 observations for unbalanced pediatric repeated measures
- Characterized lexical oscillatory signatures (theta–alpha ERD hemisphere×lexicality interaction; gamma-band ERS near word uniqueness point) and repetition priming (35% dipole attenuation) via SAM beamforming and Morlet TFR pipelines
- Delivered a 3-paper MEG program (Biological Psychiatry; NeuroReport ×2) spanning basic oscillatory neuroscience and translational pediatric diagnostics under NIH R01-DC008871

## Projects

- **WADOC IMRS NLP Incident Classifier** — Production multi-label NLP over 110K+ behavioral incident narratives (73 labels); 75.6% micro-F1, 88.3% precision, 30x random baseline; scikit-learn TF-IDF + OvR logistic regression with HITL deployment design
- **OOC Violator Analytics Pipeline** — Python/GeoPandas/NetworkX pipeline on 123K records across 39 counties; cooperation scoring, transport-flow mapping, structured-missingness audit (Cramer's V = 0.859)
- **Infant MEG Language Predictor** — Longitudinal MEG source-imaging + growth-curve models linking infant right IFC responses to later vocabulary (r = 0.73, p = 0.001); Developmental Cognitive Neuroscience 2021
- **Reading Automaticity MEG Biomarker** — Cross-task STG reading-skill correlation (r = 0.67, p = 1×10⁻⁶) in school-age children; Brain and Language 2021
- **ASD Language-Impairment MMF Biomarker** — ROC-validated MEG latency classifier (AUC 0.86, d = 3.11); Biological Psychiatry 2011

## Education

- PhD in Neuroscience, University of Münster, Germany (2007)
- MSc in Psychology, University of Oregon, USA (2004)
- BSc in Physiology, University of California at Los Angeles, USA (2000)

## Publications

Bosseler, A. N., Clarke, M., Tavabi, K., Larson, E. D., Hippe, D. S., Taulu, S., & Kuhl, P. K. (2021). Using magnetoencephalography to examine word recognition, lateralization, and future language skills in 14-month-old infants. *Developmental Cognitive Neuroscience, 47*, 100901. https://doi.org/10.1016/j.dcn.2020.100901

Bosseler, A., Clarke, M., Tavabi, K., & Kuhl, P. K. (2021). Using MEG to assess the neural mechanisms of phonetic distributional learning and future language growth in 2- and 6-month-old infants. *The Journal of the Acoustical Society of America, 150*(4), A111–A111. https://doi.org/10.1121/10.0007797

Joo, S. J., Tavabi, K., Caffarra, S., & Yeatman, J. D. (2021). Automaticity in the reading circuitry. *Brain and Language, 214*, 104906. https://doi.org/10.1016/j.bandl.2020.104906

Clarke, M., Larson, E., Tavabi, K., & Taulu, S. (2020). Effectively combining temporal projection noise suppression methods in magnetoencephalography. *Journal of Neuroscience Methods, 341*, 108700. https://doi.org/10.1016/j.jneumeth.2020.108700

Appelhoff, S., Sanderson, M., Brooks, T., van Vliet, M., Quentin, R., Holdgraf, C., Chaumon, M., Mikulan, E., Tavabi, K., Höchenberger, R., Welke, D., Brunner, C., Rockhill, A., Larson, E., Gramfort, A., & Jas, M. (2019). MNE-BIDS: Organizing electrophysiological data into the BIDS format and facilitating their analysis. *Journal of Open Source Software, 4*(44), 1896. https://doi.org/10.21105/joss.01896

Bosseler, A., Tavabi, K., Clarke, M., Larson, E., Taulu, S., & Kuhl, P. (2019). Word recognition and future language skills in 14-month-old infants. *The Journal of the Acoustical Society of America, 146*(4), 2955–2955. https://doi.org/10.1121/1.5137262

Roberts, T. P. L., Cannon, K. M., Tavabi, K., Blaskey, L., Khan, S. Y., Monroe, J. F., Qasmieh, S., Levy, S. E., & Edgar, J. C. (2011). Auditory Magnetic Mismatch Field Latency: A Biomarker for Language Impairment in Autism. *Biological Psychiatry, 70*(3), 263–269. https://doi.org/10.1016/j.biopsych.2011.01.015

Tavabi, K., Embick, D., & Roberts, T. P. L. (2011a). Spectral–temporal analysis of cortical oscillations during lexical processing. *NeuroReport, 22*(10), 474–478. https://doi.org/10.1097/WNR.0b013e3283476b84

Tavabi, K., Embick, D., & Roberts, T. P. L. (2011b). Word repetition priming-induced oscillations in auditory cortex: A magnetoencephalography study. *NeuroReport, 22*(17), 887–891. https://doi.org/10.1097/WNR.0b013e32834ca576

Tavabi, K., Elling, L., Dobel, C., Pantev, C., & Zwitserlood, P. (2009). Effects of Place of Articulation Changes on Auditory Neural Activity: A Magnetoencephalography Study. *PLoS ONE, 4*(2), e4452. https://doi.org/10.1371/journal.pone.0004452

Tavabi, K., Obleser, J., Dobel, C., & Pantev, C. (2007). Auditory evoked fields differentially encode speech features: An MEG investigation of the P50m and N100m time courses during syllable processing. *European Journal of Neuroscience, 25*(10), 3155–3162. https://doi.org/10.1111/j.1460-9568.2007.05572.x

Villablanca, J. R., Schmanke, T. D., Crutcher, H. A., Sung, A. C., & Tavabi, K. (2000). The growth of the feline brain from fetal into adult life: II. A morphometric study of subcortical nuclei. *Developmental Brain Research, 122*(1), 21–33. https://doi.org/10.1016/S0165-3806(00)00047-X

### Agency / technical deliverables

- WADOC Recidivism Measure White Paper (2026)
- Women's Mental Health Research Paper (2025)

## Funding

- Council of State Governments (CSG) Justice Center (WADOC partnership)
- NIH NINDS R01-NS104585; NIH NICHD R21HD092771 and R01HD09586101; NSF BCS 1551330
- BRAIN Initiative / NIMH 1R24MH114705; NRF Korea 2018K2A9A2A20088926 and 2019R1C1C1009383
- EC H2020-MSCA-IF-2018-837228-ENGRAVING; Academy of Finland 310988; ERC Starting Grant SLAB ERC-YStG-676943
- Bezos Family Foundation; Simms Mann Foundation; Ready Mind Project Campaign (UW); Washington State LSDF; Google Summer of Code 2019
- NIH R01-DC008871 (PI: Timothy P.L. Roberts); Nancy Lurie Marks Family Foundation; Pennsylvania Department of Health

## Open Source

- **MNE-BIDS** (co-developer) — Python package for organizing MEG/EEG/iEEG into BIDS; conversion routines, metadata extraction, anonymized sharing, validator-oriented workflows; multi-OS CI; international contributor community (JOSS 2019, DOI 10.21105/joss.01896)
- **MNE-Python ecosystem** — Production preprocessing pipelines (tSSS, OTP, SSP, autoreject) adopted across UW I-LABS pediatric studies
```

- [ ] **Step 3: Confirm structure headers exist**

```bash
rg -n '^## |^### ' cv.md
```

Expected sections in order:
`Professional Summary`, `Skills`, `Work Experience`, three `###` employers, `Projects`, `Education`, `Publications`, `Funding`, `Open Source`.

Expected: **no** matches for `EXECUTIVE SUMMARY`, `KEY METRICS`, `ACCOMPLISHMENTS`, `TECHNICAL SKILLS DEMONSTRATED`.

```bash
rg -n 'EXECUTIVE SUMMARY|KEY METRICS|ACCOMPLISHMENTS|TECHNICAL SKILLS DEMONSTRATED' cv.md || echo "wrappers_gone"
```

Expected: `wrappers_gone`

- [ ] **Step 4: Commit rewritten CV**

```bash
git add cv.md
git commit -m "refactor: restructure cv.md to example-shaped MECE master CV"
```

---

### Task 3: Verify publications + mark inventory done

**Files:**
- Modify: `docs/superpowers/plans/mece-cv-inventory.md`
- Read: `cv.md`

- [ ] **Step 1: Verify all 12 DOI publications are present**

```bash
for doi in \
  10.1016/j.dcn.2020.100901 \
  10.1121/10.0007797 \
  10.1016/j.bandl.2020.104906 \
  10.1016/j.jneumeth.2020.108700 \
  10.21105/joss.01896 \
  10.1121/1.5137262 \
  10.1016/j.biopsych.2011.01.015 \
  10.1097/WNR.0b013e3283476b84 \
  10.1097/WNR.0b013e32834ca576 \
  10.1371/journal.pone.0004452 \
  10.1111/j.1460-9568.2007.05572.x \
  10.1016/S0165-3806(00)00047-X
 do
  rg -F "$doi" cv.md >/dev/null && echo "OK $doi" || echo "MISSING $doi"
 done
```

Expected: twelve `OK` lines, zero `MISSING`.

- [ ] **Step 2: Verify agency deliverables**

```bash
rg -n 'Recidivism Measure White Paper|Women.s Mental Health Research Paper' cv.md
```

Expected: both titles appear under Publications.

- [ ] **Step 3: Size / depth sanity check**

```bash
wc -l cv.md
```

Expected: roughly **120–220 lines** (much less than 591; still deeper than the 48-line example).

- [ ] **Step 4: Update inventory statuses to `done`**

In `docs/superpowers/plans/mece-cv-inventory.md`, replace every `| pending |` with `| done |` (the Intentionally cut table stays as-is).

- [ ] **Step 5: Remove local backup if verification passed**

```bash
rm -f cv.md.pre-restructure-backup
```

- [ ] **Step 6: Commit inventory completion**

```bash
git add docs/superpowers/plans/mece-cv-inventory.md
git commit -m "docs: mark MECE CV inventory complete after restructure"
```

---

### Task 4: Update `modes/pdf.md` for master-only sections

**Files:**
- Modify: `modes/pdf.md`

- [ ] **Step 1: Insert master-only sampling rules after the Full pipeline list**

After pipeline step 16 (after the blank line following `Report: PDF path...`), insert this section:

```markdown
## Master CV section handling (`cv.md`)

The master CV is example-shaped and deeper than a 1-page ATS resume. When generating PDFs:

1. **Always use:** Professional Summary (rewrite), Skills (competency grid + skills footer), Work Experience bullets (reorder/trim by JD relevance), Projects (top 3–4), Education.
2. **Master-only by default (omit from PDF):** Publications, Funding, Open Source.
3. **Exception:** If the JD clearly emphasizes research publications, academic credentials, or open-source contribution, sample **1–3** lines from Publications and/or Open Source. Do not dump the full lists into the PDF.
4. **Never invent** metrics or employers. Only reword existing bullets with JD vocabulary.
5. Experience bullets are already MECE — select and reorder; do not re-derive content from deleted KEY METRICS blocks.
```

Also update pipeline step 7's example bridge if it still says "Built and sold a business..." — replace that parenthetical example with:

```markdown
7. Rewrite Professional Summary by injecting JD keywords + exit narrative bridge from `config/profile.yml` (truth-only; do not use unrelated boilerplate)
```

- [ ] **Step 2: Confirm the new heading exists**

```bash
rg -n 'Master CV section handling' modes/pdf.md
```

Expected: one match.

- [ ] **Step 3: Commit**

```bash
git add modes/pdf.md
git commit -m "docs: document master-only CV sections for ATS PDF generation"
```

---

### Task 5: Align `config/profile.yml` narrative (light touch)

**Files:**
- Modify: `config/profile.yml` (user layer)

- [ ] **Step 1: Read current narrative block**

```bash
rg -n 'headline:|exit_story:|proof_points:' -A 3 config/profile.yml
```

- [ ] **Step 2: Ensure proof points still match master CV metrics**

If any proof-point `hero_metric` disagrees with `cv.md`, update the YAML to match `cv.md` (CV wins). Do **not** expand scope beyond narrative/proof_points.

Minimum check — these strings should remain accurate vs `cv.md`:

- NLP: `75.6%` F1 and `88.3%` precision / `30x`
- Infant: `r=0.73`
- ASD biomarker: `AUC 0.86` and `Cohen's d=3.11`
- MNE-BIDS JOSS DOI present in proof points or pubs

- [ ] **Step 3: Commit only if YAML changed**

```bash
git add config/profile.yml
git commit -m "chore: align profile proof points with restructured cv.md"
```

If unchanged: skip commit.

---

### Task 6: Final acceptance checks

**Files:**
- Read: `cv.md`, `modes/pdf.md`, spec

- [ ] **Step 1: Run acceptance script**

```bash
python3 - <<'PY'
from pathlib import Path
cv = Path('cv.md').read_text()
assert '## Professional Summary' in cv
assert '## Skills' in cv
assert '## Work Experience' in cv
assert '## Projects' in cv
assert '## Education' in cv
assert '## Publications' in cv
assert '## Funding' in cv
assert '## Open Source' in cv
for bad in ['EXECUTIVE SUMMARY', 'KEY METRICS', 'ACCOMPLISHMENTS', 'TECHNICAL SKILLS DEMONSTRATED']:
    assert bad not in cv, bad
dois = [
  '10.1016/j.dcn.2020.100901','10.1121/10.0007797','10.1016/j.bandl.2020.104906',
  '10.1016/j.jneumeth.2020.108700','10.21105/joss.01896','10.1121/1.5137262',
  '10.1016/j.biopsych.2011.01.015','10.1097/WNR.0b013e3283476b84',
  '10.1097/WNR.0b013e32834ca576','10.1371/journal.pone.0004452',
  '10.1111/j.1460-9568.2007.05572.x','10.1016/S0165-3806(00)00047-X'
]
missing = [d for d in dois if d not in cv]
assert not missing, missing
assert 'Recidivism Measure White Paper' in cv
assert "Women's Mental Health Research Paper" in cv
pdf = Path('modes/pdf.md').read_text()
assert 'Master CV section handling' in pdf
lines = len(cv.splitlines())
assert 100 <= lines <= 250, lines
print(f'ACCEPT OK — cv.md {lines} lines')
PY
```

Expected: `ACCEPT OK — cv.md <n> lines`

- [ ] **Step 2: Optional manual PDF dry-run**

Only if the user asks in-session: run `/career-ops pdf` (or follow `modes/pdf.md`) against one DS/ML JD and confirm Publications/Funding/Open Source are omitted unless the JD is research-heavy.

- [ ] **Step 3: Final commit if any leftover fixes**

```bash
git status
# commit only if Task 6 required fixes
```

---

## Spec coverage (self-review)

| Spec requirement | Task |
|------------------|------|
| Example-shaped master structure | Task 2 |
| MECE mapping + exhaustiveness checklist | Tasks 1, 3 |
| 5–8 metric-rich bullets per role | Task 2 (WADOC 6, UW 5, CHOP 4 — CHOP slightly lean; acceptable depth) |
| Consolidated Skills / Publications / Funding / Open Source | Task 2 |
| All 12 pubs + 2 agency deliverables | Tasks 2–3, 6 |
| PDF-only ATS; master-only skip/sample | Task 4 |
| profile.yml alignment | Task 5 |
| Success: shorter than 591, deeper than example | Task 6 line-count assert |

**Note on CHOP bullet count:** Spec says 5–8 per role; CHOP content compresses cleanly to 4 strong bullets without inventing filler. Do not pad.

**Placeholder scan:** none intentional.

**Section order:** Matches brainstorm + example rhythm (Projects before Education). Spec file numbering had a gap after Experience; this plan uses the coherent order above.
