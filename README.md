# Uber Trip Demand Forecasting  
**Advanced Data Analytics and Machine Learning Project**

---

## Project Overview
This project performs an end-to-end analysis and demand forecasting of Uber trips using aggregated data released by the New York City Taxi & Limousine Commission (TLC). The primary objective is to uncover temporal demand patterns and develop reliablSe machine learning models to predict daily trip volumes.

The workflow integrates data preprocessing, exploratory data analysis (EDA), regression modeling, and ensemble learning. By benchmarking individual models against an ensemble approach, the project demonstrates improved prediction stability and accuracy in a real-world time-series forecasting context.

---

## Objectives
- Analyze historical Uber trip demand to identify temporal and seasonal patterns  
- Examine the relationship between active vehicles and total trip volume  
- Build and compare multiple machine learning regression models  
- Improve forecasting accuracy using ensemble techniques  
- Derive insights relevant to operational and fleet management decisions  

---

## Dataset Description
The analysis uses aggregated Uber trip statistics from the **Uber TLC FOIL Response dataset**.

- **Source:** NYC Taxi & Limousine Commission (TLC)  
- **Dataset:** `Uber-Jan-Feb-FOIL.csv`  
- **Time Period:** January–February 2015  
- **Granularity:** Daily aggregated data  

### Key Variables
- `dispatching_base_number` – Identifier for the Uber dispatch base  
- `date` – Date of aggregated statistics  
- `active_vehicles` – Number of vehicles active on the platform  
- `trips` – Total completed trips per day  

---

## Technologies and Tools
- **Programming Language:** Python  
- **Data Analysis:** Pandas, NumPy  
- **Visualization:** Matplotlib, Seaborn  
- **Machine Learning:** Scikit-learn (Random Forest, Gradient Boosting)  
- **Environment:** Jupyter Notebook, Visual Studio Code  
- **Additional Tools:** Microsoft Excel, SQL  

---

## Methodology

### 1. Data Preprocessing
- Parsed date columns into datetime format  
- Aggregated data across dispatch bases to obtain city-wide demand  
- Set a datetime index to enable time-series operations  
- Verified data integrity and absence of missing values  

### 2. Exploratory Data Analysis (EDA)
- Visualized daily demand trends using line plots  
- Analyzed correlation between active vehicles and trip volume  
- Identified weekly seasonality and demand fluctuations  

### 3. Model Development
Two regression models were implemented:

- **Random Forest Regressor**  
  - Ensemble bagging method  
  - Reduces variance and overfitting  

- **Gradient Boosting Regressor**  
  - Sequential boosting approach  
  - Optimizes residual errors  

### 4. Evaluation Strategy
- Chronological train–test split (80% train, 20% test)  
- Random shuffling avoided to prevent data leakage  
- **Evaluation Metric:** Mean Absolute Percentage Error (MAPE)  

### 5. Ensemble Learning
A weighted ensemble model was constructed using inverse-error weighting of the Random Forest and Gradient Boosting predictions. This approach improved generalization and reduced forecasting error.

---

## Model Performance

| Model | MAPE | Interpretation |
|------|------|----------------|
| Random Forest | 9.61% | High accuracy, captures variance effectively |
| Gradient Boosting | 10.02% | Competitive performance, sensitive to outliers |
| **Ensemble Model** | **8.60%** | **Best performance with improved stability** |

---

## Key Insights
- A strong positive relationship exists between active vehicles and trip demand  
- Ensemble learning outperformed individual models, validating combined approaches  
- Clear weekly seasonality patterns suggest the need for dynamic fleet allocation  

---

## SQL Analysis
Example SQL query used for validating daily trip aggregation:

SELECT
    date,
    SUM(trips) AS total_trips
FROM uber_data
GROUP BY date
ORDER BY date;



## Excel Analysis

- Created a pivot table to summarize total trips per day
- Built a line chart comparing trips versus active vehicles
- Used Excel to validate demand trends observed in Python models
