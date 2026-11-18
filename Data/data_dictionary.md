# Data Dictionary

**Dataset:** Nigerian_Graduate_Survey_with_Salary.csv
**Records:** 3,000 graduates
**Original columns:** 15
**Columns added during cleaning:** 2 (Salary_Bracket, Career_Stage)

## Original Columns

| Column | Type | Description | Values / Range |
|--------|------|-------------|----------------|
| Graduate_ID | Text | Unique identifier for each graduate (no analytical value) | G0001 onward |
| Age | Whole number | Age of the graduate | 21 to 34 |
| Gender | Text | Gender of the graduate | Male, Female, Other |
| State_of_Origin | Text | State the graduate is from | Nigerian states (e.g. Lagos, Kano, Edo) |
| Region | Text | Geographic region (contains inconsistencies, see Data Quality Notes) | North, South, East, West |
| Urban_or_Rural | Text | Type of settlement | Urban, Rural |
| Household_Income_Bracket | Text | Household income background | Low, Middle, High |
| Field_of_Study | Text | Discipline studied | Business, Education, Engineering, Health Sciences |
| University_Type | Text | Type of institution attended | Federal, State, Private |
| GPA_or_Class_of_Degree | Text | Degree classification | First Class, Second Class Upper, Second Class Lower, Third Class |
| Has_Postgrad_Degree | Text | Whether the graduate holds a postgraduate degree | Yes, No |
| Years_Since_Graduation | Whole number | Years since graduating | 0 to 10 |
| Employment_Status | Text | Current employment status | Employed, Unemployed |
| Salary_Level | Text | Categorical salary outcome | Low-Paid, Well-Paid, Not Employed |
| Net_Salary | Whole number | Monthly net salary in naira (0 for unemployed) | 0 to about 400,000 |

## Columns Added in Power Query

| Column | Type | Logic |
|--------|------|-------|
| Salary_Bracket | Text | Net_Salary grouped into bands: 0-100k (below 100,000), 100k-200k (100,000 to 199,999), 200k-300k (200,000 to 299,999), 300k+ (300,000 and above) |
| Career_Stage | Text | Years_Since_Graduation grouped into: Early (0 to 3 years), Mid (4 to 7 years), Established (8 to 10 years) |

## Derived Datasets

| Dataset | Rows | Used for |
|---------|------|----------|
| All_Graduates | 3,000 | Employment rate and distribution analysis |
| Employed_only | 2,107 | All salary analysis |

## Data Quality Notes

- **Zero salaries:** 893 records have Net_Salary = 0. They are all Unemployed graduates, so they were kept for employment rate analysis and excluded from salary analysis.
- **Region inconsistencies:** Some states appear under more than one region (for example Edo, Lagos and Kano). Region was not used in the four research questions.
- **Text standardisation:** Trim, Clean and Capitalize Each Word were applied to all categorical columns.
- **Data types:** All columns were verified. No mismatches were found.
