# 🛒 Retail Analytics & AI-Powered Sales Forecasting System

### Major Capstone Project — End-to-End Data Science Solution

An end-to-end **Retail Analytics and Sales Forecasting System** developed using Python to transform multi-store retail transaction data into meaningful business insights.

The project combines **data preprocessing, exploratory data analysis, KPI analysis, interactive visualization, time-series forecasting, K-Means clustering, and automated management insights** to support data-driven retail decision-making.

---

## 📌 Project Overview

Modern retail businesses generate large amounts of transactional data across stores, products, customers, regions, payment channels, promotions, and inventory.

However, raw transactional data alone does not directly help management make decisions.

This project develops a complete analytical pipeline that converts raw retail sales data into:

- Business KPIs
- Sales and revenue trends
- Product performance insights
- Store and regional comparisons
- Customer and payment analysis
- Promotional analysis
- Revenue forecasting
- Machine-learning-based store segmentation
- Automated management recommendations

The overall objective is to move from:

**Raw Data → Analysis → Prediction → Business Insights → Decision Support**

---

# 🎯 Project Objectives

The major objectives of the project are:

1. Clean and preprocess retail transaction data.
2. Analyze overall retail sales and revenue performance.
3. Identify high-performing products, stores, and regions.
4. Analyze customer, payment, promotion, and holiday behaviour.
5. Visualize important business patterns.
6. Forecast future revenue using time-series modelling.
7. Segment stores according to performance using K-Means clustering.
8. Automatically generate management-oriented business insights.
9. Export analytical results for future dashboards or BI applications.

---

# 📂 Repository Structure

```text
Retail-Analytics-Sales-Forecasting/
│
├── README.md
├── requirements.txt
├── LICENSE
├── .gitignore
│
├── data/
│   └── Retail_Sales_Data.xlsx
│
├── notebooks/
│   └── Retail_Analytics_Sales_Forecasting.ipynb
│
├── images/
│   ├── monthly_revenue_trend.png
│   ├── category_performance.png
│   ├── store_performance.png
│   ├── regional_performance.png
│   ├── customer_analysis.png
│   ├── payment_mode_analysis.png
│   ├── promotion_analysis.png
│   ├── correlation_matrix.png
│   ├── forecast_evaluation.png
│   ├── revenue_forecast.png
│   └── store_segmentation.png
│
└── outputs/
    ├── monthly_revenue.csv
    ├── category_summary.csv
    ├── store_summary.csv
    ├── store_segments.csv
    ├── revenue_forecast_30_days.csv
    └── business_insights.txt
```

---

# 📊 Dataset

The dataset used for this project is included in the repository.

### Download / View Dataset

[`Retail_Sales_Data.xlsx`](data/Retail_Sales_Data.xlsx)

The original dataset contains:

- **73,000 transaction records**
- **19 original features**
- **8 retail stores**
- **5 major product categories**
- Transactions from **1 January 2023 to 31 December 2024**

After feature engineering, the analytical dataset contains **27 features**.

---

## Dataset Features

| Feature | Description |
|---|---|
| `Date` | Date of transaction |
| `Store_ID` | Unique store identifier |
| `Store_Location` | Location/city of the store |
| `Product_ID` | Unique product identifier |
| `Product_Category` | Main product category |
| `Product_Subcategory` | Product subcategory |
| `Brand` | Product brand |
| `Unit_Price` | Price per unit |
| `Units_Sold` | Number of units sold |
| `Total_Sales` | Gross transaction value |
| `Discount_Percentage` | Discount applied |
| `Revenue` | Revenue generated after discount |
| `Customer_Type` | Type of customer |
| `Payment_Mode` | Payment method |
| `Promotion_Applied` | Whether a promotion was applied |
| `Stock_On_Hand` | Available inventory |
| `Store_Rating` | Store rating |
| `Region` | Geographic region |
| `Holiday_Flag` | Holiday/non-holiday indicator |

---

## Dataset Preview

| Date | Store | Location | Category | Brand | Unit Price | Units Sold | Discount | Revenue | Payment |
|---|---|---|---|---|---:|---:|---:|---:|---|
| 13-04-2023 | STR_104 | Chennai | Sports | Reebok | ₹29,973.06 | 39 | 5% | ₹1,110,501.87 | Debit Card |
| 25-10-2024 | STR_103 | Delhi | Sports | Yonex | ₹46,933.78 | 2 | 15% | ₹79,787.43 | UPI |
| 28-02-2023 | STR_107 | Kolkata | Groceries | Nestle | ₹39,280.28 | 44 | 15% | ₹1,469,082.47 | Cash |

---

# 🔄 Project Workflow

```text
                         RAW RETAIL DATA
                               │
                               ▼
                    Data Quality Analysis
                               │
                               ▼
                   Cleaning & Preprocessing
                               │
                               ▼
                     Feature Engineering
                               │
             ┌─────────────────┼─────────────────┐
             │                 │                 │
             ▼                 ▼                 ▼
       KPI Analysis          EDA           Visualization
             │                 │                 │
             └─────────────────┼─────────────────┘
                               ▼
                    Business Performance
                           Analysis
                               │
                    ┌──────────┴──────────┐
                    │                     │
                    ▼                     ▼
             Time-Series             K-Means
              Forecasting            Clustering
                    │                     │
                    └──────────┬──────────┘
                               ▼
                     Automated Business
                           Insights
                               │
                               ▼
                     Management Decision
                           Support
```

---

# 🧹 Data Cleaning & Preprocessing

Before analysis, the dataset is validated and cleaned.

The preprocessing pipeline includes:

- Date conversion
- Missing-value analysis
- Duplicate detection
- Numeric datatype validation
- Removal of invalid records
- Standardization of analytical fields

### Data Quality Results

- Missing values: **0**
- Duplicate rows: **0**
- Final cleaned records: **73,000**

---

# 🛠️ Feature Engineering

Several additional analytical variables are generated:

- `Year`
- `Month`
- `Month_Name`
- `Quarter`
- `Day_Name`
- `Year_Month`
- `Revenue_Per_Unit`

A derived value representing the difference between gross sales and realized revenue is also calculated for discount-related analysis.

These additional features allow the dataset to be analyzed across time, products, stores, and transaction characteristics.

---

# 📌 Key Performance Indicators

The project calculates major management KPIs from the complete dataset.

| KPI | Result |
|---|---:|
| 💰 Total Revenue | ₹41,133,782,865.04 |
| 🧾 Gross Sales | ₹45,708,091,467.57 |
| 📦 Total Units Sold | 1,817,305 |
| 💳 Average Transaction Revenue | ₹563,476.48 |
| 🏷️ Average Discount | 10.01% |

These KPIs provide a high-level summary of overall retail performance.

---

# 📈 Exploratory Data Analysis

## 1. Monthly Revenue Trend

Revenue is aggregated monthly to understand historical sales movement and fluctuations.

![Monthly Revenue Trend](images/monthly_revenue_trend.png)

The graph provides a time-based view of how retail revenue changed between 2023 and 2024.

### Business Application

Monthly revenue analysis can support:

- Performance tracking
- Trend identification
- Budget planning
- Revenue forecasting
- Seasonal analysis

---

# 🛍️ 2. Product Category Performance

Product categories are compared using both revenue and units sold.

![Revenue by Product Category](images/category_performance.png)

### Category Results

| Product Category | Revenue | Units Sold |
|---|---:|---:|
| Electronics | ₹8.319 B | 367,921 |
| Home Appliances | ₹8.263 B | 365,113 |
| Fashion | ₹8.216 B | 361,431 |
| Groceries | ₹8.171 B | 359,711 |
| Sports | ₹8.166 B | 363,129 |

### 🏆 Highest Revenue Category

**Electronics**

Revenue:

**₹8,318,538,869**

### Business Application

Category analysis helps management make decisions regarding:

- Inventory allocation
- Product assortment
- Category marketing
- Sales targets
- Stock planning

---

# 🏪 3. Store Performance Analysis

Stores are evaluated according to:

- Total revenue
- Units sold
- Number of transactions
- Average rating
- Average discount

![Store-wise Revenue Performance](images/store_performance.png)

### Store Performance

| Store | Location | Region | Revenue |
|---|---|---|---:|
| STR_103 | Delhi | North | ₹5.223 B |
| STR_102 | Bangalore | South | ₹5.186 B |
| STR_101 | Mumbai | West | ₹5.170 B |
| STR_104 | Chennai | South | ₹5.166 B |
| STR_105 | Pune | West | ₹5.162 B |
| STR_107 | Kolkata | East | ₹5.108 B |
| STR_108 | Ahmedabad | West | ₹5.078 B |
| STR_106 | Hyderabad | South | ₹5.041 B |

### 🏆 Highest Revenue Store

**Delhi — STR_103**

Revenue:

**₹5,223,064,264**

### Business Application

Store comparison helps management identify:

- Strong-performing stores
- Locations requiring improvement
- Resource-allocation opportunities
- Store-level sales differences

---

# 🌍 4. Regional Revenue Analysis

Revenue is aggregated across geographic regions.

![Revenue by Region](images/regional_performance.png)

### 🏆 Strongest Region

**West**

Regional analysis can assist with:

- Geographic expansion
- Regional campaigns
- Inventory distribution
- Resource allocation
- Performance benchmarking

---

# 👥 5. Customer Type Analysis

Revenue is compared across customer types.

![Revenue by Customer Type](images/customer_analysis.png)

Customer analysis can help identify differences in revenue contribution between different customer groups and support future customer-targeting strategies.

---

# 💳 6. Payment Mode Analysis

The project compares total revenue generated through different payment methods.

![Revenue by Payment Mode](images/payment_mode_analysis.png)

### 🏆 Highest Revenue Payment Mode

**Credit Card**

This analysis provides insight into customer payment preferences and can support payment-related partnerships and incentives.

---

# 🏷️ 7. Promotion Analysis

Transactions are divided according to whether a promotion was applied.

![Promotion Analysis](images/promotion_analysis.png)

The analysis found that promotional transactions had an average revenue difference of:

**-0.29%**

compared with non-promotional transactions.

This suggests that, in this dataset, promotional transactions did not automatically correspond to higher average transaction revenue.

### Business Application

This analysis can help evaluate whether promotions are producing meaningful revenue improvements.

---

# 🎉 8. Holiday vs Non-Holiday Analysis

Transactions are also analyzed according to holiday status.

| Day Type | Total Revenue | Average Revenue | Units Sold | Records |
|---|---:|---:|---:|---:|
| Non-Holiday | ₹40.641 B | ₹563,650.82 | 1,795,915 | 72,103 |
| Holiday | ₹492.868 M | ₹549,462.78 | 21,390 | 897 |

This provides additional context for understanding transaction behaviour during holiday periods.

---

# 🔗 9. Correlation Analysis

A correlation matrix is generated for numerical variables.

![Correlation Matrix](images/correlation_matrix.png)

Variables analyzed include:

- Unit Price
- Units Sold
- Total Sales
- Discount Percentage
- Revenue
- Stock on Hand
- Store Rating
- Holiday Flag

Correlation analysis helps identify statistical relationships among numerical business variables.

> **Note:** Correlation represents statistical association and does not necessarily imply causation.

---

# 🔮 Time-Series Revenue Forecasting

One of the major predictive components of the project is **future revenue forecasting**.

The model used is:

## Holt-Winters Exponential Smoothing

The model configuration includes:

- **Additive Trend**
- **Additive Seasonality**
- **7-Day Seasonal Period**

Transaction-level revenue is first aggregated into daily revenue.

---

## Train-Test Evaluation

The final **60 days** of historical data are reserved as test data.

The model is trained on the remaining historical observations and evaluated by comparing predicted revenue against actual revenue.

![Forecast Model Evaluation](images/forecast_evaluation.png)

### Model Performance

| Metric | Result |
|---|---:|
| MAE | ₹5,582,397.32 |
| RMSE | ₹6,744,573.91 |
| MAPE | **10.01%** |

The evaluation provides a quantitative measure of the model's forecasting performance on unseen historical data.

---

# 📅 30-Day Future Revenue Forecast

After evaluation, the Holt-Winters model is retrained using the complete historical daily revenue dataset.

It then predicts revenue for the next:

## **30 Days**

![30-Day Revenue Forecast](images/revenue_forecast.png)

### Forecast Period

**1 January 2025 onward**

The first forecasted values include:

| Date | Forecasted Revenue |
|---|---:|
| 01-Jan-2025 | ₹56,263,484.59 |
| 02-Jan-2025 | ₹56,531,959.98 |
| 03-Jan-2025 | ₹54,278,159.70 |
| 04-Jan-2025 | ₹56,893,708.98 |
| 05-Jan-2025 | ₹57,062,172.88 |

### 💰 Forecasted 30-Day Revenue

# **≈ ₹1.684 Billion**

### Business Application

Revenue forecasting can assist management with:

- Revenue planning
- Inventory planning
- Operational budgeting
- Resource allocation
- Target setting
- Short-term business planning

---

# 🤖 Store Segmentation Using K-Means

The second machine-learning component of the project performs **store performance segmentation**.

Instead of evaluating every store independently, K-Means clustering groups stores with similar characteristics.

---

## Features Used for Clustering

The model uses:

- Total Revenue
- Total Units Sold
- Average Store Rating
- Average Discount
- Average Stock
- Number of Transactions

Before clustering, all features are standardized using:

**StandardScaler**

This prevents variables with large numerical values, such as revenue, from dominating the clustering process.

---

## K-Means Configuration

```text
Number of Clusters = 3
Random State = 42
n_init = 20
```

The resulting clusters are converted into business-oriented labels:

### 🟢 High-Performance Stores
Stores showing stronger overall performance characteristics.

### 🟡 Stable Stores
Stores demonstrating moderate or relatively stable performance.

### 🔴 Developing Stores
Stores showing comparatively lower performance characteristics and potential improvement opportunities.

---

## Store Segmentation Results

![Store Performance Segmentation](images/store_segmentation.png)

The segmentation generated the following classifications:

| Store | Location | Segment |
|---|---|---|
| STR_103 | Delhi | High-Performance Stores |
| STR_102 | Bangalore | High-Performance Stores |
| STR_107 | Kolkata | High-Performance Stores |
| STR_101 | Mumbai | Stable Stores |
| STR_104 | Chennai | Stable Stores |
| STR_105 | Pune | Stable Stores |
| STR_108 | Ahmedabad | Developing Stores |
| STR_106 | Hyderabad | Developing Stores |

### Clustering Evaluation

**Silhouette Score: 0.36**

The silhouette score is used as an internal measure of how well observations are separated into their assigned clusters.

### Business Application

Store segmentation allows management to use differentiated strategies for different store groups.

For example:

- Protect and learn from high-performing stores
- Maintain and optimize stable stores
- Develop improvement plans for developing stores

---

# 🧠 Automated Business Insights

The final analytical stage automatically converts model outputs and analytical results into management-oriented observations.

### Insights Generated by the System

**1. Product Performance**

Electronics is the highest-revenue category, generating approximately:

**₹8.319 Billion**

---

**2. Store Performance**

Delhi (`STR_103`) is the highest-revenue store, generating approximately:

**₹5.223 Billion**

---

**3. Regional Performance**

**West** is the strongest region by total revenue.

---

**4. Payment Behaviour**

**Credit Card** contributes the highest total revenue among payment modes.

---

**5. Promotion Performance**

Promotional transactions show an average revenue difference of:

**-0.29%**

compared with non-promotional transactions.

---

**6. Recent Revenue Movement**

Revenue during the latest 30-day period changed by:

**+1.19%**

compared with the previous 30 days.

---

**7. Future Revenue**

The next 30-day forecast estimates total revenue of approximately:

# **₹1.684 Billion**

---

**8. Management Recommendation**

Management can prioritize inventory and marketing resources for high-performing categories while developing improvement strategies for lower-performing store segments.

---

# 🖼️ Visualization Gallery

## Revenue Trend

![Monthly Revenue](images/monthly_revenue_trend.png)

## Category Performance

![Category Performance](images/category_performance.png)

## Store Performance

![Store Performance](images/store_performance.png)

## Regional Analysis

![Regional Performance](images/regional_performance.png)

## Customer Analysis

![Customer Analysis](images/customer_analysis.png)

## Payment Mode Analysis

![Payment Mode](images/payment_mode_analysis.png)

## Promotion Analysis

![Promotion Analysis](images/promotion_analysis.png)

## Correlation Matrix

![Correlation Matrix](images/correlation_matrix.png)

## Forecast Evaluation

![Forecast Evaluation](images/forecast_evaluation.png)

## Future Revenue Forecast

![Revenue Forecast](images/revenue_forecast.png)

## Store Segmentation

![Store Segmentation](images/store_segmentation.png)

---

# 💾 Exported Results

The project automatically exports major analytical outputs to the `outputs/` directory.

| File | Purpose |
|---|---|
| `monthly_revenue.csv` | Monthly revenue analysis |
| `category_summary.csv` | Product-category performance |
| `store_summary.csv` | Store-level performance |
| `store_segments.csv` | K-Means store segmentation |
| `revenue_forecast_30_days.csv` | Future 30-day forecast |
| `business_insights.txt` | Automatically generated business insights |

These files can later be connected to:

- Power BI
- Tableau
- Streamlit
- Excel dashboards
- Other BI applications

---

# 🛠️ Technologies Used

### Programming Language

- Python

### Data Manipulation

- Pandas
- NumPy

### Data Visualization

- Plotly
- Matplotlib

### Machine Learning

- Scikit-learn
- K-Means Clustering
- StandardScaler

### Time-Series Forecasting

- Statsmodels
- Holt-Winters Exponential Smoothing

### Model Evaluation

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Percentage Error (MAPE)
- Silhouette Score

### Development Environment

- Jupyter Notebook
- Google Colab

---

# ⚙️ Installation & Setup

## 1. Clone the Repository

```bash
git clone <YOUR-GITHUB-REPOSITORY-URL>
```

Move into the project directory:

```bash
cd Retail-Analytics-Sales-Forecasting
```

---

## 2. Install Required Libraries

```bash
pip install -r requirements.txt
```

The main dependencies are:

```text
numpy
pandas
matplotlib
plotly
scikit-learn
statsmodels
openpyxl
jupyter
```

---

## 3. Dataset

The dataset is already available inside:

```text
data/Retail_Sales_Data.xlsx
```

Load it using:

```python
import pandas as pd

df = pd.read_excel("data/Retail_Sales_Data.xlsx")

print(df.shape)
df.head()
```

Expected shape:

```text
(73000, 19)
```

---

## 4. Run the Notebook

Open:

```text
notebooks/Retail_Analytics_Sales_Forecasting.ipynb
```

Run the cells sequentially.

The notebook performs the complete pipeline:

```text
Dataset
   ↓
Preprocessing
   ↓
Feature Engineering
   ↓
KPI Analysis
   ↓
EDA
   ↓
Visualizations
   ↓
Forecasting
   ↓
K-Means Clustering
   ↓
Business Insights
   ↓
Exported Results
```

---

# 📦 requirements.txt

```text
numpy
pandas
matplotlib
plotly
scikit-learn
statsmodels
openpyxl
jupyter
```

---

# 🚀 Business Applications

The project demonstrates how data analytics and machine learning can support retail decisions related to:

- Revenue monitoring
- Product-category strategy
- Inventory planning
- Store benchmarking
- Regional performance
- Customer analysis
- Payment behaviour
- Promotional effectiveness
- Revenue forecasting
- Resource allocation
- Store improvement strategies

---

# 🔭 Future Enhancements

The project can be extended further through:

### 1. Interactive Dashboard

Develop a **Streamlit dashboard** where users can interactively explore:

- Revenue
- Categories
- Stores
- Regions
- Forecasts
- Store clusters

### 2. Business Intelligence Integration

Connect exported results with:

- Power BI
- Tableau

### 3. Advanced Forecasting

Compare Holt-Winters against:

- ARIMA / SARIMA
- Prophet
- XGBoost
- LSTM

### 4. Product-Level Demand Forecasting

Predict future demand separately for different products and categories.

### 5. Inventory Optimization

Combine demand forecasts with stock levels to recommend inventory requirements.

### 6. Customer Segmentation

Apply clustering techniques to identify different customer groups.

### 7. Real-Time Data Integration

Connect the system to a database or API instead of relying on static Excel files.

### 8. Model Deployment

Expose forecasting functionality through a web application or REST API.

---

# 📌 Key Project Highlights

- ✅ **73,000 retail transactions analyzed**
- ✅ **19 original dataset features**
- ✅ **27 features after preprocessing and feature engineering**
- ✅ **8 stores analyzed**
- ✅ **5 product categories analyzed**
- ✅ **₹41.13B total revenue analyzed**
- ✅ **1.817M units sold analyzed**
- ✅ **Interactive Plotly visualizations**
- ✅ **Holt-Winters time-series forecasting**
- ✅ **10.01% forecasting MAPE**
- ✅ **30-day future revenue forecast**
- ✅ **K-Means store segmentation**
- ✅ **Automated management insights**
- ✅ **Exportable analytical outputs**

---

# 🎓 Project Type

**Major  Project**

**Domain:** Data Analytics / Data Science / Machine Learning / Business Analytics

---

# 👩‍💻 Author

## Bhavya Chopra



Major Project

---

# ⚠️ Disclaimer

This project has been developed for **academic, learning, and portfolio purposes**.

The analytical findings, forecasts, store classifications, and recommendations are derived from the supplied retail dataset and should not be interpreted as real-world financial or business advice.

---

# ⭐ Conclusion

This project demonstrates a complete data analytics workflow that converts raw retail transaction data into a practical **decision-support system**.

The system combines:

**Descriptive Analytics**  
↓  
**Exploratory Data Analysis**  
↓  
**Business Visualization**  
↓  
**Predictive Analytics**  
↓  
**Machine Learning Segmentation**  
↓  
**Automated Business Insights**

By combining historical analysis with forecasting and clustering, the project demonstrates how data can be transformed into actionable information for **inventory planning, store management, marketing decisions, resource allocation, and future revenue planning**.
