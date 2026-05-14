# Sales-Report-US-Bike-Store
# 🚴 Performance Sales Dashboard — US Bike Store
> Turning 5 years of retail transaction data into strategic business decisions.

[Looker Studio] (https://datastudio.google.com/s/lD8FewLx_Aw)

[Google Sheets] (https://docs.google.com/spreadsheets/d/1LtI5xKywzNBJuwSr3d3SL73UA-WFNQxBOkPAAmgE16g/edit?usp=sharing)

---

## 📌 Project Overview

Most dashboards show you numbers. This one tells you what to do about them.

This project analyzes **1.3 million orders** across **6 countries** and **5 years (2011–2016)** for a bike retail company. The goal was to go beyond surface-level reporting and surface the kind of findings that directly affect strategic decisions — product mix, market prioritization, customer segmentation, and transaction quality.

Built as a **2-page interactive dashboard** in Looker Studio, the project covers everything from data preparation to business storytelling.

🔗 **[View Live Dashboard](https://datastudio.google.com/s/lD8FewLx_Aw)**

---

## 🗂️ Pages at a Glance

### Page 1 — Sales Performance Overview
Answers: *"How is the business performing overall?"*

| Component | Chart Type | Purpose |
|-----------|-----------|---------|
| Revenue, Profit, Profit Margin, Order Qty | Scorecard | Top-level KPI snapshot |
| Product Distribution | Geo Map | Revenue distribution by country |
| Revenue by Product Category | Donut Chart | Category contribution breakdown |
| Revenue by Sub-Category | Donut Chart | Sub-level product performance |
| Sales Trend | Line Chart | Revenue movement over time |
| Profit Trend | Line Chart | Profit movement over time |
| Top Product Sold | Table | Highest revenue-generating products |

### Page 2 — Customer Intelligence & Sales Behaviour
Answers: *"Who are our customers and how do they behave?"*

| Component | Chart Type | Purpose |
|-----------|-----------|---------|
| Customer Density | Geo Map | Customer distribution by country |
| Segmentation by Age | Bar Chart | Revenue contribution per age group |
| Segmentation by Gender | Donut Chart | Male vs Female revenue split |
| Average Order Value Trend | Line Chart | Transaction quality over time |
| Revenue per Transaction (Basket Size) | Bar Chart | Spend per transaction by country |
| Unit Sold vs Revenue per Country | Combo Chart | Volume vs value market detection |

---

## 🔍 Key Findings

### 1. Revenue Concentration Risk
> **72.5% of total revenue comes from Bikes alone.**

Road Bikes contributes $33.36M — nearly 40% of total company revenue from a single sub-category. Accessories ($15.12M) and Clothing ($8.37M) remain significantly underutilized as revenue streams.

### 2. Volume ≠ Value: Market Discrepancy Across Countries
> **The highest-volume market is not the highest-value market.**

| Country | Basket Size | Market Type |
|---------|-------------|-------------|
| Australia | $890 | High-value |
| Germany | $809 | Balanced |
| United Kingdom | $781.7 | Balanced |
| United States | $713.6 | High-volume |
| Canada | $559.7 | Low-value |

US leads in order volume (477.5K units) but ranks low on basket size — indicating a product mix skewed toward lower-priced items.

### 3. Untapped Segmentation Data
> **Adults (35–64) drive $42M+ in revenue yet receive no dedicated retention strategy.**

Gender split is near-equal at 50.8% Male / 49.2% Female — meaning marketing should be age-driven, not gender-driven. Young Adults (25–34) sit at $30M and represent a high-potential segment for long-term nurturing.

### 4. AOV Volatility Goes Undetected
> **Revenue grew through volume, not transaction value.**

AOV fluctuated between near-zero and $4K with no monitoring system in place. Spikes likely indicate bulk/corporate purchases that were never capitalized on. Consistent decline in AOV during certain periods correlates with a product mix shift toward Accessories.

---

## 💡 Strategic Recommendations

| Finding | Recommended Action | Estimated Impact |
|---------|-------------------|-----------------|
| 72.5% revenue from Bikes | Structured cross-sell program (Bikes → Accessories) | +$6.2M potential |
| Market value gap | 3-tier market strategy (Australia: expand, US: upsell, Canada: audit) | +$45M potential from US alone |
| Age segmentation underused | Loyalty program for Adults 35–64 | +$4.2M from repeat purchase |
| AOV not monitored | Set AOV as monthly KPI with threshold alerts | +$117M cumulative potential |

---

## 🛠️ Technical Details

### Data Preparation
- Raw dataset: transaction-level records with Date, Demographics, Product, and Financial columns
- Created **TRX ID** as unique transaction identifier
- Built calculated fields for AOV and Basket Size directly in Looker Studio
- No Customer ID available — analysis adapted to transaction-based approach

### Calculated Fields (Looker Studio)
```
Average Order Value (AOV) = SUM(Revenue) / SUM(Order_Quantity)

Basket Size = SUM(Revenue) / COUNT(TRX_ID)
```

### Filters Applied
All dashboard filters (Country, State, Product Category, Sub-Category, Product, Date Range) are cross-page and interactive — selections on Page 1 carry context into Page 2.

---

## ⚠️ Limitations & Honest Notes

- No Customer ID in the dataset — customer-level analysis (CLV, churn, repeat rate) is not possible from this data
- YoY comparison requires blended data sources in Looker Studio due to the absence of a native PREVIOUS PERIOD function
- AOV spikes may indicate data anomalies or bulk orders — further investigation would require order-level detail beyond what's available

---

## 📁 Repository Contents

```
📦 bike-store-dashboard
 ┣ 📂 assets
 ┃ ┣ 📸 page1-overview.png
 ┃ ┣ 📸 page2-customer-intelligence.png
 ┃ └ 📸 data-sample.png
 ┣ 📄 README.md
 └ 📄 data-dictionary.md
```

---

## 👤 About

Made by **SYAHRAIN KUSWANDA**
📎 [LinkedIn](https://www.linkedin.com/in/syahrainkuswanda/) · 🔗 [Live Dashboard](https://datastudio.google.com/s/lD8FewLx_Aw)

---

*Dataset covers 2011–2016 retail transactions across United States, Australia, United Kingdom, Canada, Germany, and France.*
