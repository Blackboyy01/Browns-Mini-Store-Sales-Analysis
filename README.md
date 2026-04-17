# 🛒 Browns Mini Store Sales Analytics 
> End-to-end data pipeline, multi-dimensional analysis, and interactive dashboard built entirely in Microsoft Excel.

![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Power Query](https://img.shields.io/badge/Power_Query-ETL_Pipeline-217346?style=for-the-badge)
![Pivot tables](https://img.shields.io/badge/Pivot-table-217346?style=for-the-badge)
![ Dashboard](https://img.shields.io/badge/Dashboard-visualization-CF222E?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)


## Project Description:

The task is to clean, transform, and analyze the transactional sales records to evaluate revenue performance across time, outlet formats, product categories, and Stock Keeping Unit(SKU)level contributions, then present findings in an interactive dashboard.
## Objectives:

1. **Data Cleaning**: Identify and remove any records with missing or null values.
2. **Exploratory Data Analysis (EDA)**: Perform basic exploratory data analysis to understand the dataset.
3. **Business Analysis**: Use Excel to answer specific business questions and derive insights from the sales data: Core revenue drivers,
Underperforming segments,
Product concentration risks,
Overall business performance trends
4. **Dashboard Requirements**:
   Using Pivot Tables and Charts, build an interactive dashboard that answers the following:
- Top 5 Item Types by total sales
- Bottom 5 Item Identifiers by total sales
- Yearly Sales Trend
- Average Sales by each Outlet Type
- Total Sales Count
- Identify the year with the highest and lowest total sales
  
**Add slicers for**:
-	Item Type
-	Outlet Type
-	Outlet Size

## Project Structure


---

## 📌 Project Overview

This project demonstrates a full analytics workflow: from raw data ingestion to an executive-ready, interactive Excel dashboard. It covers ETL via Power Query, flat data modeling, KPI development using advanced formulas, and multi-dimensional analysis using Pivot Tables and Slicers.

---

## 🗂️ Table of Contents
- [Executive Summary](#Executive-Summary)
- [Tech Stack](#tech-stack)
- [1. Data Ingestion & Transformation](#1-data-ingestion--transformation-power-query)
- [2. Data Modeling](#2-data-modeling)
- [3. Feature Engineering & KPI Development](#3-feature-engineering--kpi-development)
- [4. Exploratory & Diagnostic Analysis](#4-exploratory--diagnostic-analysis-pivot-tables)
- [5. Dashboard Development](#5-dashboard-development-excel)
- [6. Key Insights](#6-key-insights)
- [7. Business Impact](#7-business-impact)
- [8. Deliverables](#8-deliverables)
- [9. Challenges & Resolution](#9-challenges--resolution)

---
## Executive Summary
The Mini Store recorded 8,523 sales transactions across multiple outlet formats and product categories. A structured analysis of the dataset reveals clear patterns in revenue distribution across time, channels, and product lines, highlighting both scalable strengths and underperforming segments requiring strategic adjustment
 
From a time-series perspective, the business reached its peak revenue of $3.63M in 1985, followed by a prolonged decline to a low of $190K in 1998, representing an approximate 94.8% drop from peak performance. However, the recovery to $1.85M by 2009 reflects a ~873% increase from the lowest point, indicating strong recovery capacity and underlying business resilience. This suggests that while the business is sensitive to external or operational shocks, it retains the ability to rebound when conditions are favorable.
 
Outlet-level performance shows a clear structural advantage in the supermarket formats. Supermarket Type 3 leads with $3.69M, outperforming Supermarket Type 1 ($2.32M) by approximately 59% and Supermarket Type 2 ($1.99M) by ~85%. Collectively, supermarket formats contribute the overwhelming majority of total revenue. In contrast, the Grocery Store channel contributes only $339.83, less than 10% of the top-performing outlet, suggesting significantly lower customer traffic, a limited product assortment, or weaker conversion efficiency.
 
At the category level, Fruits & Vegetables and Snack Foods each generate approximately $3M, placing them at the top of the revenue hierarchy and likely accounting for a substantial proportion of total sales. Compared to lower-performing categories such as Seafood ($149K), these top categories generate over 20x higher revenue, reinforcing their role as core demand drivers. This suggests a strong concentration of consumer preferences, while underperforming categories may reflect weak demand alignment and pricing inefficiencies.

At the Stock Keeping Unit (SKU) level, FDQ04 ($784.31) and FDF38 ($771.66) lead performance, with FDY43 ($673.79) trailing by approximately 14–16%, indicating near-top-tier potential. However, the drop to NCR42 ($332.90) represents a ~50% decline, highlighting a sharp performance gap beyond the top three SKUs. This concentration introduces dependency risk, as revenue is heavily reliant on a narrow set of products.

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **Power Query** | ETL / Data Transformation |
| **Pivot Tables** | Multi-dimensional Analysis |
| **Pivot Charts & Slicers** | Interactive Dashboarding |
| **Advanced Formulas** | KPI & Metric Calculations |

---

## 1. Data Ingestion & Transformation (Power Query)

Imported the raw dataset into Excel Power Query to establish a structured, refreshable ETL pipeline.

**Transformation steps applied:**

- ✅ Standardized data types — dates, currency, and categorical fields
- ✅ Cleaned missing values using logical replacement methods
- ✅ Removed duplicate records to ensure data integrity
- ✅ Filtered outliers to prevent skewed aggregations
- ✅ Normalized currency values for consistent cross-segment reporting
- ✅ Built a refreshable pipeline for full reproducibility

---

## 2. Data Modeling

Structured the dataset into a **flat analytical model** optimized for Excel.

| Component | Fields |
|---|---|
| **Dimensions** | Year, Outlet Type, Category, SKU |
| **Measures** | Revenue, Transaction Count |

Clean, consistent data was enforced at this layer to ensure reliability in all downstream analysis.

---

## 3. Feature Engineering & KPI Development

Calculated key business metrics using Excel formulas and Pivot-based logic:

| KPI | Method |
|---|---|
| Total Revenue | `SUM` aggregation |
| Revenue by Outlet / Category / SKU | Pivot-based breakdown |
| % Contribution by Segment | `% of Total` calculation |
| Year-over-Year Growth / Decline | Variance analysis |

> Logic mirrors DAX-style calculations (SUM, % of total, period-over-period variance) implemented entirely within Excel.

---

## 4. Exploratory & Diagnostic Analysis (Pivot Tables)

Multi-dimensional analysis performed across four lenses:

### 📅 Time-Series Analysis

| Metric | Value |
|---|---|
| Peak Revenue | **$3.63M** (1985) |
| Lowest Revenue | **$190K** (1998) |
| Peak-to-Trough Decline | ~94.8% |
| Trough-to-Recovery Growth | ~873% |

> High volatility with strong resilience — the business recovered nearly 9× from its lowest point.

---

### 🏪 Channel Performance

| Outlet Type | Revenue | vs. Type 3 |
|---|---|---|
| Supermarket Type 3 | **$3.69M** | — (Top Performer) |
| Supermarket Type 1 | ~$2.33M | ~59% below Type 3 |
| Supermarket Type 2 | ~$1.44M | ~85% below Type 3 |
| Grocery Stores | Low | Underperforming channel |

---

### 📦 Category Performance

| Category | Revenue |
|---|---|
| Fruits & Vegetables | ~$3M |
| Snack Foods | ~$3M |
| Other Categories | Mid-range |
| Seafood | $149K (>20× below top categories) |

> Strong demand concentration in two categories — all others trail significantly.

---

### 🔖 SKU-Level Analysis

| SKU | Revenue |
|---|---|
| FDQ04 | $784.31 (Top SKU) |
| FDF38 | $771.66 |
| NCR42 | $332.90 (Sharp drop-off) |

> High dependency on a small set of top-performing SKUs introduces product concentration risk.

---

## 5. Dashboard Development (Excel)

Built an **interactive Excel dashboard** powered by Pivot Tables.

**Dashboard components:**

- 📊 KPI Summary — Total Revenue, Top Categories, Top Outlets
- 📈 Trend Analysis Charts — Time-series revenue visualization
- 📉 Category & Outlet Comparison Visuals

**Dynamic filtering via Slicers:**

| Slicer | Filter Scope |
|---|---|
| Outlet Type | Filter by channel |
| Category | Filter by product group |
| Time | Filter by year / period |

---

## 6. Key Insights

| # | Insight |
|---|---|
| 1 | Supermarket Type 3 is the **primary revenue driver** |
| 2 | Revenue is **heavily concentrated** in Fruits & Vegetables and Snack Foods |
| 3 | Business shows **strong recovery resilience** despite historical volatility |
| 4 | Sales depend on a **few top SKUs** — introducing portfolio concentration risk |

---

## 7. Business Impact

**Growth opportunities identified:**
- Supermarket Type 3 and top categories are clear targets for channel and category investment

**Underperforming segments flagged:**
- Grocery Stores and Seafood require strategic review — resource reallocation or exit

**Risk highlighted:**
- SKU concentration risk signals the need for product portfolio diversification

**Actionable direction provided for:**
- Channel investment prioritization
- Category optimization
- Product portfolio balancing

---

## 8. Deliverables

| Deliverable | Description |
|---|---|
| 📂 Excel Dashboard | Interactive, slicer-driven, auto-refreshable via Power Query |
| 📑 Presentation Deck | Structured, insight-driven storytelling for stakeholders |

---

## 9. Challenges & Resolution

**Challenge 1 — Multi-dimensional aggregation**
> Selecting the right formulas to replicate DAX-style logic (% of total, YoY variance) without a full data model.

**Resolution:** Leveraged Pivot Tables with iterative validation: cross-checking outputs against manual totals before finalizing all KPIs.

---

**Challenge 2 — Dashboard design clarity**
> Translating complex pivot analysis into a single, navigable dashboard for non-technical stakeholders.

**Resolution:** Applied structured layout principles — KPI prioritization at the top, progressive disclosure via Slicers, and chart types, colors chosen for clarity over complexity.

---

## 📁 Repository Structure

```
📦 retail-sales-analytics/
 ┣ 📊 Retail_Sales_Dashboard.xlsx   ← Main Excel file (Power Query + Pivots + Dashboard)
 ┣ 📂 data/
 ┃ ┗ 📄 raw_dataset.csv             ← Source data
 ┣ 📂 presentation/
 ┃ ┗ 📄 Retail_Sales_Insights.pptx  ← Stakeholder presentation
 ┗ 📄 README.md
```

---

*Built with Microsoft Excel · Power Query · Pivot Tables · Advanced Formulas*
