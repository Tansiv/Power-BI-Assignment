<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Poppins&size=36&duration=3000&pause=1000&color=00B4D8&center=true&vCenter=true&width=600&height=70&lines=Power+BI+Portfolio;Sales+%2B+HR+Analytics" alt="Power BI Portfolio"/>

<sub>Two end-to-end business intelligence dashboards · data modeling · DAX · time intelligence</sub>

<br/><br/>

[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](#)
[![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)](#)
[![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)](#)
[![Status](https://img.shields.io/badge/Status-Complete-success?style=for-the-badge)](#)

![Repo Size](https://img.shields.io/github/repo-size/Tansiv/Power-BI-Assignment?style=flat-square&color=blue)
![Last Commit](https://img.shields.io/github/last-commit/Tansiv/Power-BI-Assignment?style=flat-square&color=orange)
![Stars](https://img.shields.io/github/stars/Tansiv/Power-BI-Assignment?style=flat-square&color=yellow)

</div>

Two production-grade Power BI dashboards built from raw data to decision-ready insight: a **retail sales analytics** model and a **full HR workforce analytics** model. Each demonstrates relational data modeling, custom DAX, time intelligence, and dashboard UX best practices.

---

## Quick Look

| | Beverage Sales | HR Analytics |
|---|:---:|:---:|
| **Domain** | Retail / FMCG | Human Resources |
| **Source Tables** | 3 (star schema) | 1 (wide table, 1.4K+ rows) |
| **DAX Measures** | 5 | 11 |
| **Visuals** | 7 | 13 |
| **File** | `powerbi-challenge-1/Beverage_Sales_Dashboard.pbix` | `powerbi-challenge-2/HR_Analytics_Dashboard.pbix` |

---

## 🥤 Beverage Sales Dashboard

Revenue, profit, and brand performance across divisions and districts.

**Model**
```
Dates (1) ──< Data >── (1) Cost
```

**Core DAX**
```dax
Total Revenue = SUMX('Data', 'Data'[Units Sold] * 'Data'[Price per Unit])
Total Profit  = [Total Revenue] - [Total Cost]
```

**Visuals:** Division/District/Brand slicers · KPI cards (Revenue, Units, Avg Price) · Month & day sales trends · Brand revenue donut · Profit vs Revenue clustered bar

<table>
<tr>
<td><img src="screenshots/challenge-1-beverage-sales/dashboard_overview.png" width="100%"/></td>
<td><img src="screenshots/challenge-1-beverage-sales/kpi_cards.png" width="100%"/></td>
</tr>
<tr>
<td><img src="screenshots/challenge-1-beverage-sales/line_charts.png" width="100%"/></td>
<td><img src="screenshots/challenge-1-beverage-sales/donut_chart.png" width="100%"/></td>
</tr>
<tr>
<td><img src="screenshots/challenge-1-beverage-sales/bar_chart.png" width="100%"/></td>
<td><img src="screenshots/challenge-1-beverage-sales/data_model.png" width="100%"/></td>
</tr>
</table>

---

## 👥 HR Analytics Dashboard

Headcount, attrition, satisfaction, and salary distribution across the employee lifecycle.

**Core DAX**
```dax
Total Current Employees = CALCULATE(DISTINCTCOUNT('HR_Data'[ID_employe]), 'HR_Data'[Attrition]="No")
Termination Rate        = DIVIDE([Total Terminated Employees], [Total Employees Since Inception], 0)
Total Salary Paid       = CALCULATE(SUM('HR_Data'[Salary]), 'HR_Data'[Attrition]="No")
```

**Visuals:** Department/Gender/EmploymentType/HireType slicers · 5 KPI cards · Gender donut · Education/Satisfaction/WLB bars · Quarterly hires vs terminations · Monthly trend lines · Salary scatter plots (tenure × employment type, experience × gender)

<table>
<tr>
<td><img src="screenshots/challenge-2-hr-analytics/dashboard_overview.png" width="100%"/></td>
<td><img src="screenshots/challenge-2-hr-analytics/kpi_cards.png" width="100%"/></td>
</tr>
<tr>
<td><img src="screenshots/challenge-2-hr-analytics/education_satisfaction_charts.png" width="100%"/></td>
<td><img src="screenshots/challenge-2-hr-analytics/quarterly_hires_terminations.png" width="100%"/></td>
</tr>
<tr>
<td><img src="screenshots/challenge-2-hr-analytics/monthly_trends.png" width="100%"/></td>
<td><img src="screenshots/challenge-2-hr-analytics/scatter_charts.png" width="100%"/></td>
</tr>
</table>

---

## Run It Locally

```bash
git clone https://github.com/Tansiv/Power-BI-Assignment.git
```

Open `powerbi-challenge-1/Beverage_Sales_Dashboard.pbix` or `powerbi-challenge-2/HR_Analytics_Dashboard.pbix` in **Power BI Desktop**. If data fails to refresh: `Home → Transform Data → Data Source Settings` → repoint to `/data`.

**Requires:** [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free), Windows 10+

---

## Structure

```
Power-BI-Assignment/
├── powerbi-challenge-1/Beverage_Sales_Dashboard.pbix
├── powerbi-challenge-2/HR_Analytics_Dashboard.pbix
├── data/
│   ├── Beverage_Sales_Data.xlsx
│   └── HR_Employee_Data.xlsx
├── screenshots/
│   ├── challenge-1-beverage-sales/
│   └── challenge-2-hr-analytics/
└── README.md
```

---

## Skills Demonstrated

`Star-schema modeling` `DAX (SUMX, CALCULATE, DIVIDE, DISTINCTCOUNT)` `Time intelligence` `Power Query ETL` `Scatter/cluster visual design` `Slicer-driven UX` `KPI storytelling`

---

<div align="center">

**Tansiv Jubayer** · [GitHub](https://github.com/Tansiv) · [LinkedIn](https://www.linkedin.com/in/tansiv-jubayer/)

───────────────────────────

⭐ **If this helped you, star the repo.**

</div>