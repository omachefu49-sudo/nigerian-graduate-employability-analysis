# Data Cleaning and Transformation Log

**Phase 1: Power Query**
**Tool:** Microsoft Excel (Power Query Editor)
**Source file:** Nigerian_Graduate_Survey_with_Salary.csv (3,000 rows, 15 columns)

## 1. Data Quality Issues Identified

### Issue 1: Zero salary records
893 records have Net_Salary = 0. These are not errors. They correspond to
Unemployed graduates, for whom salary does not apply. Including them in
salary analysis would pull every average down, so they had to be handled
deliberately.

**Decision:** keep them for employment rate analysis and exclude them from
all salary analysis.

### Issue 2: Region and State_of_Origin inconsistencies
Some states appear under more than one region. For example, Edo appears under
both North and East, and Lagos, Kano and Oyo also appear under regions they do
not belong to. This makes the Region column unreliable for geographic analysis.

**Decision:** Region was not used in any of the four research questions.
The issue is recorded as a limitation. A corrected region mapping built from
State_of_Origin is recommended for future work.

### Issue 3: Potential text inconsistencies
Survey data often contains stray spaces and inconsistent capitalisation
(for example "federal" and "Federal"), which split categories in pivot tables.

**Decision:** standardise all categorical text columns as a precaution.

### Checks that found no problems
- Data types: no mismatches in any column.
- Duplicate Graduate_IDs: none.
- Null values: none.
- Negative salaries: none.

## 2. Transformation Steps

| Step | Action | Purpose |
|------|--------|---------|
| 1 | Imported the CSV through Data > Get Data > From Text/CSV and chose **Transform Data** | Load into Power Query Editor so all cleaning happens before the data reaches a worksheet |
| 2 | Verified data types | Confirmed Net_Salary, Age and Years_Since_Graduation are Whole Number, and categorical columns are Text |
| 3 | Applied **Trim**, **Clean** and **Capitalize Each Word** to all categorical text columns | Remove stray spaces and non-printable characters, and enforce consistent capitalisation |
| 4 | Duplicated the query and renamed the copies **All_Graduates** and **Employed_only** | Create two purpose-built datasets |
| 5 | Filtered Employed_only to Employment_Status = Employed | Keep 2,107 employed records for salary analysis |
| 6 | Added conditional column **Salary_Bracket** to both queries | Group Net_Salary into bands for distribution analysis |
| 7 | Added conditional column **Career_Stage** to both queries | Group Years_Since_Graduation to control for experience |
| 8 | Used Close & Load To > Table > New Worksheet | Load both datasets to separate sheets |

Text columns standardised in Step 3: University_Type, Field_of_Study,
Employment_Status, Salary_Level, GPA_or_Class_of_Degree, Region,
Has_Postgrad_Degree, Urban_or_Rural, Gender, State_of_Origin.

## 3. Calculated Column Logic

### Salary_Bracket

| Condition | Label |
|-----------|-------|
| Net_Salary < 100,000 | 0-100k |
| Net_Salary < 200,000 | 100k-200k |
| Net_Salary < 300,000 | 200k-300k |
| Otherwise | 300k+ |

### Career_Stage

| Condition | Label |
|-----------|-------|
| Years_Since_Graduation < 4 | Early (0 to 3 years) |
| Years_Since_Graduation < 8 | Mid (4 to 7 years) |
| Otherwise | Established (8 to 10 years) |

Career_Stage is used in RQ4 to isolate Early career graduates as the closest
proxy for starting salary.

## 4. Output

| Dataset | Rows | Columns | Used for |
|---------|------|---------|----------|
| All_Graduates | 3,000 | 17 | Employment rate and distribution analysis |
| Employed_only | 2,107 | 17 | All salary analysis |

Both row counts were checked after loading.

## 5. Why Two Datasets

Mixing 893 zero-salary records into salary calculations would artificially
lower every average and median. Splitting the data keeps employment rate
analysis (which needs all 3,000 records) separate from salary analysis
(which needs employed graduates only).
