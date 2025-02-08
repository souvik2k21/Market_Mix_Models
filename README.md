# Market Mix Modeling (MMM) Project

## Overview
The Market Mix Modeling (MMM) project aims to analyze and quantify the impact of various marketing inputs such as promotions, pricing, and distribution on sales and revenue. By leveraging machine learning models, this project helps businesses optimize marketing spend and improve overall Return on Investment (ROI).

## Objectives
- Understand the influence of marketing activities on sales performance.
- Identify key drivers of sales and revenue.
- Optimize marketing spend for maximum impact.
- Build predictive models to forecast sales based on historical data.

## Data Sources
- **Sales Data:** Includes historical sales volume, sales value, and product pricing.
- **Distribution Data:** Covers product availability and distribution channels.
- **Media Data:** Tracks advertising spend, promotions, and discounts.
- **Shipment Data:** Provides insights into product stock levels and availability.

## Methodology
### 1. Data Preprocessing
- Cleaned column names for consistency.
- Handled missing data using imputation techniques.
- Standardized data for uniform scale and format.

### 2. Feature Engineering
- Extracted time-based features (lagged sales, seasonal trends).
- Created price-related metrics (price elasticity, average price per unit).
- Engineered promotional indicators to measure marketing impact.
- Evaluated the effect of distribution and availability on sales.

### 3. Exploratory Data Analysis (EDA)
- Visualized sales trends, price sensitivity, and promotional impact.
- Used histograms, scatter plots, and line charts for insights.
- Identified seasonality patterns in sales data.

### 4. Modeling
- **Data Split:** 80% training, 20% testing.
- **Models Used:**
  - Linear Regression
  - Lasso Regression
  - Ridge Regression
  - Random Forest
  - XGBoost
- **Evaluation Metrics:**
  - R² Score
  - Mean Absolute Percentage Error (MAPE)
  - Mean Squared Error (MSE)

### 5. Model Performance
| Model | Target Variable | Best Model | MAPE (%) | R² |
|--------|----------------|------------|----------|-----|
| Model 1 | Sales_Value_Brand | Lasso Regression | 3.04 | 0.828 |
| Model 2 | Sales_Value_V1 | Lasso Regression | 3.44 | 0.849 |
| Model 3 | Sales_Value_V2 | Linear Regression | 2.42 | 0.787 |
| Model 4 | Sales_Value_V3 | Linear Regression | 4.59 | 0.896 |

- Tree-based models (Random Forest and XGBoost) underperformed due to data characteristics.

## Challenges & Solutions
### 1. Data Quality Issues
- **Problem:** Missing values and inconsistent column names.
- **Solution:** Cleaned and imputed missing data.

### 2. Multicollinearity
- **Problem:** High correlation between features affected linear model performance.
- **Solution:** Used Lasso and Ridge Regression to reduce collinearity effects.

### 3. Seasonality & Trends
- **Problem:** Sales exhibited strong seasonal patterns.
- **Solution:** Included lag features to account for seasonality.

### 4. Model Selection
- **Problem:** Identifying the best model for prediction.
- **Solution:** Used cross-validation and selected models with the best MAPE and R² scores.

## Tools & Technologies
- **Programming Languages:** Python (Pandas, NumPy, Scikit-Learn, XGBoost, Seaborn, Matplotlib)
- **Data Handling:** Pandas and NumPy
- **Visualization:** Matplotlib, Seaborn
- **Storage:** CSV files for structured data storage

## Outcomes & Business Impact
1. **Model Accuracy:**
   - R² scores ranged from **0.648 to 0.945**, indicating strong explanatory power.
   - MAPE values remained below **7%**, ensuring reliable sales forecasts.
2. **Insights:**
   - Price remained one of the strongest predictors of sales.
   - Promotions significantly boosted short-term sales.
   - Product availability and stock levels influenced overall sales performance.
3. **Deployment:**
   - The best-performing models were integrated into an API for real-time sales forecasts.
   - The project provided actionable insights for optimizing marketing budgets.

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Market_Mix_Modeling.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook:
   ```bash
   jupyter notebook Market_Mix_Model_Project.ipynb
   ```

## Files in Repository
- **Market_Mix_Model_Project.ipynb** - Jupyter Notebook with full implementation.
- **Sales_Data.xlsx** - Sales data used for modeling.
- **Media_Data.xlsx** - Marketing data for analysis.
- **README.md** - Project documentation.


