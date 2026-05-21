# 📊 Sales Performance Analytics & Revenue Forecasting

**Tools Used:** Excel | Python (Pandas, NumPy, Matplotlib)

---

## 📌 Project Overview

This project analyzes transactional sales data to evaluate business performance, identify revenue trends, and forecast future revenue using statistical trend modeling.

The objective of this project was to:

- Clean and preprocess raw sales data  
- Perform exploratory data analysis (EDA)  
- Track key performance indicators (KPIs)  
- Analyze regional and category-level performance  
- Generate actionable business insights for strategic planning  

---

## 📂 Dataset Information

- Dataset: Superstore Sales Dataset  
- Records: ~9,000+ transactions  
- Key Features:
  - Order Date  
  - Region  
  - Category  
  - Sub-Category  
  - Sales  
  - Profit  
  - Quantity  
  - Segment  

---

# 🧹 Data Cleaning & Processing (Python)

The raw dataset was cleaned and processed using Python:

- Removed duplicate records  
- Converted mixed-format date values using `pd.to_datetime()`  
- Created new features:
  - Year  
  - Month  
  - Month-Year  
- Checked for missing values  
- Structured data for time-series analysis  

### Example Code:

```python
import pandas as pd

df = pd.read_csv("superstore.csv")

#Check missing values
df.isnull().sum()

# Convert date column
df['Order Date'] = pd.to_datetime(df['Order Date'], format='mixed')
df['Ship Date'] = pd.to_datetime(df['Ship Date'], format='mixed')

# Create new features
df['Year'] = df['Order Date'].dt.year
df['Month'] = df['Order Date'].dt.month
df['Month-Year'] = df['Order Date'].dt.to_period('M')
```

📊 Exploratory Data Analysis (EDA)
Key KPIs Calculated:

- Total Sales
- Total Profit
- Total Orders
- Profit Margin (%)
- Average Order Value
- Total Quantity Sold

Business Analysis Performed:

- Monthly revenue trend analysis
- Regional sales performance comparison
- Category-wise profitability analysis

📊 Excel Dashboard

An interactive Excel dashboard was developed using:

- Pivot Tables
- Pivot Charts
- KPI Cards
- Slicers (Region, Category, Segment, Year)

Dashboard Features:

- Dynamic filtering
- Real-time KPI updates
- Sales visualization
- Category and regional performance comparison

🔍 Key Insights

- West region generated the highest revenue contribution.
- Technology category delivered the highest profitability.
- Regional and category analysis helped identify high-performing business areas.
- Furniture category showed relatively lower profit margins.

🏢 Business Impact

This analysis supports:

- Inventory planning
- Regional performance optimization
- Strategic category-level decision-making
- Data-driven business insights

🛠 Tools & Technologies

- Python (Pandas, NumPy, Matplotlib)
- Excel (Pivot Tables, Charts, Slicers)
- Data Analytics

## ⭐ Author

**Palak Gupta**  
Data Analyst | Business Intelligence | HR Analytics  
📍 India  
🔗 GitHub: [https://github.com/palakguptaa02] 
