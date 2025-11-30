# Claims Analysis 

This project analyzes sample claims data from Stony Brook University Hospital to support compliance, revenue cycle operations, and clinical quality insights. The analysis uses Python and pandas to explore:

- Provider billing patterns
- Payer mix
- Most frequent diagnoses (ICD-10)
- Most frequent procedures (CPT/HCPCS)
- Relationships between service location and total charges

---

## Project Structure

```
claims-analysis/
│
├── data/
│   └── (CSV files not included in repo)
│
├── notebooks/
│   └── claims_analysis.ipynb
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Data Files (Not Included in Repo)

Place these files into the `data/` folder:

- STONYBRK_20240531_HEADER.csv
- STONYBRK_20240531_LINE.csv
- STONYBRK_20240531_CODE.csv

File meanings:
- HEADER — 1 row per claim
- LINE — 1 row per service line
- CODE — 1 row per diagnosis code

---

## How to Run the Notebook

1. Install required packages:

```
pip install -r requirements.txt
```

2. Open the notebook:

```
jupyter notebook notebooks/claims_analysis.ipynb
```

---

## Analysis Overview

The notebook includes:

- Data loading & exploration
- Provider billing analysis
- Payer mix analysis
- Top diagnoses (ICD-10)
- Top procedures (HCPCS/CPT)
- Place-of-service breakdown
- Advanced merges across HEADER/LINE/CODE
- A custom question for creative analysis

---

## Key Findings 

- **Top billing provider:** NPI 1821035601  

- **Most common primary payer:** Medicare  

- **Most common diagnosis codes:** J96.01, I10, E78.5  
  → These reflect common conditions such as acute respiratory failure, hypertension, and hyperlipidemia.

- **Most common procedure codes:** 99291, 99233, 99213  
  → These correspond to critical care services, subsequent hospital care, and office visits, indicating mixed inpatient/outpatient activity.

- **Highest-charge place of service:** Ambulatory Surgery  
  → Ambulatory surgical procedures generated the highest total charges, likely due to procedure intensity and facility fees.

### Code Definitions

**Diagnosis Codes**
- **J96.01** – Acute respiratory failure with hypoxia  
- **I10** – Essential (primary) hypertension  
- **E78.5** – Hyperlipidemia, unspecified  

**Procedure Codes**
- **99291** – Critical care, first 30–74 minutes  
- **99233** – Subsequent hospital inpatient visit, high complexity  
- **99213** – Established patient office visit, low–moderate complexity

---

## Requirements

```
pandas>=1.3.0
matplotlib>=3.4.0
seaborn>=0.11.0
```
