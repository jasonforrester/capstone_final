# Capstone Project: The Impact of Federal Reserve Interest Rate Policy on Unemployment

## Project Overview
This project analyzes how the Federal Reserve's interest rate policies affect unemployment rates. Using historical economic data, we apply machine learning techniques to model the relationship between interest rate adjustments and labor market conditions. By leveraging predictive modeling and statistical analysis, we aim to provide insights into how monetary policy decisions shape employment trends and economic stability.

## Problem Statement
The Federal Reserve uses interest rate changes as a tool to control inflation and ensure economic stability. However, the direct and indirect impacts of these changes on employment levels remain complex and multifaceted. This project aims to provide a data-driven analysis to understand the correlation between monetary policy and unemployment trends, helping policymakers and businesses make informed decisions.

### Key Questions Addressed:
- How do changes in interest rates correlate with unemployment rates over time?
- Is there a measurable lag between rate adjustments and job market shifts?
- What macroeconomic factors influence the strength of this relationship?
- Can we build a predictive model to anticipate unemployment changes based on interest rate policies?

## Data Sources
To conduct this analysis, we sourced data from multiple reputable financial and labor market sources:
- **Federal Reserve Economic Data (FRED)**: Historical interest rate data and macroeconomic indicators.
- **Bureau of Labor Statistics (BLS)**: Unemployment rate trends and employment sector breakdowns.
- **World Bank & IMF Economic Reports**: Global interest rate policies and economic comparisons.
- **Additional Macroeconomic Indicators**: Inflation rates, GDP growth, stock market trends, and consumer confidence indices.

## Key Takeaways
- Interest rate changes have a **6-12 month lag effect** on unemployment.
- GDP and inflation significantly influence unemployment trends.
- Predictive models can forecast unemployment **6 months in advance** with high accuracy.
- More aggressive interest rate hikes correlate with higher unemployment, though sectoral effects vary.
- Policymakers should consider economic lag effects when adjusting interest rates.

## Methodology
Our approach follows the CRISP-DM framework for structured data analysis and model development.

1. **Data Collection & Cleaning**
   - Aggregated data from multiple sources into a unified dataset.
   - Handled missing values using imputation techniques.
   - Removed outliers using statistical thresholding.

2. **Exploratory Data Analysis (EDA)**
   - Visualized historical trends of interest rates and unemployment.
   - Examined correlation matrices to identify key relationships.
   - Identified economic cycles and recession periods.

3. **Feature Engineering**
   - Created lag variables for interest rates to capture delayed effects.
   - Incorporated economic indicators such as inflation, GDP growth, and stock market trends.
   - Constructed categorical indicators for major economic events (e.g., financial crises, policy shifts).

4. **Machine Learning Models**
   - **Regression models** (Linear Regression, Random Forest, Lasso, Ridge) to predict unemployment trends.
   - **Time Series Analysis** using ARIMA and LSTM models.
   - **SHAP Analysis** to evaluate feature importance.
   - **Cross-validation** to assess model performance and generalization.

5. **Model Evaluation**
   - Compared models using **Root Mean Squared Error (RMSE)**, **Mean Absolute Error (MAE)**, and **R-squared**.
   - Assessed residual plots to check for bias in predictions.
   - Conducted economic scenario simulations to test model robustness.

## How to Run This Notebook
1. Clone this repository:
   ```sh
   git clone <repo-link>
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Open and run the notebook in JupyterLab or Google Colab.

## Limitations & Assumptions
- The dataset primarily focuses on U.S. economic indicators.
- The model assumes a **linear relationship** between interest rates and unemployment.
- Unemployment trends may also be influenced by **external shocks (e.g., pandemics, policy changes)** not included in this dataset.

## Next Steps
- **Enhancing Model Accuracy**: Incorporate additional macroeconomic variables such as consumer spending trends and wage growth.
- **Causal Inference Analysis**: Use econometric techniques to establish causation rather than correlation.
- **Interactive Dashboard**: Develop a user-friendly dashboard for real-time unemployment forecasting and policy impact simulations.

## Data Dictionary
| Column Name           | Description                                      |
|----------------------|--------------------------------------------------|
| Date                | Date of the record (YYYY-MM-DD)                   |
| Unemployment_Rate   | Monthly U.S. unemployment rate (%)                |
| Interest_Rate       | Federal Reserve Interest Rate (%)                 |
| GDP_Growth         | Quarterly GDP growth rate (%)                      |
| Inflation          | Yearly inflation rate (%)                          |
| Retail_Sales       | Total retail sales (in billions)                   |
| Consumer_Spending  | Total personal consumer spending ($)               |
| PC1                | First principal component from PCA analysis        |
| PC2                | Second principal component from PCA analysis       |
| Cluster            | Cluster assignment from KMeans analysis            |

## Repository Structure
```
/Capstone_Project
│── README.md  # Project overview and findings
│── notebooks/
│   ├── unemployment_analysis_perfect.ipynb  # Final Jupyter Notebook
│── data/
│   ├── raw/  # Original datasets
│   │   ├── federal_reserve_rates.csv
│   │   ├── bls_unemployment.csv
│   │   ├── gdp_growth.csv
│   │   ├── inflation_rates.csv
│   │   ├── retail_sales.csv
│   │   ├── consumer_spending.csv
│   ├── processed/  # Cleaned and feature-engineered datasets
│   ├── expanded_economic_data_perfect.csv  # Final dataset used in modeling
│── images/  # Data visualizations and SHAP analysis results
```

## Authors
Jason Forrester

