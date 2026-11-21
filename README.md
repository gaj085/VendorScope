# 📊 VendorScope: Vendor & Brand Performance Analytics

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Power BI](https://img.shields.io/badge/Power_BI-Interactive_Dashboard-F2C811?logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![SQL](https://img.shields.io/badge/SQL-SQLite%20%2F%20Data%20Aggregation-CC292B?logo=sqlite&logoColor=white)](https://www.sqlite.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)

An end-to-end business intelligence and data analytics project that evaluates **vendor efficiency, brand profitability, and inventory performance** using **SQL, Python (Pandas/Seaborn), and Power BI**.

---

## 📌 Project Overview

In retail and distribution supply chains, vendor dependency and margin variability significantly dictate net profitability. This project analyzes transaction records to:
- Evaluate supplier contribution and identify revenue concentration risks.
- Benchmark brand performance by comparing total revenue against profit margins.
- Uncover low-performing vendors and inventory capital inefficiency (unsold stock).
- Deliver an executive-ready **Power BI Dashboard** alongside deep **Exploratory Data Analysis (EDA)**.

---

## 🛠️ Tech Stack & Workflow

| Tool | Purpose |
| :--- | :--- |
| **SQL (SQLite)** | Multi-table joins, data extraction, and metric aggregations across large transaction tables |
| **Python (Pandas, NumPy)** | Data cleaning, consistency filtering, and statistical analysis |
| **Data Visualization (Seaborn, Matplotlib)** | Outlier detection, distribution plots, and correlation heatmaps |
| **Power BI** | Executive KPI cards, interactive visuals, supplier distribution, and funnel charts |
| **Git / GitHub** | Version control and portfolio documentation |

### Data Pipeline Architecture
```
[Raw Inventory & Sales DB (12M+ records)]
                 │
                 ▼  (SQL Joins & Group By aggregations in EDA.ipynb)
    [vendor_sales_summary.csv (10.6K aggregated records)]
                 │
         ┌───────┴───────────────────────┐
         ▼                               ▼
[Python In-Depth Analysis]     [Power BI Dashboard]
- Outlier detection            - Executive KPI cards
- Profitability correlation    - Vendor contribution donut
- Negative margin filtering    - Top brands vs sales
                               - Margin distribution funnel
```

---

## 📁 Repository Structure

```
VendorScope/
├── .gitignore                          # Excludes checkpoints, venvs, and cache files
├── requirements.txt                    # Python dependencies
├── README.md                           # Comprehensive project documentation
├── vendor_sales_summary.csv            # Cleaned, aggregated dataset (10,692 rows, 18 columns)
├── Vendor Performance Dashboard.pbix   # Power BI interactive report
├── EDA.ipynb                           # SQL data extraction & preliminary exploration
└── Vendor_Performance_Analysis.ipynb   # In-depth statistical EDA, distribution & correlation analysis
```

---

## 📈 Key Dashboard Metrics (KPIs)

The executive dashboard tracks five fundamental retail health indicators:

- **Total Sales**: Aggregate revenue generated across all product lines.
- **Total Purchases**: Procurement expenditure across all suppliers.
- **Gross Profit**: Net earnings generated after factoring in direct costs.
- **Profit Margin**: Operational profitability percentage across vendors and brands.
- **Unsold Capital**: Capital locked up in excess inventory, highlighting working capital risks.

> **Power BI File**: Open `Vendor Performance Dashboard.pbix` in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) to interact with the slicers, vendor rankings, and contribution charts.

---

## 🔍 Core Analysis & Findings

### 1. Supplier Concentration & Dependency
- The top-ranking vendor accounts for **~24.8% of total purchase expenditure**, highlighting heavy supplier reliance.
- Top revenue drivers:
  1. **Diageo North America**
  2. **Martignetti Companies**
  3. **Pernod Ricard USA**
  4. **Jim Beam Brands Company**
  5. **Bacardi USA**

### 2. High-Volume Brands
- Key revenue-generating consumer brands include **Jack Daniel's**, **Tito's Handmade Vodka**, **Grey Goose**, **Captain Morgan**, and **Absolut Vodka**.

### 3. Profit Margin & Pricing Inefficiencies
- Scatter plot and funnel analysis reveal several high-volume vendors generating considerable gross sales while yielding below-average profit margins.
- Root causes identified: elevated freight/procurement costs, aggressive discounting, and unoptimized supplier contracts.

---

## 💡 Business Recommendations

1. **Diversify Supplier Portfolio**: Mitigate vulnerability from the primary supplier (~25% purchase volume) by negotiating terms with alternative regional distributors.
2. **Re-evaluate Low-Margin Volume Drivers**: Re-negotiate bulk procurement pricing or minimum advertised pricing (MAP) on high-sales/low-margin brands.
3. **Optimize Inventory Turnover**: Reallocate capital tied up in slow-moving stock (high unsold capital) toward rapid-turnover, high-margin inventory.

---

## 🚀 Getting Started & Setup

### Prerequisites
- Python 3.9+
- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (to view `.pbix`)

### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/VendorScope.git
cd VendorScope
```

### 2. Set Up Python Environment
```bash
# Create virtual environment
python -m venv .venv

# Activate virtual environment
# Windows (PowerShell):
.venv\Scripts\Activate.ps1
# macOS/Linux:
source .venv/bin/activate

# Install required dependencies
pip install -r requirements.txt
```

### 3. Run the Analysis
Launch Jupyter Notebook to view and run the analysis:
```bash
jupyter notebook
```
- Open `Vendor_Performance_Analysis.ipynb` to explore distributions, correlation heatmaps, and outlier checks.
- Open `EDA.ipynb` to review the SQL data extraction logic and dataset structure.

---

## 👤 Author

**Gajendra Verma**  
- **GitHub**: [@gaj085](https://github.com/gaj085)  
- **Email**: [gajendraverma085@gmail.com](mailto:gajendraverma085@gmail.com)  

---
⭐ *If you find this project useful, consider giving it a star on GitHub!*
