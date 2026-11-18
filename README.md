# Nigerian Graduate Employability Analysis

An end-to-end Excel analysis of how institutional and academic factors affect
employment and salary outcomes among 3,000 Nigerian graduates.

**Project type:** Capstone, Techcrush Data Analysis Program
**Team:** Group 14, Career Development Sector
**Tools:** Microsoft Excel (Power Query, Pivot Tables, Slicers, Array Formulas)

---

## Business Problem

Academic excellence is no longer a guaranteed route to job security in Nigeria.
Career guidance remains generic because little quantitative evidence links
institution type, degree class and further study to actual salary outcomes.
This project helps close that gap.

## Research Questions

| # | Question |
|---|----------|
| RQ1 | Does a Private university graduate earn more on average than a Federal university graduate? |
| RQ2 | Which field of study has the highest rate of underemployment? |
| RQ3 | Is there a salary ceiling for graduates without a postgraduate degree? |
| RQ4 | Does a higher GPA lead to a significantly different starting salary? |

## Dataset

- **File:** `Nigerian_Graduate_Survey_with_Salary.csv`
- **Size:** 3,000 records, 15 variables
- **Source:** Provided by Techcrush for the capstone project
- **Key variables:** University_Type, Field_of_Study, GPA_or_Class_of_Degree,
  Has_Postgrad_Degree, Employment_Status, Salary_Level, Net_Salary
- Full column descriptions are in `data/data_dictionary.md`.

## Methodology

1. **Data cleaning (Power Query):** type checks, trim/clean/capitalise on text
   columns, dataset split into `All_Graduates` (3,000 rows) and `Employed_only`
   (2,107 rows), and two calculated columns (`Salary_Bracket`, `Career_Stage`).
2. **Exploratory analysis:** 8 baseline pivot tables checking distributions
   and early patterns.
3. **Research question analysis:** one dedicated sheet per question using
   pivot tables, averages and medians, percentage tables and charts.
4. **Dashboard:** KPI row, four charts and interactive slicers.

## Key Findings

| Question | Finding |
|----------|---------|
| RQ1 | State university graduates earn the most (avg N199,655; median N182,697). Federal graduates earn the least. No consistent university premium exists across fields. |
| RQ2 | Engineering has the highest underemployment rate (61.1%), but all four fields fall within 3.7 percentage points of each other, which points to a systemic problem. |
| RQ3 | No salary ceiling found. Salary band distributions are almost identical for graduates with and without postgraduate degrees (avg difference of N2,602). |
| RQ4 | Third Class graduates earn about N27,100 less than Second Class Upper graduates, but First Class and Second Class Upper earn almost the same. |

**Headline KPIs:** 70.2% employment rate, N193,913 average salary (employed),
20.6% hold a postgraduate degree.

**Overall insight:** Institution prestige, grades and postgraduate credentials
predict earnings far less reliably than conventional wisdom suggests.

## Dashboard



![Dashboard](dashboard/dashboard_full.png)



## Limitations

- Employment outcomes are a proxy for employability, not a direct measure of skills.
- Only four fields of study are covered, so findings are not generalisable to all graduates.
- Private universities are a small group (294 records) and results for them need cautious reading.
- The Region variable contains State-to-Region inconsistencies and was excluded from the main analysis.
- Survey data may carry self-reporting bias.

## Repository Guide

| Folder | Contents |
|--------|----------|
| `data/` | Raw dataset and data dictionary |
| `workbook/` | Final Excel workbook (cleaning, analysis, dashboard) |
| `dashboard/` | Dashboard and chart screenshots |
| `docs/` | Step-by-step documentation of every project phase |
| `presentation/` | Proposal and final presentation decks |

## How to Reproduce

1. Open `workbook/Group14_Graduate_Analysis.xlsx` in Excel (desktop version).
2. Go to Data > Queries & Connections to review the Power Query steps.
3. Follow the sheets in order: Exploration, RQ1 to RQ4, Dashboard.
4. Medians are calculated with array formulas (Ctrl + Shift + Enter) because
   pivot tables do not support Median natively.

## Author

**Peter Ugbeda**
