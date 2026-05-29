# 👥 HR Analytics Dashboard

[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Domain](https://img.shields.io/badge/Domain-Human_Resources-blueviolet?style=flat-square)]()
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)]()

> A Power BI dashboard that transforms HR workforce data into actionable people analytics — tracking employee attrition, department-wise headcount, satisfaction scores, and demographic breakdowns to support data-driven HR decision-making.

---

## 📌 Problem Statement

HR departments generate significant volumes of employee data — attrition records, performance ratings, satisfaction surveys, department rosters — yet most organizations lack a consolidated view to answer critical workforce questions: *Why are employees leaving? Which departments have the highest attrition risk? How do satisfaction scores correlate with turnover?*

Without clear visibility into these patterns, HR interventions are reactive rather than preventive, and retention strategies are applied broadly rather than targeted at high-risk cohorts.

---

## 💡 Solution Overview

The HR Analytics Dashboard provides a single-screen view of workforce health metrics. It enables HR managers and business leaders to:

- Monitor overall attrition rate and headcount in real time
- Identify which departments, age groups, or salary bands are experiencing the highest turnover
- Understand the relationship between job satisfaction, work-life balance, and attrition
- Segment the workforce by education, gender, and experience for equity analysis

---

## ✨ Features

- **Attrition KPI Banner** — Total employees, attrition count, attrition rate %, active employee count
- **Department-wise Attrition** — Breakdown of attrition across HR, Sales, R&D, and other departments
- **Age Group Distribution** — Employee count and attrition rate segmented by age band
- **Job Satisfaction Matrix** — Satisfaction rating (1–4) cross-tabulated by job role
- **Education Field Analysis** — Attrition breakdown by educational background
- **Gender & Age Demographic View** — Workforce composition by gender across age groups
- **Salary Band Attrition** — Identifies which compensation tiers face the highest turnover risk
- **Interactive Slicers** — Filter by Department, Gender, Education, and Job Role

---

## 🏗️ Dashboard Architecture

```
HR Dataset (Excel/CSV)
        │
        ▼
Power BI Data Model
├── Data Cleaning (Power Query):
│   ├── Standardized column names
│   ├── Attrition column: "Yes"/"No" → binary (1/0)
│   ├── Age groups: calculated column (binned ranges)
│   └── Salary bands: bucketed from continuous salary field
├── DAX Measures:
│   ├── Attrition Rate (%) = DIVIDE([Attrition Count], [Total Employees])
│   ├── Active Employees = [Total Employees] - [Attrition Count]
│   ├── Avg Age = AVERAGE(HR_Data[Age])
│   └── Avg Satisfaction = AVERAGE(HR_Data[JobSatisfaction])
└── Relationships: Single flat table (denormalized HR dataset)
        │
        ▼
Dashboard Pages
├── Page 1: Executive Summary (KPIs + high-level charts)
├── Page 2: Attrition Deep Dive (by dept, age, salary, education)
└── Page 3: Satisfaction & Demographics
        │
        ▼
Published .pbix file
```

---

## 🧰 Tech Stack

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Dashboard design, DAX measures, interactivity |
| **Power Query (M)** | Data transformation and cleaning |
| **DAX** | Calculated columns and measures (Attrition Rate, Active Employees) |
| **HR Analytics Dataset** | IBM HR Analytics Employee Attrition dataset (publicly available) |

---

## 🚀 Getting Started

### Prerequisites

- [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) (free download)

### Setup

```bash
git clone https://github.com/Shubh1015/HR-Analytics.git
cd HR-Analytics
```

Open `HR Analytics Dashboard.pbix` in Power BI Desktop.

> **Data Source:** IBM HR Analytics Employee Attrition & Performance dataset, available on [Kaggle](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)

---

## 📸 Dashboard Preview

![HR Analytics Dashboard](HR%20ANALYTICS.png)

---

## 📊 Key Analytical Findings

- The overall attrition rate is approximately **16%** — above the typical industry benchmark of 10–12%, signaling retention risk
- **Sales Representatives** and **Laboratory Technicians** exhibit the highest attrition rates by job role
- Employees in the **26–35 age group** account for the largest share of attrition — a critical talent segment to retain
- Workers earning **below-average salaries** (up to $5K/month) show significantly higher attrition, suggesting compensation is a primary exit driver
- Employees with **Life Sciences** and **Medical** educational backgrounds form the majority of the workforce but also the majority of departures

---

## 🔮 Future Enhancements

- [ ] Add tenure analysis — attrition rate by years at company
- [ ] Build a predictive attrition risk score using Python + Power BI integration
- [ ] Include performance rating as a dimension in attrition analysis
- [ ] Add month-wise attrition trend for time-series visibility

---

## 🤝 Contributing

Contributions and new analytical perspectives are welcome. Open an issue before submitting a PR.

---

## 📄 License

MIT License. Dataset sourced from IBM HR Analytics public dataset via Kaggle, used for educational purposes.

---

## 🏷️ Topics

`power-bi` `hr-analytics` `people-analytics` `attrition-analysis` `data-visualization` `human-resources` `business-intelligence` `dax` `workforce-analytics`
