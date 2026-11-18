# Findings, Interpretation and Limitations

**Phase 5**

## 1. Headline Numbers

| Measure | Value |
|---------|-------|
| Graduates analysed | 3,000 |
| Overall employment rate | 70.2% |
| Average net salary (employed) | N193,913 |
| Graduates with a postgraduate degree | 20.6% |

## 2. Findings by Research Question

| RQ | Finding |
|----|---------|
| RQ1 | Private graduates earn more than Federal graduates (average N196,328 vs N188,963). State graduates earn the most (average N199,655, median N182,697). No university type leads in every field: Private leads in Business and Health Sciences, State leads in Education and Engineering, Federal leads in none. |
| RQ2 | Engineering has the highest underemployment rate (61.1%) and Education the lowest (57.4%). All four fields fall within 3.7 percentage points of each other, and more than half of employed graduates in every field are low-paid. |
| RQ3 | No salary ceiling is visible. Salary band distributions are almost identical with and without a postgraduate degree, and the top band share is 19.7% vs 19.6%. The average difference is N2,602 in favour of graduates without one. |
| RQ4 | Third Class graduates earn N27,104 less than Second Class Upper graduates at the early career stage. First Class graduates earn N997 less than Second Class Upper, so there is no extra reward at the top. |

## 3. Overall Insight

The factors Nigerian students invest most in (institution type, degree class
and postgraduate study) predict earnings far less reliably than conventional
wisdom suggests. The one clear penalty in the data is at the bottom of the
degree classification (Third Class).

## 4. Possible Explanations

These are plausible interpretations of the patterns. This dataset does not
test them, so they should be read as hypotheses.

- **Relationships and sector placement:** where a graduate lands may matter
  more than the credential they hold.
- **Grades as a screening gate:** employers may use a minimum degree class as
  a threshold and then hire on other factors, which would explain why First
  Class and Second Class Upper earn about the same.
- **Pay compression at entry level:** standardised pay grades for junior
  roles could flatten differences between institutions and fields.
- **Systemic underemployment:** the narrow spread across fields suggests the
  constraint is the number of quality jobs, not the discipline studied.

## 5. Who Benefits

| Audience | How it helps |
|----------|--------------|
| Career counsellors | Replace assumption-based advice with evidence on what predicts pay. |
| Universities | Examine why Federal graduates do not out-earn State and Private graduates despite perceived prestige. |
| Graduates | Make better decisions about postgraduate study and degree class expectations. |
| Policy makers | Underemployment is uniform across fields, which points to job creation rather than credential reform alone. |

## 6. Limitations

| Limitation | Effect on the findings |
|------------|------------------------|
| Employment outcomes are a proxy for employability | Salary and employment status show what the market paid, not graduates' skills or competence. |
| Only four fields of study | Findings cannot be generalised to all Nigerian graduates. |
| Unequal group sizes (Private n=294, Third Class n=143, First Class n=449) | Averages for small groups are less reliable. |
| No formal significance testing | RQ4 describes differences in averages and does not claim statistical significance. |
| Region and State_of_Origin inconsistencies | Region was excluded from the main analysis. |
| Survey data | Self-reported answers may carry bias. |
| Cross-sectional snapshot | Results show association, not cause, and reflect one point in time. |
| Salary period not confirmed | The dataset does not state whether Net_Salary is monthly or annual. |
| Dashboard interactivity is partial | Slicers filter the pivot tables. Charts built from formula tables (RQ2 and RQ3) do not respond to slicers. |

## 7. Recommendations

**For practice**
- Counsellors should present institution type, degree class and
  postgraduate study as factors with limited pay impact, and place more
  emphasis on sector choice, skills and networks.
- Graduates considering postgraduate study should weigh its cost against the
  absence of a clear salary premium in this sample.

**For future work**
1. Correct the Region variable using a State-to-zone mapping and add
   geographic analysis.
2. Run a one-way ANOVA on GPA class vs starting salary to test significance.
3. Add a skills or competency variable to measure employability more directly.
4. Use a larger and more balanced sample, especially for Private universities.
5. Cover more fields of study.
6. Use years since graduation as a continuous variable instead of three bands.
