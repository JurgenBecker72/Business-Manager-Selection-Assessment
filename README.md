<div align="center">

<!-- HEADER BANNER -->
<img src="assets/banner.png" alt="AX Consult Group — BM Assessment Validation Study" width="100%"/>

# Business Manager Selection Assessment
## Psychometric Validation Study · Phase 1 Pilot

[![Author](https://img.shields.io/badge/Author-Jurgen%20Becker%20PhD-1F3864?style=flat-square&logo=academia)](https://ax-assess.com)
[![Organisation](https://img.shields.io/badge/Org-AX%20Consult%20Group-2E75B6?style=flat-square&logo=github)](https://github.com/AX-Consult-Group)
[![Sector](https://img.shields.io/badge/Sector-Financial%20Services-2EB8A8?style=flat-square)](#)
[![n](https://img.shields.io/badge/Pilot%20n-27%20candidates-E8A838?style=flat-square)](#dataset)
[![Status](https://img.shields.io/badge/Status-Phase%201%20Complete-6FAD7A?style=flat-square)](#status)

</div>

---

<div align="center">
<img src="BM_Methodology_Overview.svg" alt="Business Manager Assessment — Design & Methodology Overview" width="100%"/>
</div>

---

## Project Overview

This repository documents the end-to-end psychometric validation of a revised **Business Manager (BM) Selection Assessment** commissioned by a major financial services institution (anonymised as *Client A*). The project addressed a critical limitation in the incumbent assessment battery: insufficient differentiation between candidates on technical knowledge alone.

The revised tool introduces a structured **behavioural case study** targeting four competencies identified as central to future BM success, alongside an enhanced technical test. The work spans job analysis, instrument redesign, three iterative pilot phases, Classical Test Theory (CTT) analysis, Item Response Theory (IRT) modelling, and large-sample simulation studies.

> **⚠️ Anonymisation Notice:** All candidate names, assessor identities, organisation-identifying information, and proprietary assessment tool references have been removed or pseudonymised in accordance with data protection and IP obligations. Competency names have been replaced with generic descriptors that preserve the construct meaning without disclosing proprietary intellectual property.

---

## Repository Contents

| File | Type | Description |
|------|------|-------------|
| `Dataset_Clean_Anonymized.xlsx` | Data | Pilot dataset (n=27): MCQ, T/F, behavioural ratings (RM/CE/CF/SOD), performance ratings, demographics |
| `BM_Case_Study_Technical_Manual_Anonymized_Final.docx` | Report | Full technical manual: design methodology, competency framework, pilot findings, CTT/IRT analysis, recommendations |
| `BM_Assessment_Dashboard.html` | Dashboard | Interactive analytics dashboard — score distributions, equity analysis, competency profiles, candidate table |
| `BM_Project_Flow.svg` | Graphic | End-to-end project methodology flow diagram |
| `README.md` | Documentation | This file |

---

## Competency Framework

The revised case study measures four behavioural competencies identified through structured SME workshops and job analysis:

| Code | Competency | Description |
|------|------------|-------------|
| **RM** | Relationship Management | Building and sustaining productive working relationships; fostering trust and mutual confidence |
| **CE** | Communication Effectiveness | Conveying ideas clearly and persuasively across audiences; adapting style for maximum influence |
| **CF** | Client Focus | Proactively attending to client needs; resolving issues and maintaining accountability |
| **SOD** | Strategic Opportunity Development | Developing value-adding solutions by synthesising data, constraints, and strategic priorities |

---

## Methodology

### Assessment Structure

```
┌─────────────────────────────────────────────────────────────────┐
│                    BM ASSESSMENT BATTERY                        │
├───────────────────────────┬─────────────────────────────────────┤
│      SECTION 1            │           SECTION 2                 │
│   Technical Test          │      Behavioural Case Study         │
├───────────────────────────┼─────────────────────────────────────┤
│  1A: MCQ (15 items)       │  Competency ratings (1–5 scale)     │
│  1B: True/False (6 items) │  RM · CE · CF · SOD subscales       │
│  Total: 21 items          │  4 questions × 4 competencies       │
└───────────────────────────┴─────────────────────────────────────┘
                    Total duration: 2 hours
```

### Five-Phase Design Process

| Phase | Activity | Output |
|-------|----------|--------|
| **1 · Conceptualisation** | SME workshops, job analysis, competency identification | Competency framework, scenario brief |
| **2 · Development** | Case study authoring, scoring rubric design, model answers | Draft assessment + rating form |
| **3 · Pre-pilot** | Trial on n=10 internal staff; dual-marker scoring | Revised instrument (Version 1) |
| **4 · Piloting** | Two full pilot phases on operational candidates | Pilot dataset (n=27 usable) |
| **5 · Validation** | CTT, IRT, simulation, equity analysis | This report + recommendations |

### Analysis Pipeline

| Tool | Purpose |
|------|---------|
| **Excel** | Data wrangling, restructuring, frequency summaries |
| **R** | Reliability (CTT + IRT), EFA, regression, simulation |
| **SPSS** | Descriptive and inferential statistics |
| **Tableau / HTML** | Score distributions, competency profiles, equity visualisation |

---

## Key Statistics at a Glance

| Metric | Value |
|--------|-------|
| Total pilot candidates | n = 27 |
| Section 1 mean score | 55.5% |
| Section 2 mean score | 66.7% |
| Grand total mean | 61.2% |
| Inter-rater alignment (internal) | 93% |
| Inter-rater alignment (internal vs external) | 73% |
| IRT flagged items | Section 1A: multiple; Section 1B: Q17 critical |
| Strongest performance predictor (regression) | Communication Effectiveness (CE) |

---

## Large-Sample Simulation Study

Given the small pilot sample (n=27), a **multivariate normal simulation** was employed to assess parameter stability before deployment decisions:

- **Method:** Empirical means, SDs, and covariance structure from n=27 used as population parameters
- **Simulated samples:** n=250 and n=500
- **Metrics examined:** α (Cronbach), ω (McDonald), factor loadings, IRT parameters (a, b), regression fit, intercorrelations
- **Finding:** Estimates broadly consistent across sample sizes → provisional confidence in stability, with noted caveats for flagged items

---

## IRT Analysis Summary

### Models Applied
- **2PL** (Two-Parameter Logistic) for binary items (Sections 1A and 1B)
- **GRM** (Graded Response Model) for polytomous ratings (Section 2)

### Section 1A — MCQ
- High discrimination variability across items (some a > 1.0; others near-zero or negative)
- Poor item targeting relative to candidate ability distribution
- 3 items with substantial factor loadings (λ = 0.47–0.78)
- χ² diagnostics flagged specific misfitting items for removal/revision

### Section 1B — True/False
- **Q17** effectively non-discriminating (a ≈ 0) — confirmed by EFA
- Negative Cronbach's α (−0.41) at scale level confirmed by IRT item-level diagnostics
- **Recommendation: Revise or remove Section 1B**

### Section 2 — Behavioural
- Acceptable model fit across simulated samples
- Adequate discrimination despite range restriction
- IRT reliability consistent with CTT estimates

---

## Equity & Fairness Analysis

Demographic breakdowns were examined across race, gender, qualification level, and organisational experience. Key observations:

- Score distributions were reviewed across race groups (White, Asian, African American, Mixed Race) and gender (Male/Female)
- No systematic adverse impact was identified in the pilot dataset, though sample sizes per subgroup are insufficient for definitive conclusions
- Qualification level showed expected score gradients in Section 1 (technical component)
- Formal adverse impact analysis requires the target n≥150 validation sample

---

## Key Findings

1. **Inter-rater reliability** was strong for RM and CF, lower for SOD — confirming the need for structured assessor calibration training
2. **Section 1B** (True/False) showed poor psychometric properties and should be substantially revised
3. **Technical scores** (Section 1) showed limited predictive validity against incumbent performance ratings — range restriction and criterion contamination are likely confounds
4. **Communication Effectiveness (CE)** was the only significant positive predictor in regression modelling of Section 2 totals
5. **Simulation evidence** supports cautious deployment pending full validation at scale

---

## Recommendations

- [ ] Deploy revised case study in phased validation mode — target n ≥ 150 before formal predictive validity reporting
- [ ] Revise or remove flagged Section 1A items based on IRT discrimination/fit diagnostics
- [ ] Remove or substantially redesign Section 1B (True/False)
- [ ] Implement structured assessor calibration training, with particular focus on SOD scoring
- [ ] Broaden performance criterion to capture behavioural dimensions beyond financial targets
- [ ] Conduct formal adverse impact analysis at operational validation sample sizes

---

## Author & Contact

**Jurgen Becker, PhD**
Independent Researcher & Assessment Consultant
**AX Consult Group**

[![Website](https://img.shields.io/badge/Website-ax--assess.com-1F3864?style=flat-square)](https://ax-assess.com)
[![GitHub](https://img.shields.io/badge/GitHub-AX--Consult--Group-2E75B6?style=flat-square&logo=github)](https://github.com/AX-Consult-Group)

---

<div align="center">
<sub>© AX Consult Group · All rights reserved · Anonymised for public portfolio use</sub>
</div>
