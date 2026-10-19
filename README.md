# Walmart Sales Analysis and Forecasting

## Project Overview
This project analyzes historical Walmart weekly sales data for 45 stores using Python. It explores sales trends, seasonal patterns, store performance, and relationships between weekly sales and economic or environmental factors. It also compares forecasting models and predicts sales for the next 12 weeks for each store.

## Business Objectives
- Analyze historical weekly sales and identify seasonal trends.
- Compare holiday and non-holiday sales.
- Examine relationships between sales, temperature, fuel prices, CPI, and unemployment.
- Identify the best- and worst-performing stores.
- Compare forecasting models using MAE and RMSE.
- Generate 12-week forecasts for all 45 stores.

## Dataset
- **Records:** 6,435
- **Stores:** 45
- **Period:** February 2010 to October 2012
- **Features:** Store, Date, Weekly_Sales, Holiday_Flag, Temperature, Fuel_Price, CPI, Unemployment

## Tools and Technologies
- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Statsmodels
- Google Colab and Jupyter Notebook

## Project Workflow
1. Data loading, cleaning, and validation
2. Exploratory data analysis (EDA)
3. Outlier analysis and statistical testing
4. Store performance analysis
5. Forecasting model comparison
6. Forecast generation and validation
7. Business recommendations

## Key Findings
- December had the highest average weekly sales among the months analyzed.
- Average weekly sales were approximately 7.84% higher during holiday weeks than non-holiday weeks.
- Store 20 had the highest average weekly sales, while Store 33 had the lowest.
- The difference in average weekly sales between these stores was approximately 1.85 million.
- Across the 45 stores, Holt-Winters had a lower average RMSE than the seasonal-naive baseline in the 12-week holdout evaluation.

## Forecasting Results
The selected forecasting models generated 12-week forecasts for all 45 stores, covering November 2, 2012, through January 18, 2013.

| Model | Average MAE | Average RMSE |
|---|---:|---:|
| Seasonal Naive | 53,768.95 | 64,054.53 |
| Holt-Winters | 43,821.30 | 53,110.11 |

The model selected for each store was based on its RMSE on the 12-week holdout period.

## Output Files

### Main Analysis Notebook
- `Walmart_Capstone_Project.ipynb` — main analysis, exploratory data analysis, statistical testing, store performance, and forecasting for all 45 stores.
- `Walmart_Capstone_Project_ARIMA_Revision.ipynb` — additional ARIMA time-series forecasting and evaluation for five selected stores.

### Sales and Business Analysis
- `walmart_year_month_sales_analysis.csv` — sales analysis by year and month.
- `walmart_monthly_seasonality_analysis.csv` — monthly sales patterns and seasonal analysis.
- `walmart_holiday_sales_summary.csv` — holiday versus non-holiday sales summary.
- `walmart_store_unemployment_analysis.csv` — store-level unemployment and sales relationship analysis.
- `walmart_store_performance.csv` — store performance metrics and rankings.

### Forecasting Results
- `walmart_12_week_forecasts.csv` — 12-week forecasts for all 45 stores.
- `walmart_forecast_summary.csv` — summarized forecast results by store.
- `walmart_model_evaluation.csv` — evaluation metrics for the forecasting models used across all stores.
- `walmart_arima_12_week_forecasts.csv` — 12-week ARIMA forecasts for Stores 1, 5, 10, 20, and 33.
- `walmart_arima_model_evaluation.csv` — ARIMA evaluation metrics for the five selected stores.

The all-store forecasting workflow compares Seasonal Naive and Holt-Winters models using a 12-week holdout evaluation. The additional ARIMA workflow evaluates five selected stores using MAE and RMSE before generating their 12-week forecasts.

## How to Run
1. Open the notebook in Google Colab.
2. Upload the Walmart dataset or update the file path to match your environment.
3. Run the cells from beginning to end.
4. Review the analysis, visualizations, model evaluation, and forecast outputs.

## Limitations
This project uses historical data from 2010–2012. Correlations do not establish causation, and model evaluation uses a single 12-week holdout period per store. Forecasts are estimates and should not be interpreted as guaranteed future sales.

## Conclusion
This project demonstrates how exploratory data analysis, statistical testing, store performance comparisons, and time-series forecasting can provide useful insights for retail planning and data-driven decision-making.













