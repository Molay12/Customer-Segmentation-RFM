# Customer Segmentation & RFM Analysis | Python & Power BI

## Project Overview

This project analyzes retail transaction data to identify valuable customers, understand purchasing behavior, and develop targeted customer retention strategies using RFM (Recency, Frequency, Monetary) Analysis.

The objective is to help marketing teams identify high-value customers, prioritize at-risk customers, and make informed customer retention and budget allocation decisions.

## Business Problem

Which customer segments provide the greatest value to the business, and how should marketing prioritize retention campaigns?

## Tools & Technologies

- Python
- Pandas and NumPy
- Jupyter Notebook
- Power BI
- DAX
- Microsoft Excel

## Dataset

**Source:** [UCI Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail)

- Original transactions: 541,909
- Analysis period: December 2010 – December 2011
- Unique customers after cleaning: 4,338

## Data Cleaning & Preparation

- Removed duplicate transactions.
- Removed records with missing Customer IDs.
- Excluded cancelled invoices.
- Removed transactions with invalid quantities or unit prices.
- Calculated transaction revenue using Quantity × UnitPrice.
- Prepared a clean dataset for customer-level analysis.

**Final dataset:** 392,692 transactions and 4,338 customers.

## RFM Analysis Methodology

RFM analysis evaluates customers using three purchasing behaviour metrics:

| Metric | Meaning | Business Interpretation |
|---|---|---|
| Recency (R) | Days since the customer's last purchase | Lower recency indicates more recent activity |
| Frequency (F) | Number of unique invoices | Higher frequency indicates more repeat purchases |
| Monetary (M) | Total customer spending | Higher monetary value indicates greater revenue contribution |

### RFM Scoring

- Customers are divided into five scoring groups for each RFM metric.
- Recency is scored in reverse order: fewer days since the last purchase receive a higher score.
- Frequency and Monetary are scored in ascending order: higher values receive higher scores.
- Each metric receives a score from 1 to 5.

**Combined RFM score:**

`RFM Total = R Score + F Score + M Score`

The combined score ranges from 3 to 15.

### Customer Segmentation

The analysis identifies five customer segments:

- **Champions:** Recent, frequent, and high-value customers.
- **Loyal:** Customers who purchase repeatedly and contribute consistent value.
- **At Risk:** Previously valuable customers who have not purchased recently.
- **New / Potential:** Customers with opportunities to develop repeat purchasing behaviour.
- **Lost:** Customers with long periods of inactivity and low engagement.

## Power BI Dashboard

### Page 1 — Customer Segmentation

- Total customer overview
- Gross sales overview
- At-risk customer count
- Customer distribution by segment
- Gross sales by segment
- Customer purchase behavior scatter chart
- Interactive segment filtering

### Page 2 — Retention & Budget Strategy

- Proposed marketing budget allocation
- Segment-level budget distribution
- Customer-level action table
- Recommended marketing actions
- Interactive page navigation

## Proposed Marketing Budget Allocation

| Customer Segment | Proposed Allocation |
|---|---:|
| At Risk | 30% |
| Champions | 25% |
| Loyal | 25% |
| New / Potential | 10% |
| Lost | 10% |
| **Total** | **100%** |

*Budget allocations are strategic recommendations and have not been validated against actual campaign ROI data.*

## Key Findings

- Identified 4,338 customers across five RFM segments.
- Champions represent 941 customers and are a priority group for loyalty and VIP strategies.
- At Risk customers represent 466 customers and are candidates for targeted win-back campaigns.
- Lost customers form the largest segment, with 1,269 customers, suggesting an opportunity to test low-cost reactivation strategies.
- New / Potential customers can be encouraged to make a second purchase.

## Business Recommendations

1. Retain Champions through exclusive rewards and personalized experiences.
2. Encourage Loyal customers to increase repeat purchases.
3. Prioritize At Risk customers for win-back campaigns.
4. Convert New / Potential customers into repeat buyers.
5. Use cost-controlled reactivation campaigns for Lost customers.

## Project Limitations

- The dataset does not contain actual marketing campaign expenditure or campaign outcomes.
- Customer segmentation is based on historical purchasing behaviour.
- Proposed budget allocation requires validation through controlled marketing experiments.
- RFM segments represent analytical classifications, not guaranteed future customer behaviour.
- Gross sales do not represent profit or net revenue.

## Conclusion

This project demonstrates how Python-based data preparation, RFM analysis, and Power BI visualization can transform retail transaction data into actionable customer retention strategies and business recommendations.

## Repository Structure

```text
Customer-Segmentation-RFM/
│
├── 01_RFM_Analysis.ipynb
├── customer_rfm.csv
├── segment_summary.csv
├── Retail_Ecommerce_Customer_Segmentation_RFM.pbix
├── customer_segmentation.png
├── retention_budget_strategy.png
└── README.md
```

## Dashboard Screenshots

### Page 1 — Customer Segmentation

![Customer Segmentation Dashboard](customer_segmentation.png)

### Page 2 — Retention & Budget Strategy

![Retention & Budget Strategy Dashboard](retention_budget_strategy.png)

