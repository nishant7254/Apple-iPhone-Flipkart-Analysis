# 🍎 Apple Products Performance Analytics Dashboard

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-5.x-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)

**End-to-end data analytics project analyzing Apple iPhone pricing, ratings, and discounting patterns on Flipkart India — from raw data to executive-level Power BI dashboard.**

[📊 View Dashboard](#dashboard-preview) • [📁 Dataset](#dataset-information) • [💡 Key Insights](#key-insights) • [🚀 Getting Started](#installation-guide)

</div>

---

## 📋 Table of Contents

1. [Project Overview](#project-overview)
2. [Business Problem & Objectives](#business-problem--objectives)
3. [Dataset Information](#dataset-information)
4. [Data Dictionary](#data-dictionary)
5. [Project Architecture](#project-architecture)
6. [Dashboard Preview](#dashboard-preview)
7. [Exploratory Data Analysis](#exploratory-data-analysis)
8. [Key Insights](#key-insights)
9. [Business Recommendations](#business-recommendations)
10. [Technologies Used](#technologies-used)
11. [Installation Guide](#installation-guide)
12. [Project Results](#project-results)
13. [Future Scope](#future-scope)
14. [Author](#author)

---

## 📌 Project Overview

This project delivers a **comprehensive business intelligence solution** for analyzing Apple iPhone product listings on Flipkart India. Using real e-commerce data covering 62 product SKUs, the analysis uncovers pricing strategies, customer sentiment trends, and discount distribution patterns to support data-driven retail and marketing decisions.

The project spans the complete data analytics lifecycle — from raw data ingestion and cleaning through exploratory analysis, feature engineering, and culminating in an interactive Power BI dashboard that communicates executive-ready insights.

> **Domain:** E-Commerce | Retail Analytics | Consumer Electronics  
> **Market:** India (Flipkart Platform)  
> **Company Focus:** Apple Inc. — iPhone Product Line

---

## 🎯 Business Problem & Objectives

### Business Problem
Apple operates in a highly competitive premium smartphone segment in India. Retailers and category managers on Flipkart need to understand:
- How pricing correlates with customer satisfaction and review volume
- Whether discount strategies drive engagement or erode brand value
- Which product configurations command the highest ratings and reviews
- How RAM segmentation affects pricing tiers

### Project Objectives
- ✅ Analyze pricing distribution across Apple iPhone SKUs on Flipkart
- ✅ Identify correlations between price, discount, ratings, and reviews
- ✅ Determine which products generate the highest customer engagement
- ✅ Provide actionable recommendations for pricing and discount strategy
- ✅ Deliver an executive-facing Power BI dashboard for stakeholder reporting

### Expected Business Value
- Optimize discount strategy to maximize review volume without sacrificing margin
- Identify high-engagement SKUs for promotional prioritization
- Support category management decisions with data-backed evidence
- Enable benchmarking of Apple product performance vs. platform averages

---

## 📊 Dataset Information

| Attribute | Details |
|-----------|---------|
| **Source** | Flipkart India (Web-scraped) |
| **Total Records** | 62 Apple iPhone SKUs |
| **Total Features** | 11 columns |
| **Time Period** | Static snapshot |
| **Missing Values** | None (100% complete) |
| **Duplicates** | 0 |
| **File Format** | CSV |
| **File Size** | ~15 KB |

---

## 📖 Data Dictionary

| Column | Data Type | Description | Example |
|--------|-----------|-------------|---------|
| `Product Name` | String | Full product listing name including color and storage | APPLE iPhone 8 Plus (Gold, 64 GB) |
| `Product URL` | String | Direct Flipkart listing URL | https://www.flipkart.com/... |
| `Brand` | String | Product brand (all Apple in this dataset) | Apple |
| `Sale Price` | Integer (₹) | Current selling price on Flipkart | 49,900 |
| `Mrp` | Integer (₹) | Maximum Retail Price (original listed price) | 54,900 |
| `Discount Percentage` | Integer (%) | Percentage discount applied (MRP → Sale Price) | 10 |
| `Number Of Ratings` | Integer | Total count of customer star ratings | 3,431 |
| `Number Of Reviews` | Integer | Total count of written customer reviews | 356 |
| `Upc` | String | Unique product code / SKU identifier | MOBEXRGV7EHHTGUH |
| `Star Rating` | Float | Aggregate star rating (4.5 – 4.7 scale) | 4.6 |
| `Ram` | String | Device RAM specification | 4 GB |

---

## 🏗️ Project Architecture

```
┌─────────────────────────────────────────────────────────────────────┐
│                     PROJECT WORKFLOW                                │
└─────────────────────────────────────────────────────────────────────┘

  📥 Raw Data          🧹 Data Cleaning       🔍 EDA
  ─────────────        ───────────────        ──────────────────
  Flipkart CSV    →    Null check        →    Descriptive stats
  62 SKUs              Duplicate check        Distribution plots
  11 features          Outlier review         Correlation matrix
                       Type validation        Scatter analysis

         ↓
  ⚙️ Feature Engineering    📊 Power BI Modeling     📈 Dashboard
  ─────────────────────     ───────────────────      ─────────────
  Savings Amount       →    Data import         →    KPI cards
  Price Tiers               Relationships            Bar charts
  Rating Bands              DAX measures             Scatter plots
  Review Ratio              Calculated columns       Heatmaps
                                                     Histograms

         ↓
  💡 Business Insights  →  📋 Executive Report  →  🎯 Decisions
```

---

## 📸 Dashboard Preview

> **Power BI Dashboard — Apple Products Performance Dashboard**

The dashboard includes the following panels:

| Panel | Visual Type | Business Purpose |
|-------|-------------|-----------------|
| KPI Cards (×4) | Metric tiles | Top-line summary: Products, Avg Price, Avg Rating, Avg Discount |
| Avg Sale Price by RAM | Bar chart | Price segmentation by RAM tier |
| Sale Price vs Rating | Scatter plot | Pricing-quality relationship |
| Top Products by Reviews | Horizontal bar | Customer engagement ranking |
| Discount Distribution | Histogram | Discount strategy spread |
| MRP vs Sale Price | Scatter plot | Pricing integrity & discount depth |
| Correlation Matrix | Heatmap | Feature interdependency |

---

## 🔍 Exploratory Data Analysis

### Descriptive Statistics Summary

| Metric | Sale Price (₹) | MRP (₹) | Discount % | Star Rating | # Ratings | # Reviews |
|--------|---------------|---------|-----------|-------------|-----------|-----------|
| **Mean** | 80,074 | 88,058 | 9.95% | 4.58 | 22,420 | 1,862 |
| **Median** | 75,900 | 79,900 | 10% | 4.60 | 2,101 | 180 |
| **Std Dev** | 34,310 | 34,729 | 7.61% | 0.059 | 33,769 | 2,856 |
| **Min** | 29,999 | 39,900 | 0% | 4.50 | 542 | 42 |
| **Max** | 1,40,900 | 1,49,900 | 29% | 4.70 | 95,909 | 8,161 |

### RAM Distribution
| RAM | SKU Count | % of Catalog |
|-----|-----------|-------------|
| 4 GB | 29 | 46.8% |
| 6 GB | 19 | 30.6% |
| 2 GB | 13 | 21.0% |
| 3 GB | 1 | 1.6% |

### Star Rating Distribution
| Rating | Count | % of SKUs |
|--------|-------|-----------|
| 4.6 | 37 | 59.7% |
| 4.5 | 20 | 32.3% |
| 4.7 | 5 | 8.1% |

---

## 💡 Key Insights

1. **🏆 Consistently High Brand Ratings** — All 62 SKUs fall within a narrow 4.5–4.7 star range, demonstrating Apple's exceptional brand consistency and customer satisfaction on Flipkart.

2. **💰 Wide Price Spectrum** — Products range from ₹29,999 to ₹1,40,900, a 4.7× spread, indicating Apple serves multiple market segments from accessible to ultra-premium.

3. **📉 Negative Price-Ratings Correlation** — Lower-priced models (iPhone SE, XR) accumulate significantly more ratings, confirming that accessible pricing drives higher customer engagement volume.

4. **🔖 Moderate Discount Strategy** — The average discount is 9.95% with a maximum of 29%. Apple maintains premium brand positioning by keeping discounts restrained — avoiding deep discounting that could erode perceived value.

5. **⭐ iPhone SE Dominates Reviews** — iPhone SE variants hold all top-5 positions by review count, making the SE the highest-engagement product in the catalog.

6. **📦 4GB RAM is the Catalog Sweet Spot** — With 46.8% of SKUs, 4GB configurations dominate the lineup, aligning with Apple's mainstream product positioning.

7. **🔗 Strong MRP–Sale Price Correlation** — The near-linear relationship between MRP and sale price confirms consistent, predictable discounting across the catalog.

8. **📊 Bimodal Discount Distribution** — Two discount clusters emerge: 0–5% (minimal discount) and 8–12% (moderate discount), suggesting deliberate discount tiering by product generation.

9. **🌟 Premium Tier (6GB) Commands Top Prices** — 6GB RAM devices average over ₹1,00,000, clearly defining the Pro/Max tier premium segment.

10. **📈 Low Review-to-Rating Ratio** — Across the catalog, only ~8% of customers who rate a product also write a review, highlighting an opportunity to improve written review conversion.

11. **🎯 Zero-Discount SKUs Exist** — Several products carry 0% discount, confirming that newly launched or supply-constrained models are sold at full MRP.

12. **🔄 Color/Storage Drive SKU Proliferation** — The 62 SKUs represent far fewer base models, with most variation driven by color and storage configuration — a key catalog management insight.

---

## 📋 Business Recommendations

| Priority | Recommendation | Expected Impact |
|----------|---------------|-----------------|
| **HIGH** | Focus promotional campaigns on mid-range SKUs (₹40K–₹80K) to maximize rating volume | +15–25% engagement |
| **HIGH** | Apply 10–15% discount window specifically during sales events for premium SKUs | Improved sell-through rate |
| **MEDIUM** | Implement post-purchase review request campaigns to close the rating-to-review gap | +Review volume conversion |
| **MEDIUM** | Use iPhone SE as a gateway product in first-time buyer campaigns | Broader customer acquisition |
| **LOW** | Sunset 3GB RAM SKU (only 1 listing) — consolidate catalog to 2GB/4GB/6GB tiers | Simplified catalog management |
| **LOW** | Monitor 4.7-star products for featured placement opportunities | Enhanced conversion |

---

## 🛠️ Technologies Used

| Category | Technology | Version | Purpose |
|----------|-----------|---------|---------|
| **Language** | Python | 3.10+ | Core analysis scripting |
| **Data Manipulation** | Pandas | 2.x | DataFrame operations, cleaning |
| **Numerical Computing** | NumPy | 1.24+ | Mathematical operations |
| **Visualization (EDA)** | Plotly Express | 5.x | Interactive EDA charts |
| **Visualization (BI)** | Plotly Graph Objects | 5.x | Custom chart components |
| **Business Intelligence** | Microsoft Power BI | Desktop | Executive dashboard |
| **Development Environment** | Jupyter Notebook | 7.x | Exploratory analysis |
| **Statistical Analysis** | SciPy | 1.10+ | Correlation, regression |
| **Version Control** | Git / GitHub | Latest | Source control |

---

## 🚀 Installation Guide

### Prerequisites
- Python 3.10 or higher
- pip package manager
- Microsoft Power BI Desktop (for dashboard)
- Jupyter Notebook / JupyterLab

### Step 1: Clone the Repository
```bash
git clone https://github.com/yourusername/apple-products-analytics.git
cd apple-products-analytics
```

### Step 2: Create Virtual Environment
```bash
python -m venv venv

# Windows
venv\Scripts\activate

# macOS / Linux
source venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Launch Jupyter Notebook
```bash
jupyter notebook iphone.ipynb
```

### Step 5: Open Power BI Dashboard
- Open `Apple_Products_Dashboard.pbix` in Microsoft Power BI Desktop
- Refresh the data connection if prompted, pointing to `apple_products.csv`

---

## 📈 Project Results

| Metric | Value |
|--------|-------|
| Total SKUs Analyzed | 62 |
| Data Completeness | 100% (zero nulls) |
| Average Sale Price | ₹80,074 |
| Average Star Rating | 4.58 / 5.0 |
| Average Discount | 9.95% |
| Price Range | ₹29,999 – ₹1,40,900 |
| Top Reviewed Product | Apple iPhone SE (8,161 reviews) |
| Highest Rated Products | 5 SKUs at 4.7 stars |
| Dashboard Visuals Created | 7 interactive visuals |
| Actionable Insights Delivered | 12+ |

---

## 🔮 Future Scope

- [ ] **Competitor Benchmarking** — Extend dataset to include Samsung, OnePlus, and other flagship brands for comparative analysis
- [ ] **Time-Series Tracking** — Scrape data monthly to track price fluctuations and discount seasonality
- [ ] **Sentiment Analysis** — Apply NLP on written reviews to extract feature-level satisfaction themes
- [ ] **Predictive Pricing Model** — Build ML regression model to predict optimal sale price for new SKUs
- [ ] **Category Expansion** — Include Apple MacBook, iPad, and AirPods data for full ecosystem analysis
- [ ] **Real-Time Dashboard** — Connect Power BI to a live Flipkart API feed for real-time monitoring
- [ ] **Geospatial Analysis** — If regional sales data becomes available, map performance by Indian state

---

## 👤 Author

Nishant Ranjan 
Data Analyst | BI Developer | Python Enthusiast

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/nishant015/)
[![Instagram](https://img.shields.io/badge/Instagram-Follow-E4405F?style=flat-square&logo=instagram&logoColor=white)](https://www.instagram.com/inishantindia/?hl=en)
[![Email](https://img.shields.io/badge/Email-Contact-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:nishant845423@gmail.com)
---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

<div align="center">

⭐ **If you found this project useful, please give it a star!** ⭐

*Built with ❤️ using Python, Plotly, and Power BI*

</div>
