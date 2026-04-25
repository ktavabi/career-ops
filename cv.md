# CV -- Kambiz Tavabi

**Location:** Seattle, WA
**Email:** ktavabi@gmail.com
**LinkedIn:** https://www.linkedin.com/in/kambiz-tavabi-93255326b/
**GitHub:** https://github.com/ktavabi

## Professional Summary
Principal Data Scientist and BI Manager with a PhD in Neuroscience and 15+ years
spanning academic neuroimaging research (UW, CHOP), open-source ML infrastructure
(MNE-BIDS, MNE-Python), and public-sector AI deployment. At Washington DOC, overseeing
4 active value areas (63 features, 5-person team) delivering 20+ Power BI dashboards and product
owner of a production NLP classifier (75.6% F1, 88.3% precision, 30x baseline) over 110K records.
Track record includes an AUC 0.86 pediatric diagnostic biomarker (Cohen's d = 3.11), a
longitudinal infant brain-language functional predictor (r = 0.73, p = 0.001), and a reading
automaticity MEG model (r = 0.67, p = 1x10-6) — all published in high-impact journals
(Biological Psychiatry, Brain and Language, Developmental Cognitive Neuroscience).
Bridges rigorous statistical methods, production Python pipelines, and non-technical
stakeholder communication across clinical, government, and open-science domains.

## Work Experience

### Washington State Department of Corrections
**Tumwater, WA**
**Manager, Business Intelligence & Operations Surveillance (BIOS)**
**May 2023 - Present**
**Research & Data Analytics Division**

---

#### EXECUTIVE SUMMARY

Oversee 4 active Agile value areas (63 features across) for the Washington DOC Business
Intelligence & Operations Surveillance unit, directing a cross-functional team of 5 analysts
to deliver BI products, applied research, ML prototypes, and automated pipelines for correctional
operations, executive results, and research programs. Deployed 20+ Power BI dashboards and a
production NLP classifier (75.6% F1, 88.3% precision, 30x random baseline) while standing up
agency-wide BI governance, Git DevOps standards, and reproducible analytical infrastructure.

---

#### KEY METRICS

- Active Agile value areas: 4 | Features delivered: 63
- Team size: 5 cross-functional analysts plus external partners
- Power BI dashboards delivered: 20+
- Recurring report cadences: daily, weekly, monthly, quarterly, annual
- NLP classifier: 75.6% micro-F1 | 88.3% precision | 30x random baseline
- NLP training corpus: 110,928 behavioral incident records | 73 incident type labels
- OOC analysis dataset: 123,291 records | 6-year span (2019 to 2025) | 39 counties
- Healthcare data: Washington APCD claims | DOC release cohort 2016 to 2022
- External partnerships: Recidiviz | Council of State Governments (CSG)

---

#### ACCOMPLISHMENTS

PRODUCT OWNERSHIP AND AGILE PROGRAM DELIVERY

- Oversee deployment and maintenance of 60+ agile features across the following areas:
  Correctional Operations, Enterprise Results, Business Operations, Research, Community
  Interactions, Process Improvement, Collaborations) by directing daily Azure DevOps sprint 
  ceremonies, backlog management, and stakeholder requirement gathering with Prisons,
  Restrictive Housing, Health Services, Reentry, HR, Security Management, Pro-Equity 
  Anti-Racism (PEAR) Misconduct workgroup, and Fentanyl Task Force.

- Agile cross-functional BI delivery by managing a 5-analyst team through
  full product lifecycle from requirements through deployment, covering 28 features
  under value area 1 (operational surveillance reports), 12 features under value area 2 (data
  analysis and research), 5 features under value area 3 (agency initiatives), 8 features
  under value area 4 (cross-unit collaboration), and 10 features under value area 5 (process
  improvements), maintaining active sprint velocity across all value areas simultaneously.


POWER BI DASHBOARD AND REPORTING INFRASTRUCTURE

- Launched 20+ Power BI dashboards and automated recurring reports spanning daily
  through annual cadences for executive and facility stakeholders by developing
  SQL ETL pipelines, Power BI semantic models, and gateway-based scheduled refresh, 
  covering domains including Reception Center processing, Washington ONE Risk Assessment 
  (WAONE), Drug and Alcohol Testing (DAT), corrections staffing, agency recidivism rates, 
  PEAR misconduct behavior and sanctions, Security Threat Groups (STG), administrative 
  segregation and maximum custody, and fentanyl task force operational tracking.

- Eliminated manual SAS-based reporting for data processing by directing
  a full SAS-to-SQL migration that enabled automated gateway refresh and removed
  recurring analyst intervention, improving reporting throughput and establishing a
  reproducible, version-controlled template-based dashboard design.

- Delivered the Agency Performance Evaluation Dashboard and Reentry Scorecard
  Dashboard as high-visibility enterprise results products for executive and
  legislative audiences by translating multi-source DOC operational data into
  stakeholder-facing Power BI semantic models.


NLP MACHINE LEARNING AND BEHAVIORAL INCIDENT CLASSIFICATION

- Designed and deployed a production-ready multi-label NLP classifier for WADOC's
  Incident Management and Reporting System (IMRS), automating classification of
  free-text correctional incident narrative reports across 73 binary incident type
  labels with 75.6% micro-F1, 88.3% precision, 60.6% exact match accuracy, and
  60.8% Jaccard score on 27,700 held-out incidents, representing a 30x improvement
  over a random baseline, by building a full scikit-learn pipeline (TfidfVectorizer
  with 15K features, unigrams plus bigrams, sublinear TF scaling, and
  MultiOutputClassifier wrapping LogisticRegression one-vs-rest) over 110,928
  labeled records sourced from a 24-table Oracle relational database.

- Engineered structured and unstructured features from multi-table correctional
  records by concatenating multi-section narrative text fields, vectorizing with
  TF-IDF (15K vocabulary, unigrams plus bigrams), and aggregating participant-level
  features (age, injury flags, hospitalization flags) to incident level via pandas
  dataops to construct multi-hot label targets.

- Validated model reliability through systematic diagnostics covering logistic
  regression weight distributions across all 15K vocabulary features (range -3.2
  to +12.7), most-predictive token identification per label (transport, ambulance,
  hospital for medical transport; prea, family, visitor as negative predictors),
  and benchmarking against 4 baselines (all-negative, age-only, random, and label
  frequency), and designed a human-in-the-loop two-phase deployment process for
  WADOC stakeholders covering expert review then label correction and fine-tuning.


GEOSPATIAL AND OPERATIONAL ANALYTICS

- Engineered an end-to-end Python analytics pipeline on 123,291 administrative
  records spanning 6 years (2019 to 2025) across a 10-table relational schema to
  profile data quality, score inter-agency cooperation across 39 counties in Washington
  State, and map geographic violator transport flows for the DOC's violator management
  process, by integrating pandas, NumPy, SciPy, GeoPandas, and Quarto HTML reproducible reporting.
  Mapping with US Census TIGER/Line shapefiles (EPSG:4326, 3857, and 2285) and NetworkX directed
  weighted graphs.

- Developed a composite county cooperation scoring algorithm (0 to 100 scale)
  combining 3 domain-weighted metrics (agency reporting completeness 40%, county
  violator acceptance policy 30%, non-DOC arrest rate 30%) across 39 counties,
  identifying King County (6,144 incoming cross-county cases) and Thurston County
  (5,555) as primary regional hubs, Pierce-to-Thurston (3,525 cases) and
  Pierce-to-King (3,054 cases) as dominant transfer corridors, and flagging
  Snohomish-to-King as an emerging capacity pressure route (slope +55.9 cases/year).

- Applied chi-square independence testing and Cramer's V association analysis
  (Cramer's V = 0.859, p < 0.001 for admission-release county pairing) to
  distinguish structurally determined data gaps from true data quality issues,
  resolving an apparent 45% missingness rate in agency name reporting to a genuine
  0.8% gap by demonstrating the field is structurally inapplicable for DOC-made
  arrests, preventing misattribution of ~45K records and redirecting remediation
  resources to the 2 facilities (SCCC, AHCC) with genuine completeness gaps.

- Identified 4,107 high-complexity individuals experiencing dual cross-county
  processing disruptions (both cross-county booking-arrest and cross-county
  admission-release) via set intersection analysis, averaging 2.1 booking and 2.2
  release cross-county events per person (max: 22 and 20 respectively), enabling
  case-level operational prioritization for the most complex violators in the system.


HEALTHCARE DATA INTEGRATION AND RESEARCH

- Directed healthcare data linkage and analysis across Washington All Payers Claims
  Database (APCD) data for the DOC release cohort (2016 to 2022) by architecting
  multi-phase analysis covering opioid prescription patterns, healthcare coverage rates,
  PTSD and opioid intervention outcomes, and opioid treatment outcomes post-release,
  translating multi-table claims schema into reproducible Quarto HTML analytical
  notebooks for population health policy applications.

BI GOVERNANCE, DEVOPS, AND PROCESS IMPROVEMENT

- Established RDA-wide Power BI governance including a centralized PBI landing page,
  production table quality assurance standards, dashboard template alignment, and
  permission management by directing process improvement features covering
  Agile user guides, sprint ceremony formalization, Git repository skeleton files,
  README and CHANGELOG standards, and peer review pull request workflows in
  Azure DevOps, reducing onboarding time for new analysts and standardizing delivery
  quality across all value areas.

- Stood up Positron and VS Code IDE configurations (JSON settings and extensions)
  for R, SQL, and Markdown workflows, enabling consistent development environments
  across team members, and directed RDA strategic planning alignment contributing 
  BIOS program priorities to the agency planning cycle.

---

#### PUBLICATIONS AND TECHNICAL DELIVERABLES

WADOC Recidivism Measure White Paper (2026)
Women's Mental Health Research Paper (2025)

---

#### TECHNICAL SKILLS DEMONSTRATED

Python | pandas | NumPy | scikit-learn | Logistic Regression | GeoPandas | NetworkX
| SciPy | Matplotlib | Seaborn | Missingno | Quarto | R | ggplot2 | reshape2 | R Markdown
| Regression | Correlation | Quarto | R | ggplot2 | reshape2 | R Markdown | ANOVA | Regression 
| Correlation | Effect Sizes (Cohen's d) | Chi-square Testing | Cramer's V | A/B Testing
Power BI | Semantic Models | Gateway Refresh | SQL (T-SQL) | ETL Pipeline Design
| Azure DevOps | Git | Agile Sprint Management | Backlog Management | Product Ownership |
Stakeholder Requirement Gathering | Multi-label NLP Classification | TF-IDF | One-vs-Rest Strategy |
Text Feature Engineering | Geospatial Analysis | US Census TIGER/Line Shapefiles | EPSG Projections
Directed Network Graphs | Reproducible Reporting | Data Quality Auditing
Structured Missingness Analysis | Composite Scoring Algorithm Design
Positron | VS Code | JSON Configuration | Power BI Governance
Healthcare Claims Data (APCD) | Correctional Data Systems | Oracle/OMNI | GCS
Cross-functional Team Leadership | Mentorship | Grant Portfolio Management

---

#### FUNDING AND PARTNERSHIPS

Council of State Governments (CSG) Justice Center

---

### Institute for Learning & Brain Sciences, University of Washington
**Seattle, WA**
**Research Science Engineer**
**2011 - 2023**

---

#### EXECUTIVE SUMMARY

Architected scalable Python and MATLAB neuroimaging pipelines across a 12-year program
spanning pediatric speech, reading, and language development research, delivering 4
peer-reviewed publications (Journal of Open Source Software, Journal of Neuroscience
Methods, Developmental Cognitive Neuroscience, Brain and Language) and open-source
infrastructure adopted internationally. Translated high-dimensional MEG time-series
from infant through school-age cohorts into validated predictive models and
reproducible analytical frameworks under $2M+ in NIH, NSF, and foundation-funded
initiatives.

---

#### KEY METRICS

- Tenure: 12 years | 2011 to 2023
- Publications: 4 peer-reviewed | JOSS, JNeurosci Methods, Dev Cog Neurosci, Brain Lang
- Open source: MNE-BIDS co-developer | 15+ international contributors at publication
- Cohorts: N = 42 school-age reading study | N = 27 infant longitudinal study
- Longitudinal follow-up: Vocabulary outcomes at 18, 21, 24, 27, and 30 months
- Signal quality improvement: ~10 dB noise floor reduction via OTP pipeline
- Effect: r = 0.73 vocabulary-brain correlation (p = 0.001) | r = 0.67 cross-task
  reading skill correlation (p = 1x10-6)
- Grant portfolio: $2M+ managed across NIH R01, NSF BCS, NICHD R21, NIMH, and
  philanthropic funding streams

---

#### ACCOMPLISHMENTS

OPEN-SOURCE PLATFORM ENGINEERING AND INFRASTRUCTURE

- Co-architected MNE-BIDS, a Python package standardizing electrophysiological
  neuroimaging data into Brain Imaging Data Structure (BIDS) format, enabling
  automatic analysis pipelines, anonymized data sharing, and MEG/EEG-to-MRI
  coregistration at scale, by contributing to core conversion routines validated
  against the BIDS validator and tested continuously on Windows, macOS, and Linux
  via the MNE-Python ecosystem serving a growing international user base of 15+
  contributors at time of publication.

- Reduced data preparation time from hours to minutes for MEG and EEG datasets by
  engineering BIDS-compliant metadata extraction, file reorganization, and format
  conversion utilities within MNE-BIDS, supporting adoption at major institutions
  including the Martinos Center for Biomedical Imaging and serving as a dependency
  in downstream pipelines including MNE-study-template.

- Launched production-grade MEG preprocessing pipelines in MNE-Python across all
  UW I-LABS studies by implementing temporal signal space separation (tSSS),
  oversampled temporal projection (OTP), signal space projection (SSP), continuous
  head position compensation, and automated artifact rejection via the autoreject
  package, covering participant cohorts spanning 14-month-old infants through
  school-age children ages 7 to 12.


MEG SIGNAL QUALITY AND NOISE SUPPRESSION

- Drove a ~10 dB reduction in MEG noise floor in empty room recordings and improved
  single-trial source localization error significantly (F(1,31) = 32.54, p < 0.001)
  by contributing to validation of a combined oversampled temporal projection (OTP)
  and temporal signal space separation (tSSS) pipeline, demonstrating joint operation
  has the greatest effect when SNR is low or when detecting high-frequency
  oscillations (HFO) relevant to clinical epilepsy applications.

- Demonstrated inter-trial coherence z-score improvements across the 100 to 1000 Hz
  spectrum for high-frequency somatosensory evoked fields at ~20 ms post-stimulus by
  characterizing OTP plus tSSS performance on 2852-trial median nerve datasets, with
  HFO topography becoming clearly identifiable only after noise suppression, advancing
  non-invasive detection of seizure-onset biomarkers.

- Quantified SNR improvement interactions between OTP and noise suppression method
  type across single-trial (F(2,62) = 326.30, p < 0.001) and multi-trial
  (F(2,62) = 13.18, p < 0.001) phantom recordings by executing two-way repeated
  measures ANOVAs across 32 calibrated dipole sources, establishing parameter
  recommendations (tSSS correlation limit range 0.98 to 0.999) now applicable to
  any multichannel MEG system.


INFANT LANGUAGE DEVELOPMENT AND LONGITUDINAL PREDICTION

- Engineered the first MEG source modeling study of 14-month-old infants during
  familiar and unfamiliar word processing, delivering statistically significant right
  inferior frontal cortex (IFC) activity predictions of vocabulary growth from 18 to
  27 months (beta = 0.51, 95% CI 0.24 to 0.78, p = 0.001) by designing and
  executing data acquisition, surrogate MRI head modeling, unconstrained dSPM source
  localization, and linear mixed effects growth curve modeling across a 22-infant
  longitudinal cohort with 5 CDI follow-up time points.

- Identified a bidirectional right frontal cortex signature of language learning
  efficiency -- early window (150 to 300 ms) right IFC activation predicting faster
  vocabulary growth (p = 0.001) while late window (600 to 900 ms) activation
  predicting slower growth (p = 0.077, trend) -- by applying arcsine-transformed
  growth curve mixed models with Spearman rank correlation at individual follow-up
  visits, quantifying the attentional processing continuum from efficiency to
  cognitive effort in pre-verbal infants.

- Resolved a 27-month longitudinal vocabulary-brain correlation of r = 0.73
  (p = 0.001) between right IFC MEG response and productive word count by building
  an end-to-end pipeline spanning temporal signal space separation (tSSS) with
  correlation limit 0.98, MaxFilter head position compensation, MNE-Python movement
  correction targeting position [0,0,40] mm, autoreject-based trial exclusion, and
  HCP multimodal parcellation (HCPMMP1) ROI extraction -- implemented from raw
  acquisition through statistical reporting without prior MEG-in-infants precedent.


READING DEVELOPMENT AND AUTOMATICITY IN SCHOOL-AGE CHILDREN

- Isolated a cross-task reading-skill biomarker achieving r = 0.67 (p = 1x10-6)
  correlation between word-selective STG responses during lexical decision and
  fixation tasks by architecting a 306-channel MEG dSPM source localization pipeline
  with spatiotemporal cluster permutation correction (2000 permutations, p < 0.001)
  across N = 42 children ages 7 to 12, demonstrating that automatic STG activation
  in skilled readers is statistically equivalent across active reading and
  attention-diverted conditions.

- Delivered STG reading-skill correlation of r = 0.50 (p = 0.0006) and r = 0.48
  (p = 0.001) in lexical decision and fixation tasks respectively by implementing
  individualized boundary element model (BEM) source spaces with 10242 dipoles per
  hemisphere, iterative L2 minimum-norm dSPM estimation with shrunk noise
  covariance, and non-linear spherical morphing to FreeSurfer fsaverage template --
  establishing automatic left STG activation as a hallmark of skilled reading
  independent of task.

- Proved that left STG reading skill response is age-independent (multivariate
  regression: age coefficient non-significant, TOWRE coefficient p = 0.002) by
  running 3 regression models against TOWRE, Woodcock-Johnson BRS, and Reading
  Fluency scores while covarying age, confirming automaticity reflects reading
  circuit maturation rather than chronological development in first through fourth
  grade children.


PIPELINE INFRASTRUCTURE, REPRODUCIBILITY, AND OPEN SCIENCE

- Standardized MEG data management for I-LABS across 12 years of pediatric studies
  by deploying MNE-BIDS workflows that automated metadata extraction, enforced
  consistent file naming, enabled BIDS-validator compliance, and reduced per-study
  preprocessing setup from days to hours, directly supporting reproducibility across
  infant, toddler, and school-age cohorts.

- Advanced high-frequency oscillation detectability for clinical translation by
  implementing OTP plus tSSS combined pipelines in MNE-Python showing ~2x z-score
  improvement above baseline noise for somatosensory HFO signals in the
  100 to 1000 Hz range, with direct applicability to epilepsy seizure-onset zone
  localization using non-invasive MEG.

- Contributed to a 15-contributor international open-source software release
  (MNE-BIDS, Journal of Open Source Software, DOI 10.21105/joss.01896) funded by
  NIH NINDS R01-NS104585, BRAIN Initiative NIMH 1R24MH114705, Academy of Finland,
  and ERC Starting Grant, establishing BIDS electrophysiology support across MEG,
  EEG, and iEEG modalities within the MNE-Python ecosystem.

---

#### PUBLICATIONS

Clarke M., Larson E., Tavabi K., Taulu S. (2020). Effectively combining temporal
projection noise suppression methods in magnetoencephalography.
Journal of Neuroscience Methods, 341, 108700.
DOI: 10.1016/j.jneumeth.2020.108700

Appelhoff S., Sanderson M., Brooks T.L., van Vliet M., Quentin R., Holdgraf C.,
Chaumon M., Mikulan E., Tavabi K., Hochenberger R., Welke D., Brunner C.,
Rockhill A.P., Larson E., Gramfort A., and Jas M. (2019). MNE-BIDS: Organizing
electrophysiological data into the BIDS format and facilitating their analysis.
Journal of Open Source Software, 4(44), 1896.
DOI: 10.21105/joss.01896

Bosseler A.N., Clarke M., Tavabi K., Larson E.D., Hippe D.S., Taulu S., Kuhl P.K.
(2021). Using magnetoencephalography to examine word recognition, lateralization,
and future language skills in 14-month-old infants.
Developmental Cognitive Neuroscience, 47, 100901.
DOI: 10.1016/j.dcn.2020.100901

Joo S.J., Tavabi K., Caffarra S., Yeatman J.D. (2021). Automaticity in the reading
circuitry. Brain and Language, 214, 104906.
DOI: 10.1016/j.bandl.2020.104906

---

#### TECHNICAL SKILLS DEMONSTRATED

Python | MNE-Python | MNE-BIDS | MATLAB | FreeSurfer | dSPM Source Localization
Boundary Element Modeling (BEM) | Signal Space Separation (SSS) | Temporal SSS (tSSS)
Oversampled Temporal Projection (OTP) | Signal Space Projection (SSP)
Spatiotemporal Cluster Permutation Testing | Linear Mixed Effects Models (LMM)
Growth Curve Modeling | Random Forest | Dimensionality Reduction
Brain Imaging Data Structure (BIDS) | Autoreject | HCP Multimodal Parcellation
MEG Preprocessing Pipelines | Pediatric Neuroimaging | Infant MEG | dSPM
High-Frequency Oscillations (HFO) | Epilepsy Biomarkers | Reading Neuroscience
Language Development | Longitudinal Study Design | Open Source Software Development
Git | GitHub | Continuous Integration | Cross-platform Testing (Windows macOS Linux)
NIH Grant-Supported Research | NSF | NICHD | NIMH | Interdisciplinary Collaboration
Reproducible Research | Data Standardization | Scientific Software Engineering

---

#### FUNDING SUPPORTED

NIH NINDS R01-NS104585
NIH NICHD R21HD092771 and R01HD09586101
NSF BCS 1551330
BRAIN Initiative and NIMH 1R24MH114705
National Research Foundation of Korea (NRF) 2018K2A9A2A20088926 and 2019R1C1C1009383
European Commission H2020-MSCA-IF-2018-837228-ENGRAVING
Academy of Finland Grant 310988
ERC Starting Grant SLAB ERC-YStG-676943
Bezos Family Foundation
Simms Mann Foundation
Ready Mind Project Campaign, University of Washington
Washington State Life Sciences Discovery Fund (LSDF)
Google Summer of Code 2019

---

### Children's Hospital of Philadelphia, Department of Radiology
**Philadelphia, PA**
**Post-Doctoral Researcher**
**Lurie Family Foundations MEG Imaging Center**
**2008 - 2011**

---

#### EXECUTIVE SUMMARY

Architected a 3-publication MEG neuroimaging program spanning clinical ASD biomarker
validation (Biological Psychiatry), spectral-temporal lexical access (NeuroReport), and
oscillatory repetition suppression (NeuroReport) across 96+ participants and 2 independent
cohorts. Delivered an ROC-validated language-impairment classifier (AUC 0.86, sensitivity
82.4%, specificity 71.2%) and established MEG latency delay as a passive, attention-free
pediatric neurodiagnostic biomarker under NIH R01-DC008871.

---

#### KEY METRICS

- AUC: 0.86 | ROC analysis | Biological Psychiatry 2011
- Effect size: Cohen d = 3.11 | ASD+LI vs. neurotypical | p < 0.001
- Auditory processing delay detected: ~51 ms | p < 0.001
- Peer-reviewed publications: 3 | Biological Psychiatry, NeuroReport (x2)
- Pediatric cohort: N = 51 ASD, N = 27 neurotypical controls | ages 6-15
- Diagnostic sensitivity: 82.4% | Specificity: 71.2% | MMF latency biomarker
- Grant supported: NIH R01-DC008871 | Nancy Lurie Marks Family Foundation

---

#### ACCOMPLISHMENTS

BIOMARKER VALIDATION AND CLINICAL CLASSIFICATION

- Validated the first MEG-derived biomarker for language impairment in autism spectrum
  disorder achieving AUC 0.86 (p < 0.001), sensitivity 82.4%, and specificity 71.2% by
  architecting a blinded ROC analysis pipeline applied to magnetic mismatch field latency
  features extracted from 78 pediatric participants (51 ASD, 27 neurotypical controls)
  ages 6 to 15.

- Delivered a Cohen d = 3.11 group separation between ASD-with-language-impairment and
  neurotypical children by engineering a 4-condition auditory oddball MEG paradigm producing
  a 51 ms latency gap (228.73 ms vs. 177.27 ms, p < 0.001) that remained significant after
  covarying nonverbal IQ and ruling out gender confounds (F(1,111) = 1.29, p = 0.26).

- Demonstrated a graded neurobiological stratification index across 3 diagnostic subgroups:
  neurotypical (177.27 +/- 2.72 ms), ASD without language impairment (208.68 +/- 3.26 ms),
  ASD with language impairment (228.73 +/- 5.82 ms), with all pairwise Bonferroni-corrected
  contrasts significant at p < 0.01, mapping directly to clinical language severity.

- Resolved a decade of contradictory MMN findings in the ASD literature by scaling the
  cohort to N = 78 participants recruited from 3 clinical sites, achieving 5 to 8 times the
  sample size of prior studies and providing sufficient power to detect medium-to-large
  effects (Cohen d range 1.37 to 3.11).


BLINDED ANALYSIS AND REGULATORY-GRADE METHODS

- Executed all MEG source modeling and mismatch field scoring blinded to diagnostic group
  by applying a pre-specified standard bilateral superior temporal gyrus source model with
  fixed MNI coordinates (x = 37.27, y = 19.71, z = 17.35) across all 4 oddball tasks per
  subject, eliminating analyst bias and enabling a reproducible observer-independent pipeline
  consistent with FDA biomarker qualification frameworks.

- Enforced pre-registered acceptance criteria for mismatch field scoring and applied
  Bonferroni correction across all multi-comparison contrasts, meeting the methodological
  standard for regulatory-grade biomarker evidence in pediatric neuroimaging.

- Deployed linear mixed modeling across 301 observations to handle correlated repeated
  measures, unequal group variance, and unbalanced trial counts between ASD and neurotypical
  cohorts, producing bias-corrected group estimates appropriate for clinical dataset
  irregularities common in pediatric populations.


SPECTRAL-TEMPORAL OSCILLATORY BIOMARKER FINDINGS

- Established a left-lateralized theta-alpha (6 to 14 Hz) ERD as a lexical access signature
  achieving a hemisphere-by-lexicality interaction of F(1,17) = 11.42, p < 0.01,
  effect size eta-p-squared = 0.40, with words driving 84% greater left superior temporal
  gyrus suppression than acoustically matched nonwords (-11.13 vs. -6.04 nAm, p < 0.01)
  by designing a SAM beamforming pipeline across 18 participants and 120 stimulus conditions.

- Isolated a millisecond-precise gamma-band lexical access marker (40 to 50 Hz ERS peak at
  410 ms, within 35 ms of average word uniqueness point, effect size eta-p-squared = 0.35)
  distinguishing high-frequency from low-frequency words, by architecting a Morlet wavelet
  time-frequency decomposition protocol applied to bilateral auditory virtual sensors.

- Quantified a 19% attenuation of theta-alpha ERD power under low-frequency word repetition
  (-9.41 vs. -11.40 nAm, p < 0.05, effect size eta-p-squared = 0.37) as the first
  oscillatory neural correlate of the behavioral Frequency Attenuation Effect, resolved to
  a 70 ms precision window (355 to 425 ms post target onset, p < 0.001).

- Demonstrated bilateral auditory cortex habituation with a 35% reduction in dipole field
  strength between prime and target word presentations (14.64 vs. 22.49 nAm,
  F(1,12) = 31.72, p < 0.001, eta-p-squared = 0.73), strengthening translational evidence
  for MEG-derived priming metrics as candidate neurodiagnostic indicators.


CROSS-PAPER PROGRAM AND GRANT CONTRIBUTION

- Built a unified spectral-temporal MEG characterization framework across 3 publications,
  creating a continuous methodological lineage from basic oscillatory neuroscience to
  translational pediatric diagnostic application under NIH R01-DC008871 (PI: T.P.L. Roberts)
  and the Nancy Lurie Marks Family Foundation grant.

- Contributed core analytical infrastructure including SAM beamforming pipelines, bilateral
  STG virtual sensor extraction, Morlet wavelet time-frequency representation computation,
  and linear mixed model statistical validation directly supporting all 3 funded publications.

- Demonstrated millisecond-precision gamma-band lexical access timing while in parallel
  isolating a clinically actionable 51 ms auditory processing delay in ASD children,
  bridging basic oscillatory neuroscience and pediatric neurodiagnostics within a single
  3-year postdoctoral program across 96+ participants in 2 independent cohorts.

---

#### PUBLICATIONS

Roberts T.P.L., Cannon K.M., Tavabi K., Blaskey L., Khan S.Y., Monroe J.F., Qasmieh S.,
Levy S.E., Edgar J.C. (2011). Auditory magnetic mismatch field latency: a biomarker for
language impairment in autism. Biological Psychiatry, 70(3), 263-269.
DOI: 10.1016/j.biopsych.2011.01.015

Tavabi K., Embick D., Roberts T.P.L. (2011). Spectral-temporal analysis of cortical
oscillations during lexical processing. NeuroReport, 22(10), 474-478.
DOI: 10.1097/WNR.0b013e3283476b84

Tavabi K., Embick D., Roberts T.P.L. (2011). Word repetition priming induced oscillations
in auditory cortex: a magnetoencephalography study. NeuroReport, 22(17), 887-891.
DOI: 10.1097/WNR.0b013e32834ca576

---

#### TECHNICAL SKILLS DEMONSTRATED

Magnetoencephalography (MEG) | Synthetic Aperture Magnetometry (SAM) | Beamforming
Source Analysis | Equivalent Current Dipole Modeling | Time-Frequency Representation (TFR)
Morlet Wavelet Analysis | Event-Related Desynchronization (ERD) | Event-Related
Synchronization (ERS) | Mismatch Field (MMF) | Mismatch Negativity (MMN) | ROC Analysis
Linear Mixed Modeling | Repeated Measures ANOVA | Bonferroni Correction | MATLAB
Python | BESA Source Modeling | Biomarker Validation | Pediatric Neuroimaging
Clinical Cohort Design | Blinded Analysis | NIH Grant-Supported Research
Translational Neuroscience | Auditory Cognitive Neuroscience | Language Processing
Autism Spectrum Disorder (ASD) | Pediatric Clinical Research | IRB Protocols

---

#### FUNDING

NIH R01-DC008871 (PI: Timothy P.L. Roberts)
Nancy Lurie Marks Family Foundation
Pennsylvania Department of Health

## Education

- PhD in Neuroscience, University of Münster, Germany (2007)
- MSc in Psychology, University of Oregon, USA (2004)
- BSc in Physiology, University of California at Los Angeles, USA (2000)
