# Exploratory Analysis

**Phase 2**
**Sheet:** Exploration
**Tool:** Excel Pivot Tables

## Purpose

Before answering the research questions, eight baseline pivot tables were
built to understand how the cleaned data is distributed. No final conclusions
were drawn at this stage. The observations below shaped the framing of the
RQ analysis.

## Pivot Tables

### 1. Graduate count by University Type
**Dataset:** All_Graduates

| University Type | Graduates | Share |
|-----------------|-----------|-------|
| Federal | 1,498 | 49.9% |
| Private | 294 | 9.8% |
| State | 1,208 | 40.3% |
| **Total** | **3,000** | |

**Observation:** Federal graduates make up almost half of the sample. Private
is under 10%, so Private averages need cautious interpretation.

### 2. Graduate count by Field of Study
**Dataset:** All_Graduates

| Field | Graduates | Share |
|-------|-----------|-------|
| Business | 762 | 25.4% |
| Education | 736 | 24.5% |
| Engineering | 803 | 26.8% |
| Health Sciences | 699 | 23.3% |
| **Total** | **3,000** | |

**Observation:** The four fields are fairly balanced, so cross-field
comparisons are sound.

### 3. Employment rate by University Type
**Dataset:** All_Graduates

| University Type | Employed | Unemployed | Employment rate |
|-----------------|----------|------------|-----------------|
| Federal | 1,068 | 430 | 71.3% |
| Private | 204 | 90 | 69.4% |
| State | 835 | 373 | 69.1% |
| **Total** | **2,107** | **893** | **70.2%** |

**Observation:** Federal is marginally higher, but the gap across all three
types is about 2 percentage points. University type has limited influence on
whether a graduate is employed.

### 4. Employment rate by Field of Study
**Dataset:** All_Graduates

| Field | Employed | Unemployed | Employment rate |
|-------|----------|------------|-----------------|
| Business | 541 | 221 | 71.0% |
| Education | 519 | 217 | 70.5% |
| Engineering | 545 | 258 | 67.9% |
| Health Sciences | 502 | 197 | 71.8% |

**Observation:** Engineering has the lowest employment rate and Health
Sciences the highest, but the spread is narrow.

### 5. Average salary by University Type
**Dataset:** Employed_only

| University Type | Average Net Salary (N) |
|-----------------|------------------------|
| Federal | 188,963 |
| Private | 196,328 |
| State | 199,655 |
| **Overall** | **193,913** |

**Observation:** State graduates have the highest average and Federal the
lowest. This early signal shaped RQ1.

### 6. Average salary by Field of Study
**Dataset:** Employed_only

| Field | Average Net Salary (N) |
|-------|------------------------|
| Business | 195,698 |
| Education | 195,601 |
| Engineering | 188,518 |
| Health Sciences | 196,101 |

**Observation:** Engineering has the lowest average. The other three fields
sit within about N1,500 of each other.

### 7. GPA distribution
**Dataset:** All_Graduates

| Degree class | Graduates | Share |
|--------------|-----------|-------|
| First Class | 449 | 15.0% |
| Second Class Upper | 1,522 | 50.7% |
| Second Class Lower | 886 | 29.5% |
| Third Class | 143 | 4.8% |

**Observation:** Second Class Upper dominates. First Class (449) and Third
Class (143) are smaller groups, which matters for RQ4.

### 8. Postgraduate degree breakdown
**Dataset:** All_Graduates

| Postgraduate degree | Graduates | Share |
|---------------------|-----------|-------|
| No | 2,383 | 79.4% |
| Yes | 617 | 20.6% |

**Observation:** About one in five graduates holds a postgraduate degree.

## Summary

- Overall employment rate: 70.2%.
- Average salary of employed graduates: N193,913.
- Early counterintuitive signals: State graduates earn the most, and
  Engineering has both the lowest employment rate and the lowest average salary.
- Group sizes differ (Private n=294, Third Class n=143), which is noted as a
  limitation in later phases.
