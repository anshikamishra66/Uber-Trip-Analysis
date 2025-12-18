# 🚕 Uber Trip Analysis  
**Advanced Data Analytics & Machine Learning Project**

---

## 📌 Project Overview
This project analyzes Uber trip data from New York City to uncover demand patterns and build machine learning–based time-series forecasting models. The goal is to predict Uber trip demand accurately and derive insights that can help optimize operations, pricing, and resource allocation in ride-hailing platforms.

---

## 🎯 Objectives
- Analyze Uber trip demand across time to identify peak hours and seasonal trends  
- Transform raw trip data into time-series format suitable for forecasting  
- Build and evaluate multiple machine learning models  
- Improve predictions using ensemble techniques  

---

## 🧾 Dataset Description
**Source:** NYC Taxi & Limousine Commission (TLC) – FOIL Response  
**Collected by:** FiveThirtyEight  

### Dataset Coverage
- 4.5+ million Uber trips (April–September 2014)  
- 14.3+ million Uber trips (January–June 2015)  

### Key Files Used
- `uber-raw-data-apr14.csv` to `uber-raw-data-sep14.csv`  
- `Uber-Jan-Feb-FOIL.csv`

### Key Columns
- `Date/Time` – Pickup date and time  
- `Lat` – Latitude of pickup  
- `Lon` – Longitude of pickup  
- `Base` – Uber base company code  

---

## 🛠 Tools & Technologies
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- XGBoost  
- Jupyter Notebook, VS Code  

---


## ▶️ How to Run
1. Clone the repository:
   git clone https://github.com/anshikamishra66/Uber-Trip-Analysis.git
2. Go into the folder:
   cd Uber-Trip-Analysis
3. Install dependencies:
   pip install -r requirements.txt
4. Run Jupyter Notebook:
   jupyter notebook

---

## 🔍 Methodology
1. Data Cleaning and Preprocessing  
2. Exploratory Data Analysis (EDA)  
3. Time-Series Transformation (Hourly Resampling)  
4. Feature Engineering using Lag Windows  
5. Model Training:
   - XGBoost  
   - Random Forest  
   - Gradient Boosted Regression Trees  
6. Model Evaluation using MAPE  
7. Ensemble Modeling  

---

## 📊 Model Performance
| Model | MAPE |
|------|------|
| XGBoost | **8.37%** |
| Random Forest | 9.61% |
| GBRT | 10.02% |
| Ensemble Model | 8.60% |

---

## 📈 Key Insights
- Strong daily and weekly seasonality in Uber demand  
- Peak demand during commuting hours  
- XGBoost performed best among all models  
- Ensemble modeling improved prediction stability  

---

## ✅ Conclusion
This project demonstrates how machine learning–based time-series forecasting can be effectively used to predict ride-hailing demand. The results highlight the importance of temporal modeling for real-world business applications.

---

## 📂 Repository Structure
Uber-Trip-Analysis/
│
├── data/
├── notebooks/
├── visuals/
├── README.md
└── requirements.txt


---

## 👤 Author
**Anshika Mishra**  
_Data Analyst | Data Science Enthusiast_




