# 📊 E-Commerce Sales & Profitability Analysis (Excel Dashboard)

An interactive, executive-level business intelligence dashboard built in Microsoft Excel to analyze **1,194 e-commerce transaction records**. This project evaluates product category profitability, customer payment method adoption, order volume tiering, regional performance across US states, and price-to-profit margin efficiency.

---

## 🎯 Executive Summary & Key KPIs

* **Total Revenue:** **$6,182,639.00**
* **Total Net Profit:** **$1,610,697.00**
* **Overall Profit Margin:** **26.05%**
* **Total Orders Processed:** **1,194 orders**
* **Top Revenue Market:** **New York** ($1,130,048.00)

---

## 📸 Dashboard Overview

![Dashboard Preview](assets/dashboard_ecommerce1.jpeg)

> *The interactive dashboard features multi-cache Slicers filtering metrics dynamically by **State** and **Product Category**.*

---

## 🔑 Key Business Insights

1. **Category Profit Contribution:**
   * **Office Supplies** led total profit contribution ($551,575.00), closely followed by **Furniture** ($540,542.00) and **Electronics** ($518,580.00). All three core categories maintain balanced revenue generation (~$2.03M–$2.08M each).

2. **Payment Method Adoption:**
   * Digital payment modes represent the majority of transactions, with **Debit Card** (21.78%, 260 orders) and **Credit Card** (21.61%, 258 orders) leading adoption, followed closely by **UPI** (21.11%). Cash on Delivery (COD) represents the smallest volume share (17.25%).

3. **Order Basket Sizing:**
   * **Bulk Orders (>12 units)** drive the largest transaction share at **42.21%** (504 orders), demonstrating strong commercial and wholesale customer engagement.

4. **Sub-Category Revenue vs. Profit Efficiency (Scatter Analysis):**
   * **Printers** ($5,961.67 avg amount / $1,539.57 avg profit) and **Markers** ($5,707.95 avg amount / $1,588.63 avg profit) generate the highest average profit per order.
   * **Phones** ($1,124.82 avg profit) and **Pens** ($1,139.00 avg profit) record the lowest profit yield per transaction, highlighting opportunities for dynamic pricing adjustments.

---

## 🛠️ Data Architecture & Analytical Workflow

The underlying workbook is structured across 4 dedicated, modular tabs to preserve raw data integrity and support clear analytical execution:

> `[Raw_Data]` ➔ `[Working_Data]` ➔ `[Pivot_Tables]` ➔ `[Dashboard]`

* **`Raw_Data`**: Immutable source dataset of 1,194 transaction logs.
* **`Working_Data`**: Structured Excel Table (`SalesTable`) containing engineered helper columns:
  * **`Profit Margin %`**: `=[@Profit] / [@Amount]`
  * **`Quantity Tier`**: `=IF([@Quantity]<=5, "1. Small (1-5)", IF([@Quantity]<=12, "2. Medium (6-12)", "3. Bulk (>12)"))`
* **`Pivot_Tables`**: 6 dedicated Pivot Tables modeling category profit sums, payment frequency distributions, sub-category margin averages, quantity crosstabs, regional rankings, and a 3-column summary table for scatter coordinate mapping.
* **`Dashboard`**: Clean UI/UX view with gridlines removed, customized KPI scorecards, multi-connected cross-filtering slicers (`State`, `Category`), and cohesive color palette formatting.

---

## 📂 Repository Contents

| File Name | Description |
| :--- | :--- |
| `E-Commerce_Sales_&_Profitability_Dashboard.xlsx` | Complete 4-tab interactive Excel workbook |
| `assets/` | High-resolution dashboard screenshots and chart graphics |
| `README.md` | Project documentation and executive summary |

---

## 👤 Author

**Beta Catur Oktaviano**  
*Physics Student at IPB University | Data Analytics & Business Intelligence Enthusiast*   
* **Email:** oktaviano8989@gmail.com  
