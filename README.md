# Uber Trip Demand Forecasting
**Advanced Data Analytics and Machine Learning Project**

## Project Overview
This project presents an end-to-end analysis and forecasting of Uber trip demand using aggregated data released by the New York City Taxi & Limousine Commission (TLC). The objective is to identify temporal demand patterns and build robust machine learning models to predict daily trip volumes.

The workflow includes data preprocessing, exploratory data analysis (EDA), regression modeling, and ensemble learning. Model performance is evaluated using Mean Absolute Percentage Error (MAPE).

## Objectives
- Analyze historical Uber trip demand trends
- Examine the relationship between active vehicles and trip volume
- Build and compare machine learning regression models
- Improve forecasting accuracy using ensemble techniques
- Derive insights relevant to operational decision-making

## Dataset Description
- **Source:** NYC Taxi & Limousine Commission (TLC)
- **Dataset:** Uber TLC FOIL Response
- **Time Period:** January–February 2015
- **Granularity:** Daily aggregated data

### Key Variables
- `dispatching_base_number` – Uber dispatch base identifier  
- `date` – Date of aggregation  
- `active_vehicles` – Number of active vehicles  
- `trips` – Total completed trips  

## Technologies and Tools
- **Programming:** Python, SQL
- **Libraries:** Pandas, NumPy, Matplotlib, Scikit-learn
- **Environment:** Jupyter Notebook, Visual Studio Code
- **Other Tools:** Microsoft Excel

## Methodology
1. Data ingestion and preprocessing
2. Time-series exploratory data analysis
3. Model development (Random Forest, Gradient Boosting)
4. Chronological train-test split
5. Model evaluation using MAPE
6. Weighted ensemble forecasting

## Model Performance
| Model | MAPE |
|------|------|
| Random Forest | 9.61% |
| Gradient Boosting | 10.02% |
| Ensemble Model | **8.60%** |

## Key Insights
- Strong positive relationship between active vehicles and trip demand
- Ensemble learning outperformed individual models
- Weekly seasonality patterns suggest dynamic fleet allocation needs

## SQL Analysis
SQL was used to validate daily aggregation logic.

```sql
SELECT
    date,
    SUM(trips) AS total_trips
FROM uber_data
GROUP BY date
ORDER BY date;
```

## Excel Analysis
Microsoft Excel was used for supplementary validation:
- Created pivot tables to summarize daily trips
- Built line charts comparing trips versus active vehicles
- Used Excel as a secondary check for trends observed in Python

## Repository Structure
```
Uber-Trip-Analysis/
├── data/
│   └── Uber-Jan-Feb-FOIL.csv
├── notebooks/
│   └── Uber_Trip_Forecasting.ipynb
├── results/
│   └── model_comparison_plots.png
├── requirements.txt
└── README.md
```


