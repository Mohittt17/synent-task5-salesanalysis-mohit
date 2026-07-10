# 🛒 Superstore Sales Data Analysis
### End-to-End Retail Business Intelligence | Synent Technologies Internship

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat-square&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.1.4-green?style=flat-square&logo=pandas)
![Seaborn](https://img.shields.io/badge/Seaborn-0.13-orange?style=flat-square)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.8-red?style=flat-square)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Ready-yellow?style=flat-square&logo=googlecolab)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square)
![Internship](https://img.shields.io/badge/Synent-Data%20Science%20Internship-blueviolet?style=flat-square)

</div>

---

## 📌 Project Overview

This project delivers a **production-quality Exploratory Data Analysis (EDA)** on the classic Sample Superstore retail dataset. The analysis was built as part of the **Synent Technologies Data Science Internship Program** and simulates the kind of BI work performed at Amazon, Walmart, and Microsoft retail analytics teams.

The project covers **the complete data science workflow** — from raw data ingestion through statistical analysis, 20+ professional visualizations, automated business insight generation, and C-suite-ready strategic recommendations.

---

## 🎯 Business Objectives

| # | Objective |
|---|-----------|
| 1 | Identify **revenue and profit trends** across 4 years |
| 2 | Determine **best and worst performing** product categories & sub-categories |
| 3 | Analyze **regional and state-level** performance disparities |
| 4 | Quantify the **impact of discounts** on profitability |
| 5 | Profile **high-value customers** and underperforming segments |
| 6 | Evaluate **shipping mode efficiency** and its effect on margins |
| 7 | Deliver **5 strategic, data-backed recommendations** for leadership |

---

## 📂 Dataset

| Property | Value |
|----------|-------|
| **Source** | Sample - Superstore.xls.zip |
| **Rows** | 9,994 |
| **Columns** | 21 (+ 10 engineered features) |
| **Time Period** | January 2014 – December 2017 |
| **Domain** | US Retail / E-commerce |
| **Key Fields** | Sales, Profit, Discount, Category, Region, Segment, Ship Mode |

**To use this notebook:**
1. Upload `Sample - Superstore.xls.zip` to Google Colab
2. Run all cells in order — the notebook auto-extracts and loads the data

---

## 🛠️ Technologies Used

| Tool | Purpose |
|------|---------|
| **Python 3.10** | Core programming language |
| **Pandas** | Data manipulation & aggregation |
| **NumPy** | Numerical computation |
| **Matplotlib** | Base plotting layer |
| **Seaborn** | Statistical visualization |
| **SciPy** | Statistical tests (Pearson, Shapiro-Wilk) |
| **Google Colab** | Cloud notebook execution |

---

## 🗂️ Project Workflow

```
📦 superstore-sales-analysis/
│
├── 📓 Superstore_Sales_Analysis.ipynb   ← Main analysis notebook
├── 📄 README.md                         ← Project documentation (this file)
├── 📋 requirements.txt                  ← Python dependencies
├── 📊 Project_Report.md                 ← Full business report
├── 💼 LinkedIn_Post.md                  ← LinkedIn announcement post
├── 🎤 Demo_Script.md                    ← 2-minute demo presentation
├── 🗂️ GitHub_Folder_Structure.md       ← Suggested repo layout
│
└── 📁 data/
    └── Sample - Superstore.xls.zip     ← Dataset (upload to Colab)
```

---

## 📊 Analysis Sections

The notebook is structured as a professional Data Science workflow:

| # | Section | Description |
|---|---------|-------------|
| 1 | **Project Header** | Title, author, program, objectives |
| 2 | **Dataset Description** | Features, business questions, importance |
| 3 | **Import Libraries** | All dependencies with version logging |
| 4 | **Load Dataset** | Auto-extract ZIP, load Excel, display samples |
| 5 | **Data Cleaning** | Rename, type-convert, info/describe |
| 6 | **Missing Value Analysis** | Heatmap + tabular report |
| 7 | **Duplicate Analysis** | Detection and removal |
| 8 | **Feature Engineering** | 10 derived features including profit margin, ship days |
| 9 | **EDA — 16 Visualizations** | Full visual analysis (see below) |
| 10 | **Statistical Analysis** | Pearson, Shapiro-Wilk, skewness, kurtosis |
| 11 | **Business Insights** | Automated KPI extraction |
| 12 | **Recommendations** | 5 strategic, prioritized recommendations |
| 13 | **Conclusion** | Summary and projected impact |
| 14 | **Future Improvements** | 8 ML/BI extensions |

---

## 📈 Visualizations Generated

| # | Chart | Key Finding |
|---|-------|-------------|
| 1 | Monthly Revenue Trend | Q4 consistently peaks; clear YoY growth |
| 2 | Monthly Profit Trend | High variance despite growing revenue |
| 3 | Monthly Order Volume | Volume mirrors revenue trend |
| 4 | Sales Distribution | Right-skewed; Pareto principle applies |
| 5 | Profit Distribution | Significant loss tail at negative profit |
| 6 | Category Analysis | Technology = highest profit despite lower volume |
| 7 | Sub-Category Analysis | Tables & Bookcases = consistent loss-makers |
| 8 | Top 10 Products | Copiers dominate profitability |
| 9 | Worst 10 Products | Specific SKUs generate massive losses |
| 10 | Region Analysis | West leads; Central underperforms |
| 11 | State Analysis | Texas, Ohio = high sales, negative profit |
| 12 | Segment Analysis | Home Office = best margin; Consumer = highest volume |
| 13 | Shipping Mode Analysis | Standard Class = dominant; Same Day = costly |
| 14 | Discount vs Profit | > 20% discount → negative margin confirmed |
| 15 | Sales vs Profit Scatter | Furniture has worst S:P ratio |
| 16 | Top 15 Customers | Power law distribution confirmed |
| 17 | Top 15 Cities | NYC, LA, Seattle dominate |
| 18 | Correlation Heatmap | Discount:Profit strong negative confirmed |
| 19 | Pairplot | Multi-dimensional category separation |
| 20 | KPI Dashboard | 9-panel executive summary |

---

## 🔑 Key Business Results

```
💰 Total Revenue    : $2,297,201
📈 Total Profit     : $286,397
📊 Profit Margin    : ~12.5%
🛒 Total Orders     : 5,009
👥 Unique Customers : 793
🎯 Avg Order Value  : ~$458
🏷️ Avg Discount     : ~15.6%
✅ Profitable Orders: ~61%
```

---

## 💡 Top 5 Business Findings

1. **Technology** is the profit engine — highest margins, fastest growth
2. **Discounts above 20%** systematically destroy profitability
3. **Central Region** is structurally underperforming despite healthy order volume
4. **Tables & Bookcases** are chronically loss-generating sub-categories
5. **Q4 (Oct–Dec)** is the business's make-or-break quarter

---

## 🎯 Strategic Recommendations

| Priority | Action | Projected Impact |
|----------|--------|-----------------|
| 🔴 P1 | Implement 20% hard discount cap | +3–5% margin improvement |
| 🟠 P2 | Discontinue loss-making SKUs | Reduce losses by $50K+ annually |
| 🟡 P3 | Fix Central Region operations | +$30K regional profit recovery |
| 🟢 P4 | Launch VIP customer program | +15–20% retention rate |
| 🔵 P5 | Seasonal inventory planning | Prevent Q1 revenue dips |

---

## ⚙️ Installation

```bash
# Clone the repository
# ⚠️  Replace YOUR_USERNAME with your actual GitHub username before submitting
git clone https://github.com/YOUR_USERNAME/superstore-sales-analysis.git
cd superstore-sales-analysis

# Create virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch notebook
jupyter notebook Superstore_Sales_Analysis.ipynb
```

**Or run on Google Colab (recommended):**
1. Upload `Superstore_Sales_Analysis.ipynb` to [colab.research.google.com](https://colab.research.google.com)
2. Upload `Sample - Superstore.xls.zip` when prompted
3. Run All Cells → Runtime → Run All

---

## 📁 Folder Structure

```
superstore-sales-analysis/
├── Superstore_Sales_Analysis.ipynb
├── README.md
├── requirements.txt
├── Project_Report.md
├── LinkedIn_Post.md
├── Demo_Script.md
├── GitHub_Folder_Structure.md
└── data/
    └── Sample - Superstore.xls.zip
```

---

## ⚠️ Known Limitations

- This analysis is **descriptive and exploratory**. Findings such as "discounts cause losses" describe a correlation, not a proven causal relationship. Controlled experiments (A/B tests) should be conducted before implementing policy changes.
- The dataset covers **2014–2017** only. Trends may not reflect current market conditions.
- Geographic analysis is at state/city level — store-level or zip-code-level data would enable more granular operational recommendations.
- Customer lifetime value is estimated from 4 years of history; a longer time window would improve RFM scoring accuracy.

---

## 🔮 Future Scope

- [ ] Time-series forecasting with Prophet / ARIMA
- [ ] Customer churn prediction (XGBoost / Random Forest)
- [ ] RFM customer segmentation (K-Means clustering)
- [ ] Interactive dashboard (Plotly Dash / Tableau)
- [ ] Geospatial profit map (Folium)
- [ ] Price elasticity analysis
- [ ] A/B test framework for discount policy testing

---

## 👤 Author

**Mohit**  
*Data Science Intern — Synent Technologies*  
📅 July 2026  
🔗 [GitHub](https://github.com/YOUR_USERNAME) · [LinkedIn](https://linkedin.com/in/YOUR_PROFILE)  

> ⚠️ Replace the GitHub and LinkedIn URLs above with your actual profile links before submission.

---

*Built with ❤️ using Python · Pandas · Seaborn · Matplotlib · SciPy*
#   s y n e n t - t a s k 5 - s a l e s a n a l y s i s - m o h i t  
 