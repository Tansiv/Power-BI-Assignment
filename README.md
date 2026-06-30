<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0f4c75,50:1b6ca8,100:00d4ff&height=200&section=header&text=Power%20BI%20Portfolio&fontSize=42&fontColor=ffffff&fontAlignY=38&desc=Business%20Intelligence%20Dashboards%20%7C%20Sales%20%26%20HR%20Analytics&descAlignY=58&descSize=18&animation=fadeIn"/>

<p>
  <img src="https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Power BI"/>
  <img src="https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white" alt="DAX"/>
  <img src="https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white" alt="Excel"/>
  <img src="https://img.shields.io/badge/Status-2%20Projects%20Completed-00C853?style=for-the-badge" alt="Status"/>
</p>

<p>
  <img src="https://img.shields.io/badge/Challenge%201-Sales%20Analytics-FF6B35?style=flat-square"/>
  <img src="https://img.shields.io/badge/Challenge%202-HR%20Analytics-9C27B0?style=flat-square"/>
  <img src="https://img.shields.io/badge/Pages-2%20Report%20Pages-blueviolet?style=flat-square"/>
  <img src="https://img.shields.io/badge/Total%20Visuals-17%2B-teal?style=flat-square"/>
</p>

<br/>

> ### 📊 *A two-project Power BI portfolio demonstrating end-to-end business intelligence skills*
> *From beverage sales performance tracking to full HR workforce analytics*

<br/>

</div>

---

## 📌 Table of Contents

<div align="center">

| # | Section |
|:---:|:---|
| 1 | [📖 Portfolio Overview](#-portfolio-overview) |
| 2 | [🥤 Challenge 1 — Beverage Sales Dashboard](#-challenge-1--beverage-sales-dashboard) |
| 3 | [👥 Challenge 2 — HR Analytics Dashboard](#-challenge-2--hr-analytics-dashboard) |
| 4 | [🚀 How to Run Both Dashboards](#-how-to-run-both-dashboards) |
| 5 | [📁 Project Structure](#-project-structure) |
| 6 | [🛠️ Tools & Technologies](#️-tools--technologies) |
| 7 | [💡 Key Skills Demonstrated](#-key-skills-demonstrated) |
| 8 | [👤 Author](#-author) |

</div>

---

## 📖 Portfolio Overview

This repository contains **two complete Power BI dashboards** built inside a single `.pbix` file, each on its own report page. Together they demonstrate a full range of BI skills: data modeling, DAX measure design, time intelligence, and interactive visualization across two very different business domains — retail sales and human resources.

<table>
<tr>
<td width="50%" valign="top">

### 🥤 Page 1 — Beverage Sales
Tracks revenue, profit, and brand performance across divisions and districts for a beverage distribution business.

**10 Tasks** | **5 DAX Measures** | **7 Visuals**

</td>
<td width="50%" valign="top">

### 👥 Page 2 — HR Analytics
Tracks headcount, attrition, satisfaction, and salary patterns across an entire employee lifecycle.

**15 Tasks** | **11 DAX Measures** | **13 Visuals**

</td>
</tr>
</table>

---

## 🥤 Challenge 1 — Beverage Sales Dashboard

### Overview

An interactive sales performance dashboard analyzing beverage brand revenue, profit margins, and regional performance, built from three relational tables: `Data`, `Dates`, and `Cost`.

### Data Model

```
Dates (1) ──── (*) Data (*) ──── (1) Cost
```

### Key Measures

```dax
Total Revenue = SUMX('Data', 'Data'[Units Sold] * 'Data'[Price per Unit])
Total Profit  = [Total Revenue] - [Total Cost]
```

### Dashboard Features

<div align="center">

| Visual | Purpose |
|:---|:---|
| 🎚️ Slicers | Filter by Division, District, Beverage Brand |
| 🃏 KPI Cards | Total Revenue, Units Sold, Average Price per Unit |
| 📈 Line Charts | Month-wise and Day-wise sales trends |
| 🍩 Donut Chart | Revenue share by Beverage Brand |
| 📊 Clustered Bar | Profit vs Revenue comparison by brand |

</div>

### Screenshots

![Dashboard Overview](screenshots/challenge-1-beverage-sales/dashboard_overview.png)
![KPI Cards](screenshots/challenge-1-beverage-sales/kpi_cards.png)
![Line Charts](screenshots/challenge-1-beverage-sales/line_charts.png)
![Donut Chart](screenshots/challenge-1-beverage-sales/donut_chart.png)
![Bar Chart](screenshots/challenge-1-beverage-sales/bar_chart.png)
![Data Model](screenshots/challenge-1-beverage-sales/data_model.png)

---

## 👥 Challenge 2 — HR Analytics Dashboard

### Overview

A complete workforce analytics dashboard covering headcount, attrition, employee satisfaction, hiring trends, and salary distribution, built from a single comprehensive HR dataset spanning 37 columns and over 1,400 employee records since company inception.

### Key Measures

```dax
Total Current Employees =
CALCULATE(DISTINCTCOUNT('HR_Data'[ID_employe]), 'HR_Data'[Attrition] = "No")

Termination Rate =
DIVIDE([Total Terminated Employees], [Total Employees Since Inception], 0)

Total Salary Paid =
CALCULATE(SUM('HR_Data'[Salary]), 'HR_Data'[Attrition] = "No")
```

### Dashboard Features

<div align="center">

| Visual | Purpose |
|:---|:---|
| 🎚️ Slicers | Filter by Department, Gender, Employment Type, Hire Type |
| 🃏 KPI Cards | Total Employees, Current, Terminated, Termination Rate, Total Salary |
| 🍩 Donut Chart | Current employees by Gender |
| 📊 Bar Charts | Education Levels, Job Satisfaction, Work Life Balance distribution |
| 📊 Column Charts | Quarterly New Hires vs Quarterly Terminations |
| 📈 Line Charts | Monthly Termination Trends and Monthly Salary Trends |
| 🔵 Scatter Charts | Salary spread by Years at Company (Full-time vs Contractor) and by Total Working Years (Gender) |

</div>

### Screenshots

![Dashboard Overview](screenshots/challenge-2-hr-analytics/dashboard_overview.png)
![KPI Cards](screenshots/challenge-2-hr-analytics/kpi_cards.png)
![Education & Satisfaction](screenshots/challenge-2-hr-analytics/education_satisfaction_charts.png)
![Quarterly Hires vs Terminations](screenshots/challenge-2-hr-analytics/quarterly_hires_terminations.png)
![Monthly Trends](screenshots/challenge-2-hr-analytics/monthly_trends.png)
![Scatter Charts](screenshots/challenge-2-hr-analytics/scatter_charts.png)

---

## 🚀 How to Run Both Dashboards

### Prerequisites

- ✅ **Microsoft Power BI Desktop** (free) → [Download here](https://powerbi.microsoft.com/desktop/)
- ✅ Windows 10 or later

### Setup Steps

**Step 1 — Clone or Download**
```bash
git clone https://github.com/Tansiv/Power-BI-Assignment.git
```

**Step 2 — Open the File**
```
1. Navigate to the downloaded folder
2. Double-click Beverage_Sales_Dashboard.pbix
3. Power BI Desktop will open with two pages at the bottom:
      Page 1 → Beverage Sales Dashboard
      Page 2 → HR Analytics Dashboard
```

**Step 3 — If Data Refresh Fails**
```
1. Home → Transform Data → Data Source Settings
2. Update the file paths to point to the /data folder on your machine
3. Click Close & Apply
```

**Step 4 — Explore**
```
✅ Click between Page 1 and Page 2 using the tabs at the bottom
✅ Use slicers on each page to filter the data
✅ Click any chart to cross-filter related visuals
```

---

## 📁 Project Structure

```
📦 Power-BI-Assignment/
│
├── 📊 Beverage_Sales_Dashboard.pbix
│
├── 📂 data/
│   ├── 📗 Beverage_Sales_Data.xlsx
│   └── 📗 HR_Employee_Data.xlsx
│
├── 📂 screenshots/
│   ├── 📂 challenge-1-beverage-sales/
│   │   ├── dashboard_overview.png
│   │   ├── kpi_cards.png
│   │   ├── line_charts.png
│   │   ├── donut_chart.png
│   │   ├── bar_chart.png
│   │   └── data_model.png
│   │
│   └── 📂 challenge-2-hr-analytics/
│       ├── dashboard_overview.png
│       ├── kpi_cards.png
│       ├── education_satisfaction_charts.png
│       ├── quarterly_hires_terminations.png
│       ├── monthly_trends.png
│       └── scatter_charts.png
│
└── 📄 README.md
```

---

## 🛠️ Tools & Technologies

<div align="center">

| Tool | Purpose |
|:---|:---|
| <img src="https://img.shields.io/badge/Power%20BI%20Desktop-F2C811?style=flat&logo=powerbi&logoColor=black"/> | Dashboard building & visualization |
| <img src="https://img.shields.io/badge/DAX-0078D4?style=flat&logo=microsoft&logoColor=white"/> | Data modeling & calculated measures |
| <img src="https://img.shields.io/badge/Power%20Query-217346?style=flat&logo=microsoft&logoColor=white"/> | Data transformation & cleaning |
| <img src="https://img.shields.io/badge/Microsoft%20Excel-217346?style=flat&logo=microsoftexcel&logoColor=white"/> | Source data files |
| <img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white"/> | Version control & portfolio hosting |

</div>

---

## 💡 Key Skills Demonstrated

- **Data Modeling** — building star-schema relationships between fact and dimension tables (Challenge 1) and working with single wide tables (Challenge 2)
- **DAX Measure Design** — `SUMX`, `CALCULATE`, `DISTINCTCOUNT`, `DIVIDE`, and time-intelligence patterns across 16 total measures
- **Time Intelligence** — Month-wise, Quarter-wise, and Day-wise trend analysis using Date Hierarchies
- **Advanced Visuals** — scatter charts with proper Values/Details configuration for individual record-level analysis
- **Power Query (ETL)** — data type correction, custom columns, and data cleaning
- **Dashboard UX** — slicers, cross-filtering, KPI card design, and consistent color theory across both projects
- **Business Storytelling** — translating raw HR and sales data into metrics decision-makers actually use (termination rate, profit margin, brand share)

---

## 👤 Author

<div align="center">

<br/>

**Your Name Here**

[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Tansiv)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR-PROFILE)

*Power BI | Data Analytics | Business Intelligence*

<br/>

---

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:00d4ff,50:1b6ca8,100:0f4c75&height=120&section=footer&animation=fadeIn"/>

*⭐ If you found this portfolio helpful, please consider giving it a star!*

</div>