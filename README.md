# Retail Analytics & AI-Powered Sales Forecasting System

An end-to-end data analytics and machine learning project that transforms multi-store retail sales data into actionable business insights.

The system performs exploratory data analysis, evaluates store and product performance, forecasts future revenue using time-series modelling, segments stores using K-Means clustering, and automatically generates management-oriented recommendations.

## Project Overview

Retail businesses generate large volumes of transactional data across stores, products, customers, regions, and payment channels. Converting this raw information into useful decisions can be challenging.

This project develops a data-driven decision-support system that analyzes historical retail sales and answers questions such as:

- Which product categories generate the highest revenue?
- Which stores and regions perform best?
- How do discounts and promotions influence revenue?
- What sales patterns exist over time?
- What revenue can be expected in the next 30 days?
- Which stores demonstrate similar performance characteristics?
- What business actions can management take based on the results?

## Dataset

The analysis uses a retail sales dataset containing **73,000 transaction records** across multiple stores and locations.

The dataset contains information such as:

- Date
- Store ID
- Store Location
- Product ID
- Product Category
- Product Subcategory
- Brand
- Unit Price
- Units Sold
- Total Sales
- Discount Percentage
- Revenue
- Customer Type
- Payment Mode
- Promotion Applied
- Stock on Hand
- Store Rating
- Region
- Holiday Flag

The available data covers:

**January 2023 – December 2024**

with **8 retail stores** and **5 major product categories**.

## Project Workflow

```text
Raw Retail Dataset
        ↓
Data Loading
        ↓
Data Quality Checks
        ↓
Data Cleaning & Preprocessing
        ↓
Feature Engineering
        ↓
Exploratory Data Analysis
        ↓
KPI & Store Performance Analysis
        ↓
Time-Series Revenue Forecasting
        ↓
K-Means Store Segmentation
        ↓
Automatic Business Insights
        ↓
Management-Ready Outputs
```

## Data Preprocessing

The preprocessing pipeline performs:

- Date conversion and validation
- Duplicate removal
- Missing-value handling
- Numeric datatype validation
- Invalid-record removal
- Feature engineering

Additional analytical features created include:

- Year
- Month
- Month Name
- Quarter
- Day Name
- Year-Month
- Profit After Discount
- Revenue Per Unit

## Key Performance Indicators

The system calculates major retail KPIs including:

| KPI | Result |
|---|---:|
| Total Revenue | ₹41.13 Billion |
| Gross Sales | ₹45.71 Billion |
| Units Sold | 1,817,305 |
| Average Transaction Revenue | ₹563,476 |
| Average Discount | 10.01% |

## Exploratory Data Analysis

The project analyzes revenue and performance across several dimensions.

### Revenue Trend Analysis

Monthly revenue is aggregated and visualized to identify historical sales patterns and changes over time.

### Product Category Analysis

Revenue and unit sales are compared across product categories.

The highest-revenue category in the dataset was:

**Electronics — approximately ₹8.32 Billion**

### Store Performance Analysis

Stores are evaluated using:

- Total revenue
- Units sold
- Average rating
- Average discount
- Transaction volume

The highest-revenue store was:

**Delhi (STR_103) — approximately ₹5.22 Billion**

### Additional Analysis

The project also analyzes:

- Regional performance
- Customer types
- Payment methods
- Promotional transactions
- Holiday vs non-holiday performance
- Numerical feature correlations

## Revenue Forecasting

Future revenue is predicted using:

**Holt-Winters Exponential Smoothing**

The model incorporates:

- Additive trend
- Additive seasonality
- Weekly seasonal cycle

The final **60 days** of historical data are reserved as a test set before the model is retrained using the complete dataset.

### Forecast Evaluation

| Metric | Result |
|---|---:|
| MAE | ₹5.58 Million |
| RMSE | ₹6.74 Million |
| MAPE | 10.01% |

After evaluation, the model is retrained using the complete historical dataset to generate a:

**30-Day Revenue Forecast**

Estimated revenue for the following 30 days:

**≈ ₹1.68 Billion**

## Store Segmentation

K-Means clustering is used to identify stores with similar performance characteristics.

Features used for clustering include:

- Total Revenue
- Total Units Sold
- Average Rating
- Average Discount
- Average Stock
- Number of Transactions

Before clustering, the features are standardized using `StandardScaler`.

The stores are divided into three management-oriented segments:

1. **High-Performance Stores**
2. **Stable Stores**
3. **Developing Stores**

The resulting clustering achieved a **Silhouette Score of 0.36**.

The segmentation can help management differentiate strategies for high-performing and developing locations.

## Automated Business Insights

The system automatically converts analytical results into management-oriented observations.

Examples generated from the dataset include:

- Electronics was the highest-revenue product category.
- Delhi was the highest-revenue store.
- West was the strongest region by total revenue.
- Credit Card generated the highest revenue among payment modes.
- Promotional transactions showed only a small difference in average revenue compared with non-promotional transactions.
- Revenue in the latest 30-day period increased compared with the previous 30-day period.
- Forecasting estimated approximately ₹1.68 billion in revenue for the following 30 days.

This layer converts numerical analysis into information that can be interpreted directly by business stakeholders.

## Technologies Used

### Programming
- Python

### Data Analysis
- Pandas
- NumPy

### Visualization
- Plotly
- Matplotlib

### Machine Learning
- Scikit-learn

### Time-Series Forecasting
- Statsmodels
- Holt-Winters Exponential Smoothing

### Development Environment
- Jupyter Notebook
- Google Colab

## Output Files

The analysis automatically exports reusable results to the `outputs/` directory.

```text
monthly_revenue.csv
category_summary.csv
store_summary.csv
store_segments.csv
revenue_forecast_30_days.csv
business_insights.txt
```

These files can be integrated with dashboards or further business-intelligence applications.

## How to Run the Project

### 1. Clone the repository

```bash
git clone <repository-url>
cd Retail-Analytics-Sales-Forecasting
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Add the dataset

Place the retail dataset inside:

```text
data/
```

### 4. Run the notebook

Open:

```text
notebooks/Retail_Analytics_Sales_Forecasting.ipynb
```

using Jupyter Notebook, JupyterLab, VS Code, or Google Colab.

Run the cells sequentially to reproduce the complete analysis.

## Business Applications

The system can support decisions related to:

- Revenue planning
- Store performance monitoring
- Inventory planning
- Product-category strategy
- Promotional analysis
- Regional performance comparison
- Resource allocation
- Short-term revenue forecasting

## Future Improvements

The project can be extended with:

- Interactive Streamlit dashboard
- Power BI/Tableau integration
- Product-level demand forecasting
- Customer segmentation
- Inventory optimization
- Forecast comparison using ARIMA, Prophet, XGBoost, or LSTM
- Automated model selection
- Real-time database integration
- API-based prediction service

## Author

**Bhavya Chopra**

Major  Project

## Disclaimer

This project is intended for academic and portfolio purposes. Forecasts and business recommendations are based on the supplied dataset and should not be interpreted as real-world financial guidance.
