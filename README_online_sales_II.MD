# Online Retail II – Customer & Product Analytics

## 1. Business Problem

The retail business aims to better understand customer behavior and product performance in order to improve revenue, customer retention, and marketing efficiency.

Key business questions include:

* Who are the most valuable customers?
* How are customers distributed in terms of engagement and spending behavior?
* Which customer segments contribute most to revenue?
* Is revenue concentrated in a small group of customers (Pareto effect)?
* Which products and countries drive the majority of sales?
* How does revenue evolve over time, and are there seasonal patterns?

---

## 2. Dataset Overview

The dataset used is the **Online Retail II** dataset, which contains transactional data from a UK-based online retail store.

It includes:

* Invoice number
* Product description
* Quantity
* Unit price
* Invoice date
* Customer ID
* Country

Each row represents a single product line item in a transaction.

---

## 3. Data Cleaning

Before analysis, several data cleaning steps were performed:

* Removed records with missing `Customer ID`
* Removed cancelled transactions (invoice starting with "C")
* Removed negative or zero quantities
* Removed negative or zero prices
* Created a `TotalPrice` column (`Quantity × Unit Price`)
* Converted date columns to proper datetime format

---

## 4. Methodology (RFM Analysis)

Customer segmentation was performed using the **RFM framework**:

* **Recency (R):** How recently a customer made a purchase
* **Frequency (F):** How often a customer purchases
* **Monetary (M):** How much money a customer spends

Each metric was converted into a score (1–5) using quantiles.

These scores were then combined into an RFM score to enable behavioral segmentation.

---

## 5. Customer Segmentation

Customers were grouped into behavioral segments:

* Champions
* Loyal Customers
* Potential Loyalists
* New Customers
* Needs Attention
* At Risk
* Lost Customers

---

## 6. Product Performance Analysis

### Revenue vs Quantity Sold

Revenue and quantity sold do not always align. Some products with high sales volume do not necessarily generate the highest revenue.

---

### High-Value Products with Lower Volume

The product **“PAPER CHAIN KIT 50'S CHRISTMAS”** ranks 7th in revenue but 22nd in quantity sold, indicating that high revenue can be driven by relatively lower volume products.

---

### Product Contribution is Highly Skewed

Revenue is concentrated in a small number of top-performing products, showing a clear Pareto-like distribution in product performance.

---

### Product Popularity vs Profitability

There is a clear distinction between product popularity (quantity sold) and profitability (revenue contribution), highlighting the importance of analyzing both metrics together.

---

### Monthly Revenue Trend and Seasonality

Monthly revenue shows a consistent year-over-year growth trend, indicating overall business expansion.

Strong seasonality is observed, with revenue peaking between **July and January**, while early months of the year tend to be weaker.

---

### Data Limitation

Without cost or margin data, profitability analysis remains limited to revenue-based evaluation.

---

## 7. Country-Level Analysis

### Domestic Market Dominance

The majority of revenue comes from the **United Kingdom**, which is expected as the retail store is based in the UK. This indicates strong domestic market dominance.

---

### International Market Distribution

When excluding the UK from the analysis, revenue distribution changes significantly:

* The **Netherlands** and the **Republic of Ireland (EIRE)** emerge as the top-performing international markets.
* This suggests that while the UK drives the core revenue base, there is also meaningful demand in select European markets.

---

### Strategic Implications

These findings highlight the importance of:

* Maintaining strong domestic performance in the UK as the primary revenue driver
* Exploring targeted growth opportunities in high-performing international markets such as the Netherlands and Ireland
* Balancing focus between core market dominance and international expansion

---

## 8. Key Insights

### Revenue is highly concentrated among top customers

The Champions segment contributes 69.3% of total revenue, despite representing only 25.2% of customers.

---

### Strong Pareto Effect is observed

The top 23% of customers generate 80% of total revenue.

---

### Large portion of customers are inactive or low value

* Lost Customers: 25.9% of customers, only 3.8% of revenue
* Needs Attention: 14.6% of customers, only 4.0% of revenue

---

## 9. Business Recommendations

### 1. Retain high-value customers

Focus on Champions and Loyal Customers through loyalty programs and personalization.

### 2. Reactivate at-risk customers

Use targeted campaigns to prevent churn.

### 3. Re-engage lost customers selectively

Prioritize high historical value customers.

### 4. Optimize product strategy

Focus on both high-revenue and high-volume products.

### 5. Strengthen seasonal planning

Align marketing and inventory with peak demand periods (July–January).

### 6. Balance domestic and international growth

Maintain UK dominance while expanding in strong secondary markets such as Netherlands and Ireland.

---

## Final Takeaway

This analysis demonstrates that revenue is driven by a combination of a small group of high-value customers, a limited set of high-performing products, and strong seasonal demand patterns.

By integrating **customer segmentation, product performance, seasonality, and country-level insights**, the business can make more precise, data-driven decisions to optimize revenue and growth.
