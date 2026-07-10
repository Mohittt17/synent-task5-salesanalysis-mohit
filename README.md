# Superstore Sales Data Analysis

A data analysis project built as part of the **Synent Technologies Data Science Internship (Task 5)**.
The project performs an end-to-end Exploratory Data Analysis (EDA) on the Sample Superstore retail dataset,
covering sales trends, profitability drivers, regional performance, discount impact, and customer behavior
across four years of US retail transaction data.

![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat-square&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.1.4-blue?style=flat-square&logo=pandas)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Ready-orange?style=flat-square&logo=googlecolab)

---

## Project Overview

This project analyzes the Sample Superstore dataset — a widely used retail dataset containing four years of
order-level transaction records from a fictional US-based retail chain.

The goal was to move beyond surface-level summary statistics and identify **why** the business is generating
growing revenue but a relatively flat profit margin. The analysis answers the following business questions:

- Which product categories and sub-categories are profitable, and which are loss-making?
- How do discounts affect profitability, and where is the break-even point?
- Which regions and states are underperforming relative to their order volume?
- Which customer segments offer the best margin, and which are underserved?
- What seasonal patterns exist, and how should they inform planning?

---

## Objectives

- Analyze 4-year revenue and profit trends at monthly, quarterly, and annual granularity
- Identify the best and worst performing product categories and sub-categories
- Measure the correlation between discount levels and profitability
- Evaluate regional and state-level performance disparities
- Profile customer segments by revenue, margin, and order behavior
- Assess shipping mode usage and its relationship with profit
- Deliver clear, data-backed business recommendations

---

## Dataset

| Property        | Value                                         |
|-----------------|-----------------------------------------------|
| **Name**        | Sample Superstore                             |
| **File**        | `Sample - Superstore.xls.zip`                 |
| **Rows**        | 9,994 orders                                  |
| **Columns**     | 21 original + 10 engineered features          |
| **Time Period** | January 2014 – December 2017                  |
| **Geography**   | United States (49 states, 531 cities)         |
| **Customers**   | 793 unique customers                          |
| **Key Fields**  | Sales, Profit, Discount, Category, Sub-Category, Region, Segment, Ship Mode |

**Source:** [Sample Superstore Dataset — Kaggle](https://www.kaggle.com/datasets/yesshivam007/superstore-dataset?resource=download) — a standard dataset widely used in data science education.

> **Note:** The dataset file is not included in this repository. Download it separately and upload it to
> Google Colab when running the notebook. The notebook handles extraction and loading automatically.

---

## Technologies Used

| Tool              | Version  | Purpose                              |
|-------------------|----------|--------------------------------------|
| Python            | 3.10     | Core programming language            |
| Pandas            | 2.1.4    | Data manipulation and aggregation    |
| NumPy             | 1.26.2   | Numerical computation                |
| Matplotlib        | 3.8.2    | Base plotting                        |
| Seaborn           | 0.13.0   | Statistical visualization            |
| SciPy             | 1.11.4   | Statistical tests (Pearson, Shapiro-Wilk) |
| openpyxl / xlrd   | —        | Excel file handling                  |
| Google Colab      | —        | Cloud notebook execution             |
| GitHub            | —        | Version control and project hosting  |

---

## Project Workflow

### 1. Data Loading
The notebook auto-extracts the ZIP archive and loads the `.xls` file using `xlrd`. Basic shape, column
types, and sample rows are displayed to confirm a successful load.

### 2. Data Cleaning
Column names are standardized (lowercase, underscores). Date columns are parsed. Data types are verified
and corrected. Missing value and duplicate analyses are run — the dataset is clean with 0 nulls and
0 duplicates.

### 3. Feature Engineering
Ten new features are derived to enable richer analysis:

| Feature          | Description                            |
|------------------|----------------------------------------|
| `order_year`     | Calendar year of the order             |
| `order_month`    | Month number (1–12)                    |
| `month_name`     | Full month string                      |
| `quarter`        | Q1 through Q4                         |
| `year_month`     | Period string (YYYY-MM)                |
| `ship_days`      | Days from order date to ship date      |
| `profit_margin`  | `profit / sales × 100`                 |
| `revenue_per_unit`| `sales / quantity`                    |
| `discount_bucket`| Binned discount tiers                  |
| `is_profitable`  | Boolean flag: `profit > 0`             |

### 4. Exploratory Data Analysis
Twenty visualizations covering trends, distributions, category breakdowns, regional maps, and
correlation analysis (see EDA section below).

### 5. Statistical Analysis
Shapiro-Wilk normality tests on Sales, Profit, and Discount. Pearson correlation matrix for
key numeric variables.

### 6. Business Insights
Automated KPI extraction: total revenue, total profit, overall margin, average order value,
average discount rate, and percentage of profitable orders.

### 7. Recommendations
Five prioritized, data-backed recommendations with specific actions for the business.

---

## Exploratory Data Analysis

The notebook generates 20 visualizations organized into the following analysis areas:

**Sales & Profit Trends**
- Monthly revenue trend (2014–2017) — shows Q4 seasonal peaks and year-over-year growth
- Monthly profit trend — highlights variance despite growing revenue
- Monthly order volume — mirrors the revenue pattern

**Distributions**
- Sales distribution — right-skewed; a small number of orders drive a large share of revenue
- Profit distribution — bimodal with a meaningful negative tail (loss-making orders)

**Category & Sub-Category Analysis**
- Revenue, profit, and margin by category (Technology, Furniture, Office Supplies)
- Sub-category ranking — identifies top performers (Copiers, Phones) and consistent loss-makers (Tables, Bookcases)
- Top 10 and bottom 10 products by profit

**Geographic Analysis**
- Revenue and profit by region (West, East, Central, South)
- State-level profit heatmap — highlights states with high orders but negative profit

**Segment & Customer Analysis**
- Revenue, margin, and order count by customer segment (Consumer, Corporate, Home Office)
- Top 15 customers by revenue
- Top 15 cities by revenue

**Discount & Shipping Analysis**
- Discount vs. profit scatter plot — visualizes the break-even discount threshold
- Sales vs. profit scatter by category — shows Furniture's poor revenue-to-profit ratio
- Shipping mode analysis — volume and margin by ship mode

**Correlation & Statistical Analysis**
- Pearson correlation heatmap for numeric variables
- Pairplot with category-level color separation
- 9-panel KPI summary dashboard

---

## Key Findings

**Overall Performance**

| KPI                  | Value       |
|----------------------|-------------|
| Total Revenue        | $2,297,201  |
| Total Profit         | $286,397    |
| Overall Profit Margin| ~12.5%      |
| Total Orders         | 5,009       |
| Unique Customers     | 793         |
| Average Order Value  | ~$458       |
| Average Discount     | ~15.6%      |
| Profitable Orders    | ~61%        |

**Annual Trend**

| Year | Revenue | Profit | Margin |
|------|---------|--------|--------|
| 2014 | ~$484K  | ~$49K  | 10.1%  |
| 2015 | ~$470K  | ~$61K  | 13.0%  |
| 2016 | ~$609K  | ~$81K  | 13.3%  |
| 2017 | ~$733K  | ~$93K  | 12.7%  |

Revenue grew 51% from 2014 to 2017, but profit margin remained roughly flat — indicating that
cost and discount pressures are absorbing the top-line growth.

**Category Performance**
- Technology generates the highest profit ($145K, ~17.4% margin) despite having fewer orders than
  the other categories
- Furniture produces near-Technology revenue (~$742K) but only ~2.5% profit margin
- Office Supplies is volume-driven with strong absolute profit ($122K) at thin per-unit margins

**Sub-Category Losses**
Tables (−$17,725), Bookcases (−$3,473), and Supplies (−$1,189) generated losses across all four years.
Tables is the single most loss-making sub-category.

**Discount Impact**

| Discount Range | Avg Profit per Order |
|----------------|----------------------|
| 0%             | +$28.50              |
| 0–10%          | +$22.10              |
| 10–20%         | +$7.80               |
| 20–30%         | −$9.30               |
| 30–50%         | −$21.60              |
| > 50%          | −$45.80              |

The break-even discount threshold is approximately 18–20%. Orders with discounts above this
level generate a net loss on average. Pearson correlation between Discount and Profit: **−0.22**.

**Regional Performance**

| Region  | Revenue | Profit | Margin |
|---------|---------|--------|--------|
| West    | ~$725K  | ~$108K | 14.9%  |
| East    | ~$678K  | ~$91K  | 13.4%  |
| Central | ~$501K  | ~$39K  | 7.8%   |
| South   | ~$392K  | ~$46K  | 11.7%  |

Central Region has the lowest margin (7.8%) despite a healthy order volume. Texas (−$25,729),
Ohio (−$16,971), and Pennsylvania (−$15,020) are the three states generating the largest losses.

**Customer Segments**
- Home Office has the highest margin (14.0%) and the fewest customers (147) — underserved relative
  to its profitability
- Consumer drives the highest revenue volume (~$1.16M) at an 11.5% margin

**Seasonality**
- Q4 (October–December) is the strongest quarter in all four years, with December typically 20–25%
  above the monthly average
- Q1 (January–March) sees consistent demand contraction; February is typically the weakest month

---

## Business Recommendations

**1. Enforce a discount cap at 20%**
The analysis shows a clear break-even around the 18–20% discount level. Orders above this threshold
are consistently loss-making. Implementing a policy cap — with manager approval required for exceptions —
is the most direct lever available to improve overall margins.

**2. Review loss-making sub-categories**
Tables and Bookcases have generated losses in every year of the dataset. The business should review
supplier pricing, freight costs, and return rates for these lines. If the unit economics cannot be
fixed, discontinuation should be considered.

**3. Investigate Central Region operations**
Central Region's 7.8% margin is roughly half the West's 14.9%, despite comparable operational scale.
A root-cause analysis of discount practices, fulfillment costs, and product mix in this region is warranted.

**4. Invest more attention in the Home Office segment**
Home Office customers show the highest margin among the three segments but represent the smallest
customer count. This segment appears underserved and may respond well to targeted outreach or
account management.

**5. Plan inventory and capacity around Q4 seasonality**
Q4 consistently drives the largest share of annual revenue. Inventory build-up, staffing adjustments,
and logistics capacity planning should begin in Q3 to avoid supply-side constraints during peak demand.

---

## Repository Structure

```
synent-task5-salesanalysis-mohit/
│
├── Superstore_Sales_Analysis.ipynb   # Main analysis notebook
├── README.md                         # Project documentation
├── requirements.txt                  # Python dependencies
├── Project_Report.md                 # Full written report with findings and recommendations
├── Demo_Script.md                    # 2-minute demo presentation notes
├── LinkedIn_Post.md                  # LinkedIn post draft
├── GitHub_Folder_Structure.md        # Repository layout reference
│
└── data/
    └── README.md                     # Instructions for obtaining the dataset
```

> The dataset (`Sample - Superstore.xls.zip`) is not committed to this repository.
> See the Dataset section above for the source link.

---

## How to Run

### Option 1 — Google Colab (Recommended)

1. Go to [colab.research.google.com](https://colab.research.google.com)
2. Upload `Superstore_Sales_Analysis.ipynb`
3. When the notebook prompts for the dataset, upload `Sample - Superstore.xls.zip`
4. Go to **Runtime → Run All**

The notebook handles ZIP extraction and file loading automatically. No manual path configuration is needed.

### Option 2 — Local Jupyter

```bash
# Clone the repository
git clone https://github.com/Mohittt17/synent-task5-salesanalysis-mohit.git
cd synent-task5-salesanalysis-mohit

# Create and activate a virtual environment
python -m venv venv
venv\Scripts\activate        # Windows
# source venv/bin/activate   # macOS / Linux

# Install dependencies
pip install -r requirements.txt

# Launch the notebook
jupyter notebook Superstore_Sales_Analysis.ipynb
```

Place `Sample - Superstore.xls.zip` in the `data/` folder before running, or update the file path
in the `extract_and_load()` function to match your local path.

---

## Known Limitations

- The dataset covers **2014–2017** only. Patterns observed may not reflect current market conditions.
- The analysis is **descriptive and correlational**. The discount-profit relationship describes a
  correlation, not a proven causal effect. Controlled A/B testing would be needed before making
  policy changes.
- Geographic analysis is at the state and city level. Store-level or zip-code-level data would
  allow more granular operational conclusions.
- Customer lifetime value estimates are based on four years of history. A longer observation window
  would improve segment-level reliability.

---

## Future Improvements

- [ ] Sales forecasting using ARIMA or Facebook Prophet
- [ ] Customer segmentation using RFM analysis and K-Means clustering
- [ ] Churn prediction model (Logistic Regression / XGBoost)
- [ ] Interactive dashboard using Plotly Dash or Streamlit
- [ ] Geospatial profit visualization using Folium
- [ ] Price elasticity analysis to model optimal discount levels
- [ ] A/B test framework to validate discount policy changes

---

## Author

**Mohit**  
Data Science Intern — Synent Technologies  
July 2026

- GitHub: [github.com/Mohittt17/synent-task5-salesanalysis-mohit](https://github.com/Mohittt17/synent-task5-salesanalysis-mohit)
- LinkedIn: [View LinkedIn Post](https://www.linkedin.com/feed/update/urn:li:activity:7481413946391056384/)

---

*Superstore Sales Data Analysis — Synent Technologies Data Science Internship, Task 5*