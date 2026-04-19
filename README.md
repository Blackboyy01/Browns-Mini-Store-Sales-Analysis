# Browns Mini Store Sales Analytics

> End-to-end data pipeline, multi-dimensional analysis, and interactive dashboard built entirely in Microsoft Excel.

![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Power Query](https://img.shields.io/badge/Power_Query-ETL_Pipeline-217346?style=for-the-badge)
![Pivot tables](https://img.shields.io/badge/Pivot-table-217346?style=for-the-badge)
![ Dashboard](https://img.shields.io/badge/Dashboard-visualization-CF222E?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

## Table of Contents

- [Executive Summary](#executive-summary)
- [Project Description](#project-description)
- [Project Structure](#project-structure)
- [Tech Stack](#tech-stack)
- [Process Flow](#process-flow)
- [1. Data Ingestion & Transformation](#1-data-ingestion--transformation-power-query)
- [2. Data Modeling](#2-data-modeling)
- [3. Feature Engineering & KPI Development](#3-feature-engineering--kpi-development)
- [4. Exploratory & Diagnostic Analysis](#4-exploratory--diagnostic-analysis-pivot-tables)
- [5. Dashboard Development](#5-dashboard-development-excel)
- [6. Key Insights](#6-key-insights)
- [7. Business Impact](#7-business-impact)
- [8. Recommendations](#8-recommendations)
- [9. Deliverables](#9-deliverables)
- [10. Challenges & Resolution](#10-challenges--resolution)

## Executive Summary

Browns Mini Store has processed **8,523 sales transactions** across multiple outlet formats and product categories. The business has demonstrated a clear capacity for recovery: despite a **~94.8% revenue decline** from its peak of **$3.63M in 1985** to a low of **$190K in 1998**, it rebounded to **$1.85M by 2009**, a **~873% increase** from its lowest point. That trajectory is not a coincidence; it reflects a business with real demand behind it. The question is no longer whether this business can grow, but where to focus to grow it faster and more efficiently.

Outlet-level performance shows a clear structural advantage in the supermarket formats. Supermarket Type 3 leads with **$3.69M**, outperforming Supermarket Type 1 (**$2.32M**) by approximately **59%** and Supermarket Type 2 (**$1.99M**) by **~85%**. Collectively, supermarket formats contribute the overwhelming majority of total revenue. In contrast, the Grocery Store channel contributes only **$339.83**, less than **10%** of the top-performing outlet, suggesting significantly lower customer traffic, a limited product assortment, or weaker conversion efficiency.

At the category level, Fruits & Vegetables and Snack Foods each generate approximately **$3M**, placing them at the top of the revenue hierarchy and likely accounting for a substantial proportion of total sales. Compared to lower-performing categories such as Seafood (**$149K**), these top categories generate over **20x** higher revenue, reinforcing their role as core demand drivers. This suggests a strong concentration of consumer preferences, while underperforming categories may reflect weak demand alignment and pricing inefficiencies.

At the Stock Keeping Unit (SKU) level, FDQ04 (**$784.31**) and FDF38 (**$771.66**) lead performance, with FDY43 (**$673.79**) trailing by approximately **14 to 16%**, indicating near-top-tier potential. However, the drop to NCR42 (**$332.90**) represents a **~50% decline**, highlighting a sharp performance gap beyond the top three SKUs. This concentration introduces dependency risk, as revenue is heavily reliant on a narrow set of products.

## Project Description

The task is to clean, transform, and analyze the transactional sales records to evaluate revenue performance across time, outlet formats, product categories, and Stock Keeping Unit (SKU) level contributions, then present findings in an interactive dashboard.

## Objectives

1. **Data Cleaning**: Identify and remove any records with missing or null values.
1. **Exploratory Data Analysis (EDA)**: Perform basic exploratory data analysis to understand the dataset.
1. **Business Analysis**: Use Excel to answer specific business questions and derive insights from the sales data: Core revenue drivers, Underperforming segments, Product concentration risks, Overall business performance trends.
1. **Dashboard Requirements**:
   Using Pivot Tables and Charts, build an interactive dashboard that answers the following:
   
   **Key Questions to be Answered by the dashboard**
- Top 5 Item Types by total sales
- Bottom 5 Item Identifiers by total sales
- Yearly Sales Trend
- Average Sales by each Outlet Type
- Total Sales Count
- Identify the year with the highest and lowest total sales
   
   **Add slicers for:**
- Item Type
- Outlet Type
- Outlet Size

## Project Structure

-----

## Project Overview

This project is a full analytics workflow: from raw data ingestion to an executive-ready, interactive Excel dashboard. It covers ETL via Power Query, flat data modeling, KPI development using advanced formulas, and multi-dimensional analysis using Pivot Tables and Slicers.

## Tech Stack

|Tool                      |Purpose                   |
|--------------------------|--------------------------|
|**Microsoft Excel**       |End-End Analysis          |
|**Power Query**           |ETL / Data Transformation |
|**Pivot Tables**          |Multi-dimensional Analysis|
|**Pivot Charts & Slicers**|Interactive Dashboarding  |
|**Advanced Formulas**     |KPI & Metric Calculations |

-----

## Process Flow

-----

## 1. Data Ingestion & Transformation (Power Query)

Imported the raw dataset into Excel, then Power Query to establish a structured, refreshable ETL pipeline.

**Transformation steps applied:**

- Standardized data types: dates, currency, and categorical fields
- Cleaned missing values using logical replacement methods
- Removed duplicate records to ensure data integrity
- Filtered outliers to prevent skewed aggregations
- Normalized currency values for consistent cross-segment reporting
- Built a refreshable pipeline

-----

## 2. Data Modeling

Structured the dataset into a **flat analytical model** optimized for Excel.

|Component     |Fields                          |
|--------------|--------------------------------|
|**Dimensions**|Year, Outlet Type, Category, SKU|
|**Measures**  |Revenue, Transaction Count      |

Clean, consistent data was enforced at this layer to ensure reliability in all downstream analysis.

-----

## 3. Feature Engineering & KPI Development

Calculated key business metrics using Excel formulas and Pivot-based logic:

|KPI                               |Method                  |
|----------------------------------|------------------------|
|Total Revenue                     |`SUM` aggregation       |
|Revenue by Outlet / Category / SKU|Pivot-based breakdown   |
|% Contribution by Segment         |`% of Total` calculation|
|Year-over-Year Growth / Decline   |Variance analysis       |


> Logic mirrors DAX-style calculations (SUM, % of total, period-over-period variance) implemented entirely within Excel.

-----

## 4. Exploratory & Diagnostic Analysis (Pivot Tables)

Multi-dimensional analysis performed across four lenses:

### Time-Series Analysis

|Metric                   |Value            |
|-------------------------|-----------------|
|Peak Revenue             |**$3.63M** (1985)|
|Lowest Revenue           |**$190K** (1998) |
|Peak-to-Trough Decline   |**~94.8%**       |
|Trough-to-Recovery Growth|**~873%**        |


> High volatility with strong resilience. The business recovered nearly **9x** from its lowest point.

-----

### Channel Performance

|Outlet Type       |Revenue    |vs. Type 3             |
|------------------|-----------|-----------------------|
|Supermarket Type 3|**$3.69M** |Top Performer          |
|Supermarket Type 1|**~$2.33M**|**~59%** below Type 3  |
|Supermarket Type 2|**~$1.44M**|**~85%** below Type 3  |
|Grocery Stores    |**$339.83**|Underperforming channel|

-----

### Category Performance

|Category           |Revenue                                      |
|-------------------|---------------------------------------------|
|Fruits & Vegetables|**~$3M**                                     |
|Snack Foods        |**~$3M**                                     |
|Other Categories   |Mid-range                                    |
|Seafood            |**$149K** (over **20x** below top categories)|


> Strong demand concentration in two categories. All others trail significantly.

-----

### Stock Keeping Units (SKU) Level Analysis

|SKU  |Revenue                     |
|-----|----------------------------|
|FDQ04|**$784.31** (Top SKU)       |
|FDF38|**$771.66**                 |
|NCR42|**$332.90** (Sharp drop-off)|


> High dependency on a small set of top-performing SKUs introduces product concentration risk.

-----

## 5. Dashboard Development (Excel)

Built an **interactive Excel dashboard** powered by Pivot Tables.

**Dashboard components:**

- KPI Summary: Total Revenue, Top Categories, Top Outlets
- Trend Analysis Charts: Time-series revenue visualization
- Category & Outlet Comparison Visuals

**Dynamic filtering via Slicers:**

|Slicer     |Filter Scope           |
|-----------|-----------------------|
|Outlet Type|Filter by channel      |
|Outlet Size|Filter by channel size |
|Item Type  |Filter by type of goods|

-----

## 6. Key Insights

|#|Insight                                                                                                                    |
|-|---------------------------------------------------------------------------------------------------------------------------|
|1|Supermarket Type 3 is the **primary revenue driver** at **$3.69M**                                                         |
|2|Revenue is **heavily concentrated** in Fruits & Vegetables and Snack Foods at approximately **$3M each**                   |
|3|Business shows **strong recovery resilience**, growing **~873%** from its lowest point                                     |
|4|Sales depend on a **few top SKUs**, with a **~50%** revenue drop to the next tier, introducing portfolio concentration risk|

-----

## 7. Business Impact

**Growth opportunities identified:**

- Supermarket Type 3 (**$3.69M**) is the highest-performing format, outperforming Type 1 by **~59%** and Type 2 by **~85%**, flagged for **60 to 70%** of expansion budget allocation
- Fruits & Vegetables and Snack Foods (**~$3M each**) identified as core revenue anchors, targeted for a **20 to 30%** shelf space increase and **10 to 15%** basket value uplift

**Underperforming segments flagged:**

- Grocery Store channel (**$339.83**) generates less than **10%** of top outlet revenue. A two-month performance test with a **25 to 40%** growth benchmark has been set before reallocation decision
- Seafood (**$149K**) generates **20x** less than top categories. Inventory reduction of **20 to 40%** recommended, with a **15%** recovery threshold before exit

**Risk highlighted:**

- Top SKUs (FDQ04, FDF38) show a **~50%** revenue drop to the next tier. Cross-merchandising and **5 to 10%** discount trials introduced to reduce concentration dependency and build second-tier SKU performance

**Actionable direction provided for:**

- Channel investment prioritization: budget and promotional resources redirected to Supermarket Type 3 within the next budget cycle
- Category optimization: KPIs established for revenue growth (**+10 to 15%**), inventory turnover, and basket size uplift
- Product portfolio balancing: second-tier SKU visibility and demand sensitivity actively being tested

-----

## 8. Recommendations

1. **Expand and Replicate the Supermarket Type 3 Model**
   
   Why it matters: Supermarket Type 3 generates **$3.69M**, outperforming Type 1 by **~59%** and Type 2 by **~85%**, making it the most efficient revenue-generating format and the strongest candidate for scalable growth.
   
   How:
- Prioritise Supermarket Type 3 in the next budget cycle (**60 to 70%** of expansion budget)
- Conduct a comparative analysis of pricing, product mix, and layout across outlet types within **30 days**, and redirect promotional resources to this outlet format as the primary growth vehicle
1. **Strengthen Core Revenue Categories**
   
   Why it matters: Fruits & Vegetables and Snack Foods generate **~$3M each**, over **20x** higher than low-performing categories, making them critical to overall revenue stability.
   
   How:
- Increase shelf space allocation for these categories by **20 to 30%** across all outlets
- Launch bundled promotions targeting a **10 to 15%** increase in average basket value within **30 days**
- Monitor KPIs: category revenue growth (**+10 to 15%**), inventory turnover rate, and basket size uplift
1. **Develop Second-Tier SKUs to Reduce Revenue Concentration Risk**
   
   Why it matters: Top SKUs (FDQ04, FDF38) dominate performance, while the next tier shows a **~50%** revenue drop, indicating untapped growth potential and high dependency risk.
   
   How:
- Implement cross-merchandising with top SKUs to drive at least **10%** uplift in visibility-driven sales
- Introduce pricing or discount trials (**5 to 10%**) to test demand sensitivity
1. **Test the Grocery Store Channel**
   
   Why it matters: At **$339.83**, the Grocery Store channel generates less than **10%** of the top-performing outlet, indicating low efficiency and potential misallocation of resources.
   
   How:
- Execute a two-month test period with a performance benchmark of minimum **25 to 40%** revenue growth
- If targets are not met, reallocate **30 to 50%** of inventory and staffing resources to higher-performing supermarket formats
1. **Optimize Low-Performing Categories**
   
   Why it matters: Categories like Seafood (**$149K**) generate over **20x** less revenue than top categories, indicating inefficient use of shelf space and capital.
   
   How:
- Reduce inventory levels for low-performing categories by **20 to 40%** in initial test outlets
- Reallocate freed shelf space to top-performing categories, targeting a **10 to 15%** increase in overall category revenue
- Run targeted promotions to test recovery potential, aiming for at least a **15%** increase before further reduction

-----

## 9. Deliverables

|Deliverable        |Description                                                 |
|-------------------|------------------------------------------------------------|
|📂 Excel Dashboard  |Interactive, slicer-driven, auto-refreshable via Power Query|
|📑 Presentation Deck|Structured, insight-driven storytelling for stakeholders    |

-----

## 10. Challenges & Resolution

**Challenge 1: Multi-dimensional aggregation**

> Selecting the right formulas to replicate DAX-style logic (% of total, YoY variance) without a full data model.

**Resolution:** Leveraged Pivot Tables with iterative validation, cross-checking outputs against manual totals before finalizing all KPIs.

-----

**Challenge 2: Dashboard design clarity**

> Translating complex pivot analysis into a single, navigable dashboard for non-technical stakeholders.

**Resolution:** Applied structured layout principles: KPI prioritization at the top, progressive disclosure via Slicers, and chart types and colors chosen for clarity over complexity.

------

*Built with Microsoft Excel · Power Query · Pivot Tables · Advanced Formulas*
