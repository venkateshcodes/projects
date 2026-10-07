# Bank Loan Analytics Dashboard — Client Questions & Data Analyst Insights

## Overview

This project demonstrates how a **Senior Data Analyst** turns transactional loan origination data and an enterprise Power BI dashboard into an executive client-facing business conversation[cite: 1].

The example client is **ApexBank Lending** (fictional)[cite: 1]. The analysis uses:

- `Financial_loan_data.xlsx`[cite: 1]
- `Bank Loan Analytics Dashboard.pbix`[cite: 1]
- `Bank Loan Description.pdf`
- `Problem Statement.pptx`
- `PPT.pptx`[cite: 1]

The dashboard covers **Portfolio Quality, Good vs. Bad Loans, Lending Operations, Capital Recovery, Risk Segmentation, and Geographic Distribution**[cite: 1].

## Business Problem

A bank executive does not normally ask:

> “Show me a donut chart.”

They ask business-critical lending questions such as:

- How healthy is our overall loan portfolio[cite: 1]?
- What percentage of our capital is tied up in defaulted loans[cite: 1]?
- Which loan terms carry the highest risk of charge-off[cite: 1]?
- Which borrower purposes drive the largest cash volume and nominal write-offs[cite: 1]?
- Are higher interest rates actually compensating for lower-tier borrower risk[cite: 1]?
- How much cash have we recovered from bad loans versus what we disbursed[cite: 1]?
- Where should credit risk policy and underwriting thresholds tighten next[cite: 1]?

The purpose of this project is to map those questions directly to visual answers, report verified dataset metrics, and translate findings into operational underwriting recommendations[cite: 1].

## Project Files & Resources

| Resource | Description | Link |
|---|---|:---:|
| 📄 Client Analysis Document | Complete 20-question business guide, visual answers, next-level questions & recommendations (.docx)[cite: 1] | [View Client Analysis Document](Bank_Loan_Analytics_Client_Questions_and_Insights.docx)[cite: 1] |
| 📊 Excel Dataset | Cleaned institutional loan dataset (38,576 records, 24 attributes)[cite: 1] | [View Loan Dataset](Financial_loan_data.xlsx)[cite: 1] |
| 📈 Power BI Dashboard | Multi-page interactive Power BI reporting model (.pbix)[cite: 1] | [Open Power BI Dashboard](Bank%20Loan%20Analytics%20Dashboard.pbix)[cite: 1] |
| 📊 Final Presentation Deck | Executive stakeholder summary slide deck (.pptx)[cite: 1] | [View Presentation PPT](PPT.pptx)[cite: 1] |
| 📋 Problem Statement | Business requirements, KPIs, and visual mockups (.pptx)[cite: 1] | [View Problem Statement](Problem%20Statement.pptx)[cite: 1] |
| 🖼️ Dashboard Screenshot | High-resolution operational screenshot gallery | [View Dashboard Screenshots](#dashboard-screenshots) |

### Dashboard Screenshots

The project includes an operational visual gallery:

![Dashboard Overview](https://github.com/venkateshcodes/projects/blob/e155ae8d766513323aeac1bd1a190bd05d512560/Power%20Bi%20Projects/Bank%20Loan%20Analytics/Project%20Previeww.png)

**[Open Full Dashboard Overview Screenshot](screenshots/dashboard-overview.png)**

> **Tip:** Additional granular views are organized under the `screenshots/` directory (`summary-page.png`, `overview-page.png`, `loan-status.png`, and `geography.png`).

## Dataset Summary

| Area / Entity | Records | Main Fields |
|---|---:|---|
| Loan Applications | 38,576[cite: 1] | `id`, `member_id`, `issue_date`, `loan_amount`, `funded_amount`, `term`, `int_rate`, `installment`[cite: 1] |
| Risk & Underwriting | 38,576[cite: 1] | `grade`, `sub_grade`, `verification_status`, `loan_status` (`Fully Paid`, `Current`, `Charged Off`)[cite: 1] |
| Borrower Profile | 38,576[cite: 1] | `emp_title`, `emp_length`, `home_ownership`, `annual_income`, `dti`, `address_state`, `purpose`, `total_acc`[cite: 1] |
| Cash Repayments | 38,576[cite: 1] | `total_payment`, `last_payment_date`, `next_payment_date`, `last_credit_pull_date` |

## Executive KPIs

- **Total Loan Applications:** 38,576 (4,314 MTD Dec \| +6.9% MoM)[cite: 1]
- **Total Funded Amount:** $435,757,075 / $435.8M ($54.0M MTD Dec \| +13.0% MoM)[cite: 1]
- **Total Amount Received:** $473,070,019 / $473.1M ($58.1M MTD Dec \| +15.8% MoM)[cite: 1]
- **Average Interest Rate:** 12.05% (12.36% MTD Dec \| +3.5% MoM / +41 bps)[cite: 1]
- **Average Debt-to-Income (DTI):** 13.33% (13.68% MTD Dec \| +2.7% MoM / +36 bps)[cite: 1]
- **Good Loan %:** 86.18% (33,243 applications \| $370.2M funded \| $435.8M received)[cite: 1]
- **Bad Loan %:** 13.82% (5,333 charged-off applications \| $65.5M funded \| $37.3M received)[cite: 1]

> **Important:** Good Loans include both `Fully Paid` and `Current` facilities[cite: 1]. Bad Loans represent `Charged Off` accounts where unrecovered principal equals -$28,247,462[cite: 1]. Net portfolio cash flow remains positive at +$37.31M (1.085x recovery multiple)[cite: 1].

## Client Questions → Visualization Answers

### 1. How healthy is our overall loan portfolio?

**Visualization:** Good Loan vs. Bad Loan KPI Donut Chart & Portfolio Status Summary Cards[cite: 1]

**Answer:** 86.18% Good Loans (33,243 loans, $370.2M funded) vs. 13.82% Bad Loans (5,333 loans, $65.5M funded)[cite: 1].

**Analyst interpretation:** Portfolio health exceeds subprime benchmarks, but the 13.82% charge-off rate ties up $65.5M in non-performing assets[cite: 1].

### 2. What is our net cash recovery on charged-off debt?

**Visualization:** Loan Status Grid View + Funded vs. Received Clustered Bar Chart[cite: 1]

**Answer:** On Bad Loans, the bank disbursed $65,532,225 but collected only $37,284,763, creating an unrecovered principal deficit of -$28,247,462 (0.569x recovery multiple)[cite: 1].

**Analyst interpretation:** While Good Loans yield a surplus of +$65.6M to cover losses, early post-default collection intervention is needed within 60 days of delinquency[cite: 1].

### 3. Which loan term carries the highest volume, and where does risk diverge?

**Visualization:** Loan Term Donut Chart & Tenor Risk Matrix[cite: 1]

**Answer:** 36-month loans represent 73.2% of originations (~28,237 loans, ~$273M funded), while 60-month loans represent 26.8% (~10,339 loans, ~$162.7M funded)[cite: 1]. However, 60-month loans default at ~22.6% compared to ~10.6% for 36-month loans[cite: 1].

**Analyst interpretation:** Prolonged 5-year repayment structures more than double borrower default probability[cite: 1].

### 4. Which loan purpose drives the most volume?

**Visualization:** Loan Purpose Breakdown Bar Chart[cite: 1]

**Answer:** Debt consolidation leads the portfolio with >47% of total volume (~18,214 applications and ~$217M funded principal)[cite: 1]. Credit cards rank second (~5,000 loans, ~$60M)[cite: 1].

**Analyst interpretation:** Over 60% of aggregate lending represents consumer debt refinancing[cite: 1]. Direct disbursement to existing creditors is required to prevent secondary re-leveraging[cite: 1].

### 5. Which loan purpose carries the highest default rate?

**Visualization:** Purpose by Loan Status Stacked Bar Chart & Default Rate Matrix[cite: 1]

**Answer:** Small business loans exhibit the highest individual charge-off rate at ~27.1%[cite: 1]. In nominal dollars, debt consolidation drives the largest aggregate loss (~$34.5M charged off)[cite: 1].

**Analyst interpretation:** Unsecured personal borrowing for small business needs shows excessive commercial volatility[cite: 1].

### 6. How does credit tiering (Grades A–G) correlate with risk?

**Visualization:** Loan Grade vs. Interest Rate & Default Rate Dual-Axis Chart[cite: 1]

**Answer:** Grade A carries a 7.3% average rate and a 5.9% default rate[cite: 1]. Risk scales progressively to Grade D (15.8% rate, 21.0% default) and Grade G (20.9% rate, 33.8% default)[cite: 1].

**Analyst interpretation:** Yield premiums on Grades F and G do not offset loss-given-default rates exceeding 30%[cite: 1]. Cap low-grade exposures at 3.5% of total volume[cite: 1].

### 7. Which states represent our highest capital exposure?

**Visualization:** Regional Analysis Filled Map (by Address State)[cite: 1]

**Answer:** California leads with ~6,894 applications (~$79.5M funded), followed by New York (~3,700 loans, ~$42M), Texas (~2,650 loans, ~$30M), Florida (~2,300 loans, ~$26M), and New Jersey (~1,800 loans, ~$21M)[cite: 1].

**Analyst interpretation:** The top 5 states account for ~45% of total portfolio disbursement, creating significant geographic concentration risk[cite: 1].

### 8. Which states demonstrate elevated default rates?

**Visualization:** State-Level Delinquency Heat Map & Ranking Table[cite: 1]

**Answer:** Nevada (NV), Florida (FL), and Mississippi (MS) display charge-off rates between 15.5% and 17.2%, surpassing the national 13.82% benchmark[cite: 1].

**Analyst interpretation:** Regional cost-of-living and employment variables require automated +50 bps rate premiums or 20-point scorecard overlays[cite: 1].

### 9. How does home ownership affect credit reliability?

**Visualization:** Home Ownership Treemap & Risk Breakdown[cite: 1]

**Answer:** Renters (~18,440 loans) and Mortgage holders (~17,190 loans) comprise ~90% of originations[cite: 1]. Outright homeowners comprise ~7.4% (~2,840 loans)[cite: 1]. Default rates are highest for Renters (14.9%) versus Mortgage holders (12.8%) and Owners (12.5%)[cite: 1].

**Analyst interpretation:** Homeowners possess stronger balance sheets and default less often[cite: 1].

### 10. Does employment stability (emp_length) insulate against default?

**Visualization:** Employee Length Analysis Bar Chart[cite: 1]

**Answer:** Borrowers with 10+ years of employment form the largest cohort (~8,890 loans, ~$112M funded)[cite: 1]. However, default rates remain flat across tenure (~13.1% to 14.2%, with 10+ year workers defaulting at 13.5%)[cite: 1].

**Analyst interpretation:** Experienced workers borrow higher balances ($12,500 avg vs $9,800 for <1 yr), equalizing default probability[cite: 1]. Disposable free cash flow is a more critical approval metric than tenure alone[cite: 1].

### 11. What is the impact of borrower leverage (DTI)?

**Visualization:** Average DTI Distribution Histogram & Loan Status DTI Matrix[cite: 1]

**Answer:** Overall average DTI is 13.33%[cite: 1]. Charged-off loans exhibit an average DTI of 14.00% versus 13.17% for fully paid loans[cite: 1].

**Analyst interpretation:** Borrowers allocating over 14% of gross income to fixed debt service show significantly higher vulnerability[cite: 1]. Impose hard approval cutoffs at 20% DTI[cite: 1].

### 12. How did loan origination trend over the calendar year?

**Visualization:** Monthly Trends by Issue Date Line & Clustered Bar Chart[cite: 1]

**Answer:** Lending surged from ~1,560 loans ($17.5M funded) in January to 4,314 loans ($54.0M funded) in December (+208% funding growth)[cite: 1].

**Analyst interpretation:** Aggressive Q4 originations present concentrated portfolio seasoning risk in the following operational year[cite: 1].

### 13. Does third-party income verification reduce default rates?

**Visualization:** Verification Status vs. Loan Status Matrix[cite: 1]

**Answer:** Verified loans exhibit a higher default rate (~15.2%) than Not Verified loans (~12.1%)[cite: 1].

**Analyst interpretation:** Adverse underwriting selection—underwriters trigger manual income verification primarily on borderline or high-risk applicants[cite: 1].

## Additional Questions a Real Client May Ask

1. How do default rates migrate across sub-grades (A1 to G5)[cite: 1]?
2. What is our post-default recovery curve at 90, 180, and 365 days[cite: 1]?
3. What is the cumulative default risk when combining Grade D–G, 60-month terms, and Renters[cite: 1]?
4. Does the large Q4 origination surge create higher first-payment default (FPD) rates[cite: 1]?
5. What proportion of loans pay off early, and how does prepayment speed (CPR) impact net interest yield[cite: 1]?
6. Do debt consolidation borrowers re-default or take on secondary revolving debt[cite: 1]?
7. How do state-level usury rate caps correlate with debt recovery outcomes[cite: 1]?
8. At what interest rate threshold do prime Grade A and B borrowers walk away[cite: 1]?
9. Can a machine learning model (XGBoost/Logistic Regression) predict probability of default at point-of-sale with an AUC ROC > 0.82[cite: 1]?
10. How does borrower credit utilization in the 90 days before default impact Exposure at Default (EAD)[cite: 1]?
11. How would a 200 bps macroeconomic interest rate shock impact portfolio charge-offs and capital reserve requirements[cite: 1]?
12. Which fully paid customer cohorts show the highest lifetime value (CLV) for cross-selling mortgages or auto loans[cite: 1]?

## Recommended Next Improvements

- Enforce hard term caps eliminating 60-month loans for borrowers below Grade C or DTI > 16%[cite: 1].
- Implement direct third-party disbursement for debt consolidation to avoid consumer re-leveraging[cite: 1].
- Separate unsecured small business lending into commercial underwriting scorecards requiring DSCR validation[cite: 1].
- Implement DAX Calculation Groups in Power BI to toggle visuals across Funded Amount, Applications, and Default Rate[cite: 1].
- Add interactive What-If sensitivity sliders for credit loss provisioning[cite: 1].
- Configure automated drill-through from summary charts directly to loan-level transactional ledgers[cite: 1].
- Embed dynamic report-page tooltips on the geographic map with 12-month default trendlines[cite: 1].
- Formalize institutional Net Charge-Off (NCO) and First Payment Default (FPD) tracking measures[cite: 1].
- Migrate flat Excel data to an Azure SQL / Microsoft Fabric Star Schema architecture[cite: 1].

## Suggested Presentation Flow

**1. Executive summary** → 38,576 applications, $435.8M funded, $473.1M collected, +13% MoM growth[cite: 1]  
**2. Portfolio quality** → 86.2% Good Loans ($370.2M) vs. 13.8% Bad Loans ($65.5M)[cite: 1]  
**3. Credit risk & grade analysis** → default rates across Grade A (5.9%) to Grade G (33.8%)[cite: 1]  
**4. Geography & exposure** → top 5 volume states (CA, NY, TX, FL, NJ) and delinquency hot spots (NV, FL)[cite: 1]  
**5. Loan purpose dynamics** → debt consolidation volume vs. small business default risk (27.1%)[cite: 1]  
**6. Recommendations & roadmap** → underwriting term limits, direct disbursement, calculation groups, and lakehouse migration[cite: 1]

## Files

- `Financial_loan_data.xlsx` — cleaned institutional loan dataset (38,576 rows)[cite: 1]
- `Bank Loan Analytics Dashboard.pbix` — interactive Power BI dashboard[cite: 1]
- `Bank_Loan_Analytics_Client_Questions_and_Insights.docx` — client questions and analyst interpretation guide[cite: 1]
- `PPT.pptx` — final stakeholder executive presentation[cite: 1]
- `Problem Statement.pptx` — project specifications and KPI business requirements[cite: 1]
- `README.md` — GitHub project portfolio documentation

## Disclaimer

The entity **ApexBank Lending** is fictional and used strictly as a client-presentation case study[cite: 1]. All loan metrics, percentages, dollar figures, and operational distributions are calculated directly from `Financial_loan_data.xlsx`[cite: 1]. Measure calculations should be aligned with institutional credit committees before regulatory submission[cite: 1].
