# Excel Salary Dashboard

![Dashboard Screenshot](Screenshot 2026-03-15 010908.png)

## Project Overview

The **Excel Salary Dashboard** is a data analysis project built using **Microsoft Excel** to visualize salary trends for different data-related jobs.

This project was recreated independently for learning purposes by studying concepts from an online tutorial. The goal of the project was to practice **Excel data analysis, dashboard design, and data visualization techniques**.

The dashboard helps users explore salary insights based on **job roles, countries, and job schedule types**.

---

## Dashboard File

The Excel dashboard file included in this repository:

`1_Salary_Dashboard.xlsx`

---

## Tools and Skills Used

This project demonstrates the use of the following Excel features:

- Charts (Bar Chart, Map Chart)
- Excel Formulas and Functions
- Data Validation
- Data Filtering
- Structured Tables
- Dashboard Design

---

## Dataset Overview

The dataset used in this project contains **data science job information from 2023**.

It includes the following information:

- Job Titles
- Average Salaries
- Job Locations
- Job Schedule Types
- Required Skills

The dataset is used only for **learning and analysis purposes**.

---

# Dashboard Features

## 1. Salary Comparison by Job Role

The dashboard includes a **bar chart** that compares median salaries across different data-related job roles.

### Implementation

- Excel **Bar Chart** used for visualization
- Job roles sorted by **highest to lowest salary**
- Salary values formatted for readability

### Insight

Higher-level roles such as **Data Engineers and Senior Data Scientists** typically offer higher salaries compared to analyst roles.

---

## 2. Global Salary Distribution

The dashboard includes a **map chart** that displays median salary distribution across countries.

### Implementation

- Excel **Map Chart**
- Countries color-coded based on salary values

### Insight

The visualization highlights **salary differences across different regions globally**.

---

# Excel Formulas Used

## Median Salary Calculation

```excel
=MEDIAN(
IF(
(jobs[job_title_short]=A2)*
(jobs[job_country]=country)*
(ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
(jobs[salary_year_avg]<>0),
jobs[salary_year_avg]
)
)
