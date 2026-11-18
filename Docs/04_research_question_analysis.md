# Research Question Analysis

**Phase 3**
**Sheets:** RQ1, RQ2, RQ3, RQ4
**Tool:** Excel Pivot Tables, array formulas and charts

Each research question has its own sheet. Salary questions use the
`Employed_only` dataset (2,107 rows). Employment and distribution questions
use `All_Graduates` (3,000 rows).

---

## RQ1: University Type vs Earnings

**Question:** Does a Private university graduate earn more on average than a
Federal university graduate?
**Dataset:** Employed_only

### Method
1. Pivot table with University_Type in Rows and Average of Net_Salary in Values.
2. Median salary added beside the pivot using an array formula, because pivot
   tables have no Median option:
   `=MEDIAN(IF(Employed_only[University_Type]="Federal",Employed_only[Net_Salary]))`
   confirmed with Ctrl + Shift + Enter, repeated for Private and State.
3. Second pivot with Field_of_Study and University_Type nested in Rows, to test
   whether the university effect holds within each field.
4. Clustered column chart comparing average and median salary.

### Results: average vs median

| University Type | Average (N) | Median (N) | Gap (N) |
|-----------------|-------------|------------|---------|
| Federal | 188,963 | 167,089 | 21,874 |
| Private | 196,328 | 173,822 | 22,506 |
| State | 199,655 | 182,697 | 16,958 |

Both measures were used because a few high earners pull averages upward. The
median shows what a typical graduate earns.

### Results: average salary by field and university type (N)

| Field | Federal | Private | State | Highest |
|-------|---------|---------|-------|---------|
| Business | 185,042 | 211,756 | 204,350 | Private |
| Education | 192,245 | 180,072 | 203,759 | State |
| Engineering | 179,563 | 192,050 | 200,814 | State |
| Health Sciences | 200,423 | 203,498 | 188,225 | Private |

### Finding
- Directly answering the question: Private graduates earn more than Federal
  graduates, by about N7,365 on average and N6,733 at the median.
- State graduates earn the most overall (average N199,655, median N182,697).
  Federal graduates earn the least.
- No university type leads consistently. Private leads in Business and Health
  Sciences, State leads in Education and Engineering, and Federal leads in
  none of the four fields.
- Private has only 294 records in the sample, so Private results need
  cautious reading.

---

## RQ2: Underemployment by Field of Study

**Question:** Which field of study has the highest rate of underemployment?
**Dataset:** All_Graduates

### Definition
Underemployment rate = Low-Paid graduates / Employed graduates x 100,
where Employed = Low-Paid + Well-Paid (Not Employed is excluded).

### Method
1. Pivot table with Field_of_Study in Rows, Salary_Level in Columns and
   Count of Graduate_ID in Values.
2. Calculation table beside the pivot using direct cell references.
3. Column chart of underemployment rate by field.

### Results

| Field | Low-Paid | Well-Paid | Employed total | Underemployment rate |
|-------|----------|-----------|----------------|----------------------|
| Business | 327 | 214 | 541 | 60.4% |
| Education | 298 | 221 | 519 | 57.4% |
| Engineering | 333 | 212 | 545 | 61.1% |
| Health Sciences | 300 | 202 | 502 | 59.8% |
| **All fields** | **1,258** | **849** | **2,107** | **59.7%** |

### Finding
- Engineering has the highest underemployment rate (61.1%) and Education the
  lowest (57.4%).
- The spread between highest and lowest is only 3.7 percentage points.
- More than half of employed graduates in every field are low-paid, so
  underemployment looks systemic rather than field-specific.

---

## RQ3: Postgraduate Degree and the Salary Ceiling

**Question:** Is there a salary ceiling for graduates without a postgraduate
degree?
**Dataset:** Employed_only

### Method
1. Pivot table with Has_Postgrad_Degree in Rows and Average and Max of
   Net_Salary in Values.
2. Pivot table with Salary_Bracket in Rows, Has_Postgrad_Degree in Columns
   and Count of Graduate_ID in Values.
3. Percentage table (band count / group total x 100), because the two groups
   differ in size.
4. Clustered column chart of salary band distribution.

### Results: average and maximum salary

| Postgrad degree | Graduates | Average (N) | Maximum (N) |
|-----------------|-----------|-------------|-------------|
| No | 1,659 | 194,466 | 399,641 |
| Yes | 448 | 191,864 | 399,479 |

### Results: salary band distribution

| Salary band | No postgrad | Yes postgrad |
|-------------|-------------|--------------|
| 0-100k | 20.6% | 21.7% |
| 100k-200k | 38.8% | 39.3% |
| 200k-300k | 21.0% | 19.4% |
| 300k+ | 19.7% | 19.6% |

### Finding
- No salary ceiling is visible. Graduates without a postgraduate degree
  reach the top band as often as those with one (19.7% vs 19.6%).
- The average difference is N2,602, and it favours the group without a
  postgraduate degree.
- In this dataset a postgraduate degree alone does not predict higher pay.
  Any benefit may come through channels the data does not capture.

---

## RQ4: GPA vs Starting Salary

**Question:** Does a higher GPA result in a significantly different starting
net salary?
**Dataset:** Employed_only, filtered to Career_Stage = Early (0 to 3 years
since graduation), used as the closest proxy for starting salary.

### Method
1. Pivot table with GPA_or_Class_of_Degree in Rows, Average of Net_Salary in
   Values and Career_Stage as a filter set to Early.
2. Rows ordered First Class, Second Class Upper, Second Class Lower, Third Class.
3. Line chart of average starting salary by degree class.

### Results

| Degree class | Average starting salary (N) |
|--------------|-----------------------------|
| First Class | 201,310 |
| Second Class Upper | 202,307 |
| Second Class Lower | 184,683 |
| Third Class | 175,203 |

### Finding
- Third Class graduates earn N27,104 less than Second Class Upper graduates.
- First Class graduates earn N997 less than Second Class Upper graduates, so
  there is no extra reward at the top.
- GPA shows a penalty at the low end but diminishing returns at the top.

### Limitation on significance
A formal significance test (such as one-way ANOVA with the Data Analysis
ToolPak) was not run. The finding describes the pattern in the averages and
does not claim statistical significance. Running ANOVA is listed as a next step.

---

## Overall Insight

Where a graduate studied, what they studied, their degree class and whether
they hold a postgraduate degree predict earnings less reliably than
conventional wisdom suggests.
