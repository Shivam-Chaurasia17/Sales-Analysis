# 📈 Regional Sales Performance Analysis — End-to-End EDA Project

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0?style=for-the-badge&logo=python&logoColor=white)
![PowerBI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/Status-Complete-2ECC71?style=for-the-badge)

> **A recruiter-ready regional sales analytics project** — cleaning, merging, and analyzing multi-year sales data to uncover revenue drivers, profitability trends, and regional performance gaps, backed by an interactive Power BI dashboard.

---

## 🎯 Project Overview

This project delivers an **end-to-end sales analytics pipeline** for a multi-region distribution business. It combines data wrangling across multiple source tables, exploratory data analysis, profitability metric engineering, and business-ready visual reporting — structured as a professional portfolio piece suitable for Data Analyst, Business Analyst, and BI Analyst roles.

### Business Problem
Sales, cost, and budget data were spread across **6 disconnected Excel sheets** (orders, customers, products, regions, state mapping, budgets), making it difficult to answer core business questions:
- Which products, customers, and regions actually drive **profit**, not just revenue?
- Are sales channels and states performing in line with their **allocated budgets**?
- What seasonal and pricing patterns should guide **inventory and marketing** decisions?

### Key Findings at a Glance

| Insight | Detail |
|---|---|
| Revenue Concentration | A small subset of products & customers drives majority of revenue (Pareto pattern) |
| Top Channel | Wholesale contributes **54.1%** of total revenue |
| Profitability Driver | Higher cost does **not** guarantee higher profit margin — pricing strategy matters more |
| Seasonality | Clear month-over-month revenue cycles across years |
| Budget Alignment | Some states outperform their budget allocation; others underdeliver despite higher funding |
| Demographic Impact | Population, income, and household data show **weak correlation** with revenue |

---

## 📂 Project Structure

```
Regional-Sales-Performance-Analysis/
│
├── 📄 README.md                              # Project documentation
├── 📊 EDA_region_sales_analysis.ipynb         # Full data cleaning, feature engineering & EDA notebook
├── 📁 data/
│   └── Regional_Sales_Dataset.xlsx            # Original multi-sheet dataset
│
├── 📁 outputs/
│   ├── file.csv                                # Merged raw dataset (pre-cleaning)
│   └── Sales_data_EDA_Exported_.csv            # Final cleaned & feature-engineered dataset
│
└── 📁 dashboard/
    └── SALES_REPORT.pbix                       # Interactive Power BI dashboard
```

---

## 🔬 Methodology

### Phase 1 — Data Understanding
- Source: 6 Excel sheets — Sales Orders, Customers, Products, Regions, State Regions, 2017 Budgets
- Target metrics: Revenue, Cost, Profit, Profit Margin %

### Phase 2 — Data Cleaning & Wrangling
- Merged Sales Orders with Customers, Products, Regions, State Regions, and Budgets into a single unified dataframe
- Fixed misaligned headers in the State Regions sheet
- Checked and handled missing values across all source tables
- Removed duplicate/redundant ID columns post-merge (`Customer Index`, `Index`, `id`, `State Code`)
- Standardized column names to lowercase, snake_case for consistency

### Phase 3 — Feature Engineering
Created new business metrics:
| Feature | Description |
|---|---|
| `total_cost` | order_quantity × unit cost — actual expenditure per transaction |
| `profit` | revenue − total_cost |
| `profit_margin_pct` | profit as a % of revenue, standardized across price ranges |
| `order_month`, `year`, `month` | time features for trend & seasonality analysis |

### Phase 4 — Exploratory Data Analysis
Analysis conducted across multiple dimensions:
- **Time Trends**: Monthly & yearly revenue patterns, seasonal peaks
- **Product Performance**: Top 10 products by revenue, pricing distribution
- **Channel Analysis**: Revenue share and profit margin distribution by channel
- **Customer Analysis**: Top 10 and bottom 10 customers by revenue
- **Regional Analysis**: State-wise order count vs. profit, budget vs. revenue comparison
- **Profitability Analysis**: Cost vs. profit margin density heatmap
- **Correlation Analysis**: Financial metrics vs. demographic variables (population, income, households)

### Phase 5 — Dashboard Reporting
Built an interactive **Power BI dashboard** to translate the cleaned dataset into stakeholder-ready visuals covering regional sales, profitability, and channel performance.

---

## 📈 Key Visualizations

The notebook generates **10+ visualizations** including:

1. **Monthly & Yearly Revenue Trends** — line charts across years
2. **Top 10 Products by Revenue** — bar chart
3. **Sales by Channel** — pie chart of revenue share
4. **Average Order Value Distribution** — histogram
5. **Cost vs. Profit Margin Heatmap** — order density by cost/margin bins
6. **State-wise Order Count vs. Profit** — dual-axis bar chart
7. **State-wise Budget vs. Revenue** — dual-axis bar chart
8. **Profit Margin by Channel** — boxplot distribution
9. **Unit Price Distribution by Product** — boxplot
10. **Top & Bottom 10 Customers by Revenue** — horizontal bar charts
11. **Correlation Heatmap** — financial & demographic metrics

---

## 🏗️ Technology Stack

| Category | Tools |
|---|---|
| **Language** | Python 3.10+ |
| **Data Processing** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn |
| **Dashboarding** | Power BI |
| **Environment** | Jupyter Notebook |

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn openpyxl
```

### Run the Analysis
```bash
jupyter notebook EDA_region_sales_analysis.ipynb
```

### Output
- Cleaned dataset: `outputs/Sales_data_EDA_Exported_.csv`
- Interactive dashboard: `dashboard/SALES_REPORT.pbix`

---

## 💡 Top Business Insights

### 1. Revenue Follows a Pareto Distribution
A small set of products and customers generates a disproportionately large share of total revenue — these should be prioritized in inventory planning and account management.

### 2. Cost Doesn't Predict Profitability
Products with higher unit cost don't necessarily deliver higher profit margins, indicating **pricing strategy** — not production cost — is the stronger lever for profitability.

### 3. Wholesale Dominates, but Isn't the Whole Story
Wholesale drives the majority of revenue (54.1%), but margin variability across channels shows other channels may offer more predictable, and in some cases more profitable, returns.

### 4. Budget Allocation Isn't Always Efficient
Some states convert their budget into revenue far more efficiently than others — a signal for reallocating funds toward higher-return regions.

### 5. Demographics Alone Don't Drive Sales
Population, income, and household counts show weak correlation with revenue, suggesting sales performance is driven more by product mix, pricing, and channel strategy than by regional demographics.

---

## 👤 Author

**Data Analytics Portfolio Project**
Built with professional-grade data analysis methodologies suitable for Data Analyst, Business Analyst, and BI Analyst roles.

---

## 📄 License

This project is for educational and portfolio purposes.
