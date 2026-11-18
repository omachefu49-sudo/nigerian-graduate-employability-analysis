# Project Brief

## Overview

| Item | Detail |
|------|--------|
| Project title | Analysis of Graduate Employability Trends |
| Subtitle | Investigating Institutional Backgrounds and Labour Market Outcomes |
| Program | Techcrush Data Analysis Capstone |
| Team | Group 14 |
| Sector | Career Development |
| Proposal date | 24 May 2026 |
| Proposal status | Approved |
| Primary tool | Microsoft Excel (Power Query, Pivot Tables, Slicers) |

## Topic

How University Type (Federal, State, Private) and Field of Study affect the
employment status and salary levels of Nigerian graduates.

The project treats employment outcomes (employment status and net salary) as
proxy measures for employability, because the dataset has no direct measure
of skills or competencies.

## Statement of the Problem

Academic excellence is no longer a guarantee of job security in Nigeria.
Little quantitative evidence links specific institution types and degree
classes to actual net salaries. As a result, career development
interventions remain generic and less effective for high-potential graduates.

## Objectives

1. Compare employment rates across Private, State and Federal universities.
2. Analyse the distribution of net salaries across fields of study.
3. Evaluate whether GPA significantly affects starting salaries.
4. Assess the impact of postgraduate degrees on salary outcomes.

## Research Questions

| # | Question | Linked sheet |
|---|----------|--------------|
| RQ1 | Does a Private university graduate earn more on average than a Federal university graduate? | RQ1 |
| RQ2 | Which field of study has the highest rate of underemployment? | RQ2 |
| RQ3 | Is there a salary ceiling for graduates without a postgraduate degree? | RQ3 |
| RQ4 | Does a higher GPA result in a significantly different starting net salary? | RQ4 |

## Dataset

- **File:** Nigerian_Graduate_Survey_with_Salary.csv
- **Records:** 3,000 graduates
- **Variables:** 15 original columns (see `data/data_dictionary.md`)
- **Availability:** In the group's possession before the proposal presentation

## Project Workflow

| Phase | Description | Output |
|-------|-------------|--------|
| 1 | Data cleaning and transformation in Power Query | All_Graduates and Employed_only datasets |
| 2 | Exploratory analysis | 8 baseline pivot tables |
| 3 | Research question analysis | RQ1 to RQ4 sheets with charts |
| 4 | Dashboard | KPI row, four charts, slicers |
| 5 | Findings and interpretation | Written findings and limitations |
| 6 | Final presentation | Presentation deck |

## Workbook Structure

| Sheet | Purpose |
|-------|---------|
| All_Graduates | Full cleaned dataset (3,000 rows) |
| Employed_only | Employed graduates only (2,107 rows), used for salary analysis |
| Exploration | Baseline pivot tables |
| RQ1 | University type vs earnings |
| RQ2 | Underemployment by field of study |
| RQ3 | Postgraduate degree salary ceiling |
| RQ4 | GPA vs starting salary |
| Dashboard | Summary KPIs, charts and slicers |
