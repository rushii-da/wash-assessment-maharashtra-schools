# 💧 WASH Infrastructure Assessment — 39 Schools, Maharashtra

> **Public Health Analytics · Python · Full Data Pipeline · Infrastructure Gap Analysis · Hygiene Practice Assessment**

[![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)](https://python.org)
[![Framework](https://img.shields.io/badge/Framework-WHO%2FJMP-blue)](https://washdata.org)
[![Schools](https://img.shields.io/badge/Schools-39-informational)](data/)
[![SDG](https://img.shields.io/badge/SDG-6%3A%20Clean%20Water-0096c7)](https://sdgs.un.org/goals/goal6)

## Overview

A cross-sectional WASH (Water, Sanitation, Hygiene) infrastructure assessment of **39 schools across 6 districts of Maharashtra**, evaluating compliance with Indian government (Swachh Bharat Mission) and WHO/UNICEF JMP standards. The project delivers a full data pipeline from field observation to interactive dashboard, with a prioritised gap analysis and remediation cost estimate.

**Live Dashboard →** [View Interactive Dashboard](dashboard_wash.html)

---

## Key Findings

| Indicator | Compliance |
|-----------|-----------|
| Functional water access | 61.5% (24/39) |
| Adequate sanitation (functional toilets) | 48.7% (19/39) |
| Observed correct handwash practice | 41.0% (16/39) |
| Schools with separate girls' toilets | 53.8% (21/39) |
| Water quality testing conducted | 33.3% (13/39) |
| **Full WASH compliance (all criteria)** | **23.1% (9/39)** |

### Infrastructure Gap — Priority Matrix

| Priority | Intervention | Schools Affected | Est. Cost |
|----------|-------------|-----------------|-----------|
| 🔴 P1 — Critical | Toilet functionality restoration | 20 | ₹12 lakh |
| 🟠 P2 — High | Water quality testing protocol | 26 | ₹78,000 |
| 🟡 P3 — Moderate | Handwash station installation | 18 | ₹14,000 |
| 🟢 P4 — Developmental | WASH education programme rollout | 14 | ₹48,000 |

### Key Disparities

- **Urban vs Rural:** Functional water access 78% vs 47%; handwash compliance 34% lower in rural schools
- **By School Type:** Private schools — 81.6% compliance; Ashram (residential) schools — 22.8% (most critical)
- **WASH Champion Effect:** Schools with designated WASH champion show **2.4× higher handwash compliance**
- **Toilet:Pupil Ratio:** Mean 1:42 vs recommended 1:25 (GoI standard); Ashram schools at 1:68

---

## Project Structure

```
03_WASH_Maharashtra_Schools/
├── data/
│   ├── WASH_Schools_Analysis_Report.xlsx        # Full dataset with all indicators
│   ├── WASH_Schools_Analysis_Feb2025_v4.xlsx    # Final clean version
│   └── WASH_Final_Draft.xlsx                    # Analysis summary
├── reports/
│   └── WASH_Analysis_Interpretation_Guide.pdf  # Field assessment guide
├── dashboard_wash.html                          # Interactive web dashboard
└── README.md
```

---

## Methodology

### Study Population
- **39 schools** purposively sampled using maximum variation approach
- **6 districts:** Pune, Nashik, Aurangabad, Beed, Solapur, Kolhapur
- **School types:** ZP Government, Municipal, Private, Ashram (residential)
- Enrolment range: 68–842 students per school

### Assessment Framework
Based on **WHO/UNICEF Joint Monitoring Programme (JMP)** WASH in Schools indicators, aligned with:
- India's **Swachh Bharat Mission** school sanitation standards
- **SDG 6** (Clean Water and Sanitation) targets
- **Swachh Vidyalaya Puraskar** guidelines (Ministry of Education)

### Data Collection
- Structured observation checklist (18 WASH indicators)
- Direct observation by trained field teams (Feb 2025)
- Key informant interviews: headteachers and WASH staff
- Student focus group discussions (n = 78 students)
- Photographic documentation (geo-tagged)

### Data Pipeline

```
KoBoCollect/ODK Mobile Forms → Excel (Power Query cleaning)
→ Python (Pandas analysis) → WASH composite score computation
→ Gap analysis → Interactive HTML dashboard + PDF report
```

### WASH Composite Score
Weighted sum of 18 indicators across 3 domains:
- **Water** (6 indicators) — 35% weight
- **Sanitation** (7 indicators) — 40% weight  
- **Hygiene** (5 indicators) — 25% weight

Score range: 0–100 | Threshold for compliance: ≥ 65

---

## WASH Compliance by District

| District | Schools | Mean Compliance | Critical Schools |
|----------|---------|----------------|-----------------|
| Pune | 8 | 62.4% | 1 |
| Nashik | 7 | 54.8% | 2 |
| Aurangabad | 7 | 44.2% | 3 |
| Beed | 6 | 36.1% | 4 |
| Solapur | 6 | 48.9% | 2 |
| Kolhapur | 5 | 58.3% | 1 |

**Beed district** shows the most critical WASH deficits, compounded by fluoride-risk groundwater zones.

---

## Critical Recommendations

1. **Immediate:** Structural/plumbing repair for non-functional toilets in 20 schools (Priority 1)
2. **Urgent:** Water quality testing protocol + fluoride mapping in Aurangabad/Beed (Priority 2)
3. **Short-term:** Low-cost tippy-tap handwash stations in 18 schools (₹200/unit) (Priority 3)
4. **Systemic:** WASH champion designation + student hygiene clubs in all non-compliant schools (Priority 4)
5. **Policy:** Separate girls' toilet and MHM facilities required in 18 schools — critical for girl retention

---

## Limitations

- Cross-sectional snapshot — seasonal water availability variation not captured (data collected pre-monsoon)
- Self-report bias in headteacher interviews for maintenance indicators
- 39-school sample limits statistical power for subgroup analysis
- Cost estimates approximate, based on district PWD schedules
- Qualitative data from student FGDs was supplementary, not fully analysed

---

## References

1. WHO/UNICEF JMP (2023). *WASH in Schools Monitoring Report.* Geneva
2. MoE, Government of India (2022). *Swachh Vidyalaya Puraskar Guidelines*
3. UNICEF India (2020). *WASH in Schools: Maharashtra State Report*
4. Rheingans R et al. (2012). Economic costs of diarrhea related to WASH. *J Dev Eff*
5. Freeman MC et al. (2017). Impact of WASH in schools on WASH behaviours. *Lancet*

---

## Policy Context

This study contributes to evidence on **SDG 6** achievement in Maharashtra and informs the state's implementation of Swachh Bharat Mission Phase II (2020–2025). Findings were shared with district education authorities in Beed and Aurangabad as part of the project dissemination.

---

## Author

**Rushi Badgujar**  
Public Health Analytics & Data Science  
📧 rushibadgujar8@gmail.com  
🔗 [github.com/rushii-da](https://github.com/rushii-da)

---

*Field data collected with institutional permissions from Maharashtra State Education Department. No student personal data included in this repository.*
