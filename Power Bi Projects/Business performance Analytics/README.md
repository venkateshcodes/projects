# Business Analysis Dashboard — Client Questions & Data Analyst Insights

## Overview

This project demonstrates how a **Data Analyst** can turn a cleaned MIS dataset and a Power BI dashboard into a client-facing business conversation.

The example client is **NovaTech Electronics** (fictional). The analysis uses:

- `MIS_Cleaned_Data.xlsx`
- `Business_Analysis_Dashboard.pbix`

The dashboard covers **Sales, Operations, Finance and CRM**.

## Business Problem

A client does not normally ask:

> “Show me a bar chart.”

They ask business questions such as:

- How much are we selling?
- Which region is performing best?
- Which products drive revenue?
- Where are leads getting stuck?
- Are payments overdue?
- Which warehouse is fastest?
- Where should management focus next?

The purpose of this project is to map those questions to the correct visualization and explain the business meaning of the answer.

## Project Files & Resources

| Resource | Description | Link |
|---|---|---|
| 📄 Client Analysis Document | Client questions, visualization answers, insights and recommendations | [View Client Analysis Document](https://github.com/venkateshcodes/projects/blob/b60e56f6269adaf8bc8587fbf93cf99b0701e825/Power%20Bi%20Projects/Business%20performance%20Analytics/Business_Analytics_Client_Questions_and_Insights.docx) |
| 📊 Excel Dataset | Cleaned MIS dataset used for the analysis | [View MIS Cleaned Data](https://github.com/venkateshcodes/projects/blob/b60e56f6269adaf8bc8587fbf93cf99b0701e825/Power%20Bi%20Projects/Business%20performance%20Analytics/MIS_Cleaned_Data.xlsx) |
| 📈 Power BI Dashboard | Interactive Power BI business analysis dashboard | [Open Power BI Dashboard](https://github.com/venkateshcodes/projects/blob/b60e56f6269adaf8bc8587fbf93cf99b0701e825/Power%20Bi%20Projects/Business%20performance%20Analytics/Business_Analysis_Dashboard.pbix) |
| 🖼️ Dashboard Screenshot | Preview image of the Power BI dashboard | [View Dashboard Screenshot](https://github.com/venkateshcodes/projects/blob/b60e56f6269adaf8bc8587fbf93cf99b0701e825/Power%20Bi%20Projects/Business%20performance%20Analytics/Project_Preview.png) |
| 👉 Presentation | Overall Presentation | [View Presentation ](https://github.com/venkateshcodes/projects/blob/bce1f0847cb27715e28eae52c9a1455477a65419/Power%20Bi%20Projects/Business%20performance%20Analytics/MIS%20Intern%20PPT.pptx) |


### Dashboard Screenshot

The current project includes a dashboard preview:

![Dashboard Overview](https://github.com/venkateshcodes/projects/blob/b60e56f6269adaf8bc8587fbf93cf99b0701e825/Power%20Bi%20Projects/Business%20performance%20Analytics/Project_Preview.png)

**[Open Full Dashboard Screenshot](https://github.com/venkateshcodes/projects/blob/b60e56f6269adaf8bc8587fbf93cf99b0701e825/Power%20Bi%20Projects/Business%20performance%20Analytics/Project_Preview.png)**

> **Tip:** If you later add more screenshots, place them in a `screenshots/` folder and link them with normal Markdown image syntax.

## Dataset Summary

| Area | Records | Main fields |
|---|---:|---|
| Sales | 1,500 | Order, customer, product, price, units, region, date, amount, channel |
| Operations | 1,500 | Warehouse, inventory, shipment date, fulfillment days |
| Finance | 1,500 | Expense, budget, payment status, due date, expense type |
| CRM | 1,500 | Customer, lead, lead status, contact date, conversion rate |

## Executive KPIs

- **Total sales:** ₹13.41 Cr
- **Orders:** 1,500
- **Units sold:** 74,650
- **Average conversion-rate field:** 0.6%
- **Average fulfillment:** 7.72 days
- **Finance records marked overdue:** 480 / 1,500 = 32.0%

> **Important:** The overdue percentage above is calculated from raw record status. Before client reporting, confirm that the Power BI `Overdue %` measure uses the same denominator and business definition.

## Client Questions → Visualization Answers

### 1. How much revenue are we generating?

**Visualization:** Total Amount KPI

**Answer:** ₹13.41 Cr across 1,500 orders.

**Analyst interpretation:** This is the executive sales headline. Drill into time, region, product and channel to understand the drivers.

### 2. Which month performed best?

**Visualization:** Monthly Performance line chart

**Answer:** March 2024 was the highest month at ₹3.42 Cr. January was lowest at ₹3.18 Cr.

### 3. Which region contributes the most?

**Visualization:** Region Status bar chart

**Answer:**
- East — ₹3.57 Cr
- North — ₹3.37 Cr
- West — ₹3.24 Cr
- South — ₹3.23 Cr

**Analyst interpretation:** East is the strongest revenue region. Compare it with customer count, marketing spend and fulfillment before changing regional investment.

### 4. Which product drives revenue?

**Visualization:** EC Product Status

**Answer:**
- Mobiles — ₹5.56 Cr
- Laptop — ₹2.77 Cr
- Mobile — ₹2.67 Cr
- Phone — ₹2.41 Cr

**Analyst interpretation:** Mobiles are the largest revenue contributor. Revenue is not the same as profit; margin data is required for profitability decisions.

### 5. Which channel is strongest?

**Visualization:** Channel Mode Status + Sales data

**Revenue answer:**
- Online — ₹6.54 Cr
- Offline — ₹3.66 Cr
- Retail — ₹3.21 Cr

**Analyst interpretation:** Online leads by revenue. The Power BI channel visual counts operational orders, so order volume and revenue should be interpreted separately.

### 6. Where are leads getting stuck?

**Visualization:** Lead Status funnel

**Answer:**
- Converted — 390
- Closed — 382
- In-Progess — 360
- Open — 368

**Analyst interpretation:** Open and in-progress leads represent a pipeline-management opportunity. Investigate lead source, response time and sales ownership.

### 7. What is the conversion performance?

**Visualization:** Conversion Rate KPI

**Answer:** 0.6% average Conversion_Rate field.

**Next step:** Define conversion consistently as converted leads / eligible leads and segment it by lead source, product, region and salesperson.

### 8. Where are we spending the most?

**Visualization:** Expense category pie chart

**Answer:** Marketing is the largest recorded expense category at ₹3.31 Cr.

**Next step:** Compare spend with budget and business outcomes such as revenue and conversion.

### 9. How serious is overdue finance activity?

**Visualization:** Over Due (%) KPI + Finance analysis

**Answer:** 480 of 1500 finance records are marked Overdue (32.0%).

**Next step:** Report overdue **amount**, aging, category and invoice-level exposure rather than relying only on record count.

### 10. Which warehouse has the most inventory?

**Visualization:** Inventory Level treemap

**Answer:**
- WH - B — 406,336.0
- WH - C — 405,162.0
- WH - A — 389,189.0

### 11. Which warehouse is fastest?

**Visualization:** Warehouse slicer + Operations analysis

**Answer:** WH - A is fastest at 7.54 days average; WH - C is slowest at 7.83 days.

## Additional Questions a Real Client May Ask

1. What is gross margin by product?
2. Which customers have the highest lifetime value?
3. Which marketing source gives the best conversion?
4. What is average order value by channel?
5. Which lead source generates the most converted customers?
6. How long does a lead take to convert?
7. Which warehouses have excess inventory?
8. Which products are at stock-out risk?
9. Which expenses are above budget?
10. What is the overdue amount and aging?
11. Does fulfillment time affect repeat purchases?
12. Can we forecast next month's sales and inventory?

## Recommended Next Improvements

- Add cost, gross profit and margin fields.
- Normalize product names (`Mobile`, `Mobiles`, `Phone`) using a product master.
- Add customer segmentation and customer lifetime value.
- Add lead source, sales owner and conversion timestamps.
- Add inventory reorder points and stock-out flags.
- Add overdue amount and aging buckets.
- Add a longer historical period for trend and forecasting.
- Add drill-through pages from KPI → category → transaction.
- Document every KPI definition and denominator.

## Suggested Presentation Flow

**1. Executive summary** → revenue, units, conversion  
**2. Sales performance** → month, region, product, channel  
**3. Customer funnel** → open → in-progress → closed → converted  
**4. Finance risk** → expense categories and overdue exposure  
**5. Operations** → inventory and fulfillment  
**6. Recommendations** → decisions, additional data and next dashboard version

## Files

- `MIS_Cleaned_Data.xlsx` — source MIS workbook
- `Business_Analysis_Dashboard.pbix` — Power BI dashboard
- `Business_Analytics_Client_Questions_and_Insights.docx` — detailed client-question and analyst-answer document
- `README.md` — GitHub project documentation

## Disclaimer

The business name **NovaTech Electronics** is fictional and used only as a client-presentation example. The numerical findings are derived from the supplied workbook. Dashboard measure definitions should be validated with the business owner before external reporting.
