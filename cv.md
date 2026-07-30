# CV -- Kambiz Tavabi

**Location:** Seattle, WA
**Email:** ktavabi@gmail.com
**LinkedIn:** https://www.linkedin.com/in/kambiz-tavabi-93255326b/
**GitHub:** https://github.com/ktavabi
**Portfolio:** https://ktavabi.github.io/

Data Scientist and Machine Learning Engineer | Business Intelligence Leader | PhD Neuroscientist

## Professional Summary

Data Scientist with 15+ years translating research-grade ML into production systems—from pediatric neuroimaging biomarkers (AUC 0.86, published in Biological Psychiatry) to a live NLP classifier processing 110,000+ correctional incident records. Currently lead analytics and ML delivery at Washington State DOC, building Python pipelines, Power BI dashboards, and human-in-the-loop models that bridge rigorous statistics with stakeholder needs. PhD neuroscientist with a track record of shipping: multi-label classification, growth-curve modeling, and reproducible workflows across government, clinical, and open-source domains.

## Work Experience

### Washington State Department of Corrections -- Tumwater, WA
**Manager, Business Intelligence and Operations Surveillance (BIOS)** | Research and Data Analytics Division
May 2023 – Present

- Lead 5-analyst team across 5 Agile value areas (63 features delivered), shipping 20+ Power BI dashboards, ML prototypes, and applied research for Prisons, Health Services, Reentry, Security, and executive leadership; partner with Recidiviz and CSG Justice Center on policy analytics
- Own a production multi-label NLP classifier for correctional-facility incident narratives: 73 labels across 110,928 training records from a 24-table relational export; scikit-learn TF-IDF with MultiOutputClassifier one-vs-rest logistic regression (ongoing SVM experimentation, ~+5 F1); k-fold cross-validation with Jaccard scoring on 27,700 held-out incidents — 75.6% micro-F1, 88.3% precision, 66.1% recall, 60.8% micro-Jaccard, 60.6% exact match (~30x vs. random baseline); deployed with human-in-the-loop review
- Ship 20+ Power BI dashboards and automated daily-to-annual reports (reception, dynamic risk-and-needs assessment, drug and alcohol screening, custody staffing, recidivism, behavioral misconduct, security-threat assessment, restrictive housing, and fentanyl task force) via SQL ETL (T-SQL, Oracle), DAX semantic models, Power Automate, and gateway refresh; led a SAS-to-SQL migration and gateway automation that cut reporting cycle time roughly 60–70%
- Built end-to-end Python analytics pipeline on 123,291 transport records (2019–2025, 39 counties): 10 source tables to a 32-field analytic model, county-cooperation KPI scoring (0–100), NetworkX transport-flow maps, and automated flagging of 4,107 high-complexity dual-mismatch individuals; resolved apparent 45% key-variable missing data to 0.8% structural gap via chi-square and Cramer's V (V = 0.859); shipped interactive Quarto HTML reports
- Applied A/B and quasi-experimental program evaluation on large administrative datasets (chi-square, Cramer's V) as lead methodologist, preventing misattribution of approximately 45,000 records and strengthening data-quality and program investment decisions
- Directed Medicaid all-payer-claims-database (APCD) linkage for the DOC release cohort (2016–2022): opioid prescribing, coverage, and post-release treatment outcomes in reproducible Quarto notebooks for population-health policy
- Established division-wide Power BI governance (quality-assurance standards, UX templates, permissions) and Git / Azure DevOps standards (README and CHANGELOG conventions, pull-request review), cutting onboarding time and standardizing delivery quality

### Institute for Learning and Brain Sciences, University of Washington -- Seattle, WA
**Research Science Engineer**
2011 – 2023

- Architected scalable Python and MATLAB magnetoencephalography (MEG) pipelines across a 12-year pediatric speech, reading, and language program (signal space separation, artifact rejection, multi-table integration); supported $2M+ in NIH, NSF, and foundation-funded academic research with reproducible, standardized neuroimaging data structure-oriented workflows
- Co-developed an open-source Python package for structured data conversion and metadata tooling (reducing data-prep from hours to minutes; CI/CD on Windows, macOS, and Linux); deployed production MEG preprocessing for cohorts from children through adults
- Validated a combined noise-suppression method (~10 dB reduction in empty-room noise floor; single-trial localization F(1,31) = 32.54, p < 0.001), improving accuracy for dense sensor array MEG parameter guidance
- Delivered the first MEG source-modeling study of 14-month-olds during word processing: right frontal cortical activity predicted vocabulary growth (beta = 0.51, p = 0.001); longitudinal brain-to-vocabulary correlation r = 0.73 (p = 0.001) at 27 months (N = 22, 5 follow-up assessments)
- Isolated a task-switching reading-skill biomarker in 42 children (ages 7–12): word-selective superior-temporal-gyrus (STG) responses correlated with reading skill at r = 0.67 (p = 1e-6) across two tasks, using statistical parametric mapping with spatiotemporal cluster-permutation testing

### Children's Hospital of Philadelphia, Department of Radiology -- Philadelphia, PA
**Post-Doctoral Researcher** | Lurie Family Foundations MEG Imaging Center
2008 – 2011

- Validated MEG auditory discrimination neuromagnetic component latency as a language-impairment biomarker in autism spectrum disorders: AUC = 0.86, sensitivity 82%, specificity 71%, Cohen's d = 3.11 (~51 ms group delay) in 78 children (51 ASD, 27 controls), with blinded scoring and Bonferroni-corrected contrasts—potential biotechnology diagnostic application
- Built regulatory-minded analysis practices: a pre-specified bilateral STG source model, blinded brain response scoring, and linear mixed models across 301 observations for unbalanced pediatric repeated measures
- Characterized lexical oscillatory brain function signatures (theta-alpha desynchronization by hemisphere and lexicality; gamma-band synchronization near the word-uniqueness point) and semantic repetition priming (35% dipole attenuation) via beamforming source localization and Morlet wavelet time-frequency pipelines
- Ran a four-condition auditory oddball design across two cohorts (N = 96+) — 5–8× larger than prior work — using repeated-measures ANOVA, Morlet wavelet time-frequency analysis, and beamforming for neural source isolation
- Delivered a 3-paper MEG program (Biological Psychiatry; NeuroReport, 2011a,b) spanning basic oscillatory neuroscience and translational pediatric diagnostics, under NIH grant R01-DC008871

## Skills

- **Machine Learning and AI:** scikit-learn, MultiOutputClassifier, multi-label classification, NLP pipelines, TF-IDF, k-fold and Jaccard evaluation, model validation, ROC/AUC analysis, experiment design, human-in-the-loop (HITL) deployment
- **Statistics:** linear mixed models, growth-curve modeling, ANOVA, chi-square and Cramer's V association, effect sizes (Cohen's d), spatiotemporal cluster permutation testing, A/B and quasi-experimental design
- **Analytics and BI:** Power BI (semantic models, DAX, gateway refresh), Power Automate, SQL / T-SQL / Oracle, ETL pipelines, SAS-to-SQL migration, Quarto / R Markdown reporting
- **Programming:** Python (pandas, NumPy, SciPy), MATLAB, R, SQL
- **Geospatial and Networks:** GeoPandas, NetworkX, U.S. Census TIGER/Line data, composite scoring
- **Neuroimaging and Scientific Python:** MNE-Python, MNE-BIDS, MEG preprocessing, signal space separation, artifact rejection, Morlet wavelet time-frequency analysis, beamforming, dSPM, boundary-element modeling (BEM), FreeSurfer
- **Delivery and Infrastructure:** Azure DevOps, Git, Agile product ownership, reproducible research workflows

## Projects

- **Correctional Incident NLP Classifier (IMRS)** — Production multi-label classifier for 110,928 correctional-facility incident narratives (73 labels, 24-table export); MultiOutputClassifier one-vs-rest logistic regression with TF-IDF (SVM experimentation ~+5 F1); k-fold / Jaccard on 27,700 holdout — 75.6% micro-F1, 88.3% precision, 66.1% recall, 60.8% micro-Jaccard, 60.6% exact match (~30x random baseline); human-in-the-loop deployment at Washington State DOC
- **Transport Analytics Pipeline** — Python, GeoPandas, and NetworkX pipeline over 123,291 records (10 source tables → 32-field model, 39 counties); county-cooperation KPI, NetworkX flows, automated flagging of 4,107 high-complexity dual-mismatch individuals, Cramer's V missing-data audit (V = 0.859), and interactive Quarto HTML reports
- **Program Experiment Design & Causal-Style Evaluation** — A/B and quasi-experimental frameworks on large administrative datasets as lead methodologist (DOC); chi-square and Cramer's V to separate artifacts from quality problems; prevented misattribution of approximately 45,000 records
- **BIOS Enterprise BI, ETL & Reporting Automation** — Program-scale Power BI / SQL ETL (T-SQL, Oracle) with DAX, Power Automate, and gateway automation (~60–70% reporting cycle-time reduction); 63 features across five Agile domains and 20+ dashboards for executive, legislative, and operational stakeholders
- **Long-Horizon Pediatric Cohort Data Engineering** — 12-year I-LABS MEG program infrastructure: scalable Python and MATLAB pipelines with signal space separation, artifact rejection, and multi-table integration under a $2M+ NIH/NSF portfolio
- **Auditory Oddball & Cortical Dynamics** — Four-condition auditory oddball across two CHOP cohorts (N = 96+); repeated-measures ANOVA, Morlet wavelet time-frequency analysis, and beamforming; peer-reviewed lexical/spectral-temporal papers (NeuroReport)
- **Infant MEG Language Predictor** — Longitudinal MEG source imaging with growth-curve models linking infant brain responses to later vocabulary (r = 0.73, p = 0.001); Developmental Cognitive Neuroscience, 2021
- **Reading-Automaticity MEG Biomarker** — Task-switching brain activation and reading-skill correlation (r = 0.67, p = 1e-6) in school-age children; Brain and Language, 2021
- **ASD Language-Impairment Auditory Discrimination Biomarker** — ROC-validated MEG latency classifier (AUC = 0.86, Cohen's d = 3.11); Biological Psychiatry, 2011

## Education

- PhD, Neuroscience, University of Münster, Germany (2007)
- MSc, Psychology, University of Oregon, USA (2004)
- BSc, Physiology, University of California, Los Angeles, USA (2000)

## Publications

Bosseler, A. N., Clarke, M., Tavabi, K., Larson, E. D., Hippe, D. S., Taulu, S., & Kuhl, P. K. (2021). Using magnetoencephalography to examine word recognition, lateralization, and future language skills in 14-month-old infants. *Developmental Cognitive Neuroscience, 47*, 100901. https://doi.org/10.1016/j.dcn.2020.100901

Bosseler, A., Clarke, M., Tavabi, K., & Kuhl, P. K. (2021). Using MEG to assess the neural mechanisms of phonetic distributional learning and future language growth in 2- and 6-month-old infants. *The Journal of the Acoustical Society of America, 150*(4), A111. https://doi.org/10.1121/10.0007797

Joo, S. J., Tavabi, K., Caffarra, S., & Yeatman, J. D. (2021). Automaticity in the reading circuitry. *Brain and Language, 214*, 104906. https://doi.org/10.1016/j.bandl.2020.104906

Clarke, M., Larson, E., Tavabi, K., & Taulu, S. (2020). Effectively combining temporal projection noise suppression methods in magnetoencephalography. *Journal of Neuroscience Methods, 341*, 108700. https://doi.org/10.1016/j.jneumeth.2020.108700

Appelhoff, S., Sanderson, M., Brooks, T., van Vliet, M., Quentin, R., Holdgraf, C., Chaumon, M., Mikulan, E., Tavabi, K., Höchenberger, R., Welke, D., Brunner, C., Rockhill, A., Larson, E., Gramfort, A., & Jas, M. (2019). MNE-BIDS: Organizing electrophysiological data into the BIDS format and facilitating their analysis. *Journal of Open Source Software, 4*(44), 1896. https://doi.org/10.21105/joss.01896

Bosseler, A., Tavabi, K., Clarke, M., Larson, E., Taulu, S., & Kuhl, P. (2019). Word recognition and future language skills in 14-month-old infants. *The Journal of the Acoustical Society of America, 146*(4), 2955. https://doi.org/10.1121/1.5137262

Roberts, T. P. L., Cannon, K. M., Tavabi, K., Blaskey, L., Khan, S. Y., Monroe, J. F., Qasmieh, S., Levy, S. E., & Edgar, J. C. (2011). Auditory magnetic mismatch field latency: A biomarker for language impairment in autism. *Biological Psychiatry, 70*(3), 263–269. https://doi.org/10.1016/j.biopsych.2011.01.015

Tavabi, K., Embick, D., & Roberts, T. P. L. (2011a). Spectral-temporal analysis of cortical oscillations during lexical processing. *NeuroReport, 22*(10), 474–478. https://doi.org/10.1097/WNR.0b013e3283476b84

Tavabi, K., Embick, D., & Roberts, T. P. L. (2011b). Word repetition priming-induced oscillations in auditory cortex: A magnetoencephalography study. *NeuroReport, 22*(17), 887–891. https://doi.org/10.1097/WNR.0b013e32834ca576

Tavabi, K., Elling, L., Dobel, C., Pantev, C., & Zwitserlood, P. (2009). Effects of place of articulation changes on auditory neural activity: A magnetoencephalography study. *PLoS ONE, 4*(2), e4452. https://doi.org/10.1371/journal.pone.0004452

Tavabi, K., Obleser, J., Dobel, C., & Pantev, C. (2007). Auditory evoked fields differentially encode speech features: An MEG investigation of the P50m and N100m time courses during syllable processing. *European Journal of Neuroscience, 25*(10), 3155–3162. https://doi.org/10.1111/j.1460-9568.2007.05572.x

Villablanca, J. R., Schmanke, T. D., Crutcher, H. A., Sung, A. C., & Tavabi, K. (2000). The growth of the feline brain from fetal into adult life: II. A morphometric study of subcortical nuclei. *Developmental Brain Research, 122*(1), 21–33. https://doi.org/10.1016/S0165-3806(00)00047-X

## Awards

- National Institutes of Health (NIH) Loan Repayment Award — Translational Research Excellence (2010)

## Certifications and Professional Development

- Introduction to Deep Learning and Neural Networks with Keras — IBM Deep Learning Professional Certificate, Coursera (2026). [Credential](https://www.coursera.org/account/accomplishments/verify/OUJCQZSHU8NV)
- Machine Learning with Python — IBM AI Engineering Professional Certificate, Coursera (2026). [Credential](https://coursera.org/share/ac41f26ddb1d0c95e7f915a9d170fa47)
- Supervised Machine Learning: Regression and Classification — Coursera (2024). [Credential](https://coursera.org/verify/UWLZ48LYBDFW)
- Bayesian Statistics: From Concept to Data Analysis — Coursera (2023). [Credential](https://www.coursera.org/account/accomplishments/certificate/DR5CTTN4HL35)
- Data Visualization with Python — Coursera (2023). [Credential](https://www.coursera.org/account/accomplishments/certificate/G4G3368QTG2N)
- Data Science Orientation — Coursera (2023). [Credential](https://www.coursera.org/account/accomplishments/certificate/HM6YZKUP8J8X)
- Certified SQL Developer — W3Schools (2023). [Credential](https://verify.w3schools.com/1NDRG69DTP)
- Statistical Learning — edX (2022). [Credential](https://courses.edx.org/certificates/6def26e9529b4ded83ebfe2e86e7e0da)
- Elekta Neuromag MEG Advanced Program — Elekta, Helsinki, Finland (2012)

## Grant Funding

- Council of State Governments (CSG) Justice Center — Washington State DOC partnership
- National Institutes of Health (NIH): NINDS R01-NS104585; NICHD R21-HD092771 and R01-HD09586101; BRAIN Initiative / NIMH 1R24-MH114705; R01-DC008871 (PI: Timothy P. L. Roberts)
- National Science Foundation (NSF): BCS 1551330
- National Research Foundation of Korea: 2018K2A9A2A20088926 and 2019R1C1C1009383
- European Commission Horizon 2020: MSCA-IF-2018-837228-ENGRAVING; European Research Council Starting Grant SLAB ERC-YStG-676943; Academy of Finland 310988
- Foundations and other: Bezos Family Foundation; Simms Mann Foundation; Ready Mind Project Campaign (University of Washington); Washington State Life Sciences Discovery Fund; Google Summer of Code 2019; Nancy Lurie Marks Family Foundation; Pennsylvania Department of Health

## Open Source

- **MNE-BIDS** (co-developer) — Python package for organizing MEG, EEG, and intracranial-EEG data into the Brain Imaging Data Structure (BIDS); conversion routines, metadata extraction, anonymized-sharing and validator-oriented workflows, and multi-OS continuous integration for an international contributor community (Journal of Open Source Software, 2019; DOI 10.21105/joss.01896)
- **MNE-Python ecosystem** — Production preprocessing pipelines adopted across University of Washington pediatric neuroimaging studies
