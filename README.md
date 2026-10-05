# Ulcer Health Risk Analysis

Power BI dashboard analyzing 500 patient records — connecting ulcer history, H. pylori status, medication use, and lifestyle factors with ulcer severity, bleeding symptoms, and treatment outcomes.

<img width="1446" height="817" alt="project dashboard" src="https://github.com/user-attachments/assets/392d5ad8-9f39-4f64-9327-9a95c57e56cd" />


**Dashboard includes:** summary KPI cards (with year-over-year comparison indicators), an annual patient trend line, average BMI and hemoglobin trend lines, an ulcer history donut chart, an age distribution line chart, an ulcer depth bar chart, a medication distribution column chart, a pain pattern bar chart, and an interactive filter by ulcer stage.

---

## Overview

| Metric | Value |
|---|---|
| Total patients | 500 |
| Average age | 52 years |
| Average BMI | 27.4 |
| Average hemoglobin | 11.6 g/dL |
| Average ulcer size | 15.3 mm |
| Average pain severity (0–10 scale) | 5.6 |

---

## Key Findings

### 1. Patient Snapshot

| Sex | Patients |
|---|---|
| Male | 250 |
| Female | 250 |

| Age Group | Patients |
|---|---|
| 26–30 | 42 |
| 31–35 | 63 |
| 36–40 | 44 |
| 41–45 | 23 |
| 46–50 | 53 |
| 51–55 | 69 |
| 56–60 | 8 |
| 61–65 | 70 |
| 66–70 | 69 |
| 71–75 | 57 |
| 76+ | 2 |

The patient base is evenly split by sex, with the largest concentrations in the 51–55 and 61–70 age brackets.

### 2. Ulcer Profile & Risk Factors

| Ulcer History | Patients |
|---|---|
| Previous ulcer | 206 |
| None | 167 |
| Recurrent | 127 |

| H. pylori Status | Patients |
|---|---|
| Positive | 314 |
| Negative | 186 |

| Medication Type | Patients |
|---|---|
| NSAIDs | 208 |
| None | 171 |
| Aspirin | 121 |

NSAID users make up the largest share of patients with a previous ulcer history (100 of 208), a higher share than aspirin users (43 of 121) or patients on no medication (63 of 171) — consistent with NSAIDs being a known ulcer risk factor.

### 3. Clinical Severity

| Ulcer Depth | Patients |
|---|---|
| Deep | 177 |
| Superficial | 159 |
| Erosion | 114 |
| Very deep | 50 |

| Ulcer Stage | Patients |
|---|---|
| Stage 1 | 170 |
| Stage 2 | 129 |
| Stage 3 | 121 |
| Stage 4 | 80 |

| Pain Pattern | Patients |
|---|---|
| Postprandial (after eating) | 171 |
| Fasting | 129 |
| Nocturnal | 121 |
| Mixed | 79 |

### 4. Bleeding & Hospitalization

| Bleeding Symptom | Patients | Avg. Hemoglobin (g/dL) |
|---|---|---|
| None | 300 | 13.4 |
| Hematemesis | 125 | 8.3 |
| Melena | 75 | 9.5 |

| Hospitalization Required | Patients |
|---|---|
| No | 300 |
| Yes | 200 |

**Every patient with a bleeding symptom (hematemesis or melena) required hospitalization — 200 out of 200. Every patient with no bleeding symptom did not require hospitalization — 300 out of 300.** Hemoglobin also drops sharply alongside bleeding, from 13.4 g/dL (no bleeding) to 9.5 g/dL (melena) to 8.3 g/dL (hematemesis) — a clear anemia signal tied to active bleeding.

### 5. Treatment & Outcomes

| Treatment Category | Patients |
|---|---|
| Medical | 323 |
| Endoscopic | 89 |
| Surgical | 88 |

| Ulcer Outcome | Patients |
|---|---|
| Healed | 350 |
| Persistent | 150 |

Healing rate stayed close to 70% across every ulcer stage (Stage 1: 119 of 170; Stage 2: 90 of 129; Stage 3: 85 of 121; Stage 4: 56 of 80) and across every treatment category — meaning stage and treatment type did not strongly separate outcomes in this dataset.

---

## Key Insights

- **Bleeding symptoms are a near-perfect predictor of hospitalization** in this dataset — every patient with hematemesis or melena was hospitalized, and no patient without a bleeding symptom was. This is the strongest, most actionable signal in the data.
- **Hemoglobin level tracks closely with bleeding severity**, making it a reliable early flag for patients likely to need admission.
- **NSAID use is linked to a higher rate of prior ulcer history**, reinforcing the clinical link between NSAID use and ulcer recurrence.
- **62.8% of patients are H. pylori positive**, but positivity was distributed proportionally across all four ulcer stages — it did not concentrate in more severe stages in this sample.
- **Healing rate held steady at roughly 70% regardless of ulcer stage or treatment type**, suggesting that in this dataset, outcome is not being driven primarily by how advanced the ulcer was at diagnosis or which treatment path was chosen.

---

## Recommendations

1. Use bleeding symptoms (hematemesis/melena) and hemoglobin drop as the primary triage flags for hospitalization decisions, they were the clearest predictors in this data.
2. Reinforce NSAID-use screening for patients with a prior ulcer history, given the higher overlap observed between NSAID use and previous/recurrent ulcers.
3. Since healing rates were similar across stages and treatment types, investigate what other factors (adherence, follow-up timing, comorbidities) might better explain the 150 persistent cases.
4. Track hemoglobin and bleeding status longitudinally for at-risk patients to catch deterioration early, before hospitalization becomes necessary.
