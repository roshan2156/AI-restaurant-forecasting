AI Demand Forecasting for Restaurant Sales
📊 Project Overview

This project focuses on time-series demand forecasting for restaurant sales using historical Point-of-Sale (POS) data. The goal is to identify trends, seasonality patterns, holiday effects, and customer demand behavior to build forecasting-ready features for machine learning models.

The project covers:

Exploratory Data Analysis (EDA)
Time-Series Analysis
Seasonal Decomposition
Autocorrelation Analysis (ACF/PACF)
Feature Engineering
Demand Pattern Discovery
Forecasting Dataset Preparation
🚀 Project Objectives
Analyze daily restaurant sales data
Discover weekly and monthly seasonality
Measure holiday and weekend impact
Identify top-performing menu items
Generate forecasting features
Prepare data for machine learning demand forecasting models
📂 Dataset Information

Dataset: restaurant_sales.csv

Property	Value
Domain	Food & Restaurant Services
Date Range	Jan 2023 – Dec 2024
Records	5,848
Granularity	Daily Sales per Menu Item
Menu Items	8
Time Span	731 Days
Menu Items
Biryani
Butter Chicken
Dal Makhani
Gulab Jamun
Mango Lassi
Masala Dosa
Naan
Paneer Tikka
Dataset Columns
Column	Description
date	Transaction date
day_of_week	Day name
month	Month number
year	Year
is_weekend	Weekend flag
is_holiday	Holiday flag
menu_item	Product name
units_sold	Quantity sold
unit_price	Price per item
revenue	Daily revenue
📦 Installation

Clone the repository:

git clone https://github.com/yourusername/ai-demand-forecasting.git
cd ai-demand-forecasting

Install dependencies:

pip install pandas numpy matplotlib seaborn statsmodels
🛠 Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Statsmodels
Google Colab
📈 Exploratory Data Analysis
Data Validation

Performed:

Date conversion
Null value detection
Duplicate checking
Missing date verification

Results:

✅ 0 missing values
✅ 0 missing dates
✅ Continuous time series
✅ 731 unique dates
📊 Key Business Insights
Revenue Growth
Year	Average Daily Revenue
2023	₹148,654
2024	₹178,426

Year-over-Year Growth: +20%

Weekly Seasonality
Metric	Value
Best Day	Friday
Worst Day	Monday
Weekend Premium	+30.6%

Key Finding:

Restaurants experience significantly higher revenue during weekends.

Monthly Seasonality

Top Months:

November
October
December

Lowest Month:

June

The festive season generates the strongest sales performance.

Holiday Impact
Category	Average Revenue
Non-Holiday	₹161,753
Holiday	₹256,134

Holiday Premium: +58.3%

🍛 Menu Item Performance
Highest Revenue Items
Rank	Item
1	Biryani
2	Butter Chicken
3	Paneer Tikka
Highest Volume Items
Rank	Item
1	Naan
2	Biryani
3	Butter Chicken
Key Observation
Biryani drives maximum revenue.
Naan sells the most units but has a lower price point.
Mango Lassi exhibits seasonal demand spikes during warmer months.
🔍 Time-Series Analysis
Seasonal Decomposition

Performed decomposition into:

Trend Component
Seasonal Component
Residual Component

Periods analyzed:

Weekly Seasonality (7 days)
Monthly Seasonality (30 days)
Autocorrelation Analysis

Significant lag values:

Lag	Correlation
1	0.57
2	0.40
7	0.86
14	0.83

Key Finding:

Strong weekly repeating sales patterns exist.

⚙️ Feature Engineering
Chronological Features
day_of_week
day_name
month
month_name
year
quarter
week_of_year
is_weekend
is_holiday
Lag Features
lag_1
lag_7
lag_14
Rolling Window Features
rolling_7_mean
rolling_14_mean
rolling_30_mean
Trend Features
day_number
📋 Final Forecasting Features
[
    'day_of_week',
    'month',
    'quarter',
    'week_of_year',
    'is_weekend',
    'is_holiday',
    'lag_1',
    'lag_7',
    'lag_14',
    'rolling_7_mean',
    'rolling_14_mean',
    'rolling_30_mean'
]
📉 Train-Test Strategy

Time-series forecasting requires chronological splitting.

Split Method
Train Set  → First 10 Months
Test Set   → Last 2 Months

This prevents data leakage and simulates real-world forecasting.

📊 Visualizations Included
Revenue Distribution
Units Sold Distribution
Daily Revenue Trend
7-Day Rolling Average
30-Day Rolling Average
Weekly Seasonality Analysis
Revenue Heatmaps
Monthly Trend Analysis
Item-Level Performance Charts
Holiday Impact Analysis
Seasonal Decomposition
ACF Plot
PACF Plot
🎯 Project Outcomes

The analysis identified:

Strong weekly seasonality
Significant holiday effects
Long-term growth trend
Item-specific demand patterns
Important forecasting lag features

These findings form the foundation for machine learning demand forecasting models.

📌 Future Work
Stationarity Testing (ADF Test)
Feature Scaling
Model Training
Linear Regression
Random Forest
XGBoost
Prophet
SARIMA
Hyperparameter Tuning
Forecast Evaluation
Production Deployment
