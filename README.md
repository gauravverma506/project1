#  E-commerce Return Rate Reduction Analysis

##  Objective
This project analyzes e-commerce order and return data to:
- Identify patterns in product returns
- Understand how return rates vary across categories, suppliers, geography, and marketing channels
- Predict the likelihood of product returns using logistic regression
- Generate a return risk score per product
- Create an interactive Power BI dashboard to support decision-making

---

##  Tools Used
- **Python (Pandas, Scikit-learn)** for data cleaning and prediction
- **Power BI** for dashboard and visual analytics
- **CSV files** for input/output datasets
- **Jupyter Notebook / Colab** for development and testing

---

##  Project Structure
- ecommerce_data.csv # Input dataset (200 records)
- high_risk_products.csv # Output of products with high return risk
- return_prediction.py # Python script for model and scoring
- PowerBI_Dashboard.pbix # Power BI file with visualizations (to be created)
- README.md # Project documentation


---

## 🔍 Analysis Summary

### 1. Data Cleaning
- Removed duplicates and null values
- Standardized column names

### 2. Return Rate Analysis
- Return % calculated per `Category` and `Supplier`
- Group-based summary insights generated in Python

### 3. Predictive Modeling
- Logistic Regression used to model return behavior
- Features: Category, Region, Marketing Channel, Price, Quantity
- Target: `ReturnFlag` (1 = returned, 0 = not returned)
- Output: `return_risk_score` (0–1)

### 4. Risk Classification
- Products with risk score > 0.7 are labeled as high-risk
- High-risk products exported to `high_risk_products.csv`

---

##  Power BI Dashboard
**Included Visuals:**
- Return % by Category (Bar chart)
- Return % by Supplier
- Return % by Region (Map)
- Return % by Marketing Channel
- Table of High-Risk Products (filtered from return risk score)
- Drill-through filters for Category, Region, ProductID

---

##  Getting Started

### Prerequisites
- Python 3.7+
- Power BI Desktop
- Packages: `pandas`, `scikit-learn`

### Run the Python Script
```bash
pip install pandas scikit-learn
python return_prediction.py
