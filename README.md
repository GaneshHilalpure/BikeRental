# BikeRental
Machine Learning project to predict bike rental demand using EDA, feature engineering, and regression models like Random Forest and XGBoost.

##  Overview

This project predicts daily bike rental demand (`cnt`) using environmental and seasonal data. It involves data analysis, feature engineering, and machine learning models to forecast bike usage.

##  Problem Statement

The goal is to accurately predict the number of bike rentals to help optimize resource allocation and improve urban transportation planning.

##  Dataset Features

* Season, Year, Month, Weekday
* Holiday, Working Day
* Weather Situation
* Temperature, Feeling Temperature
* Humidity, Wind Speed
* Casual & Registered Users (removed to avoid leakage)
* Target: `cnt` (total rentals)

##  Steps Performed

* Data Cleaning & Preprocessing  
* Exploratory Data Analysis (EDA)  
* Feature Engineering (lag features, rolling mean, cyclical encoding)  
* Handling Missing Values  
* Time-Series Aware Train-Test Split  
* Model Building (Ridge, Lasso, Random Forest, Gradient Boosting, XGBoost)  
* Hyperparameter Tuning using TimeSeriesSplit  
* Model Evaluation  

##  Results

* Best Model: **Ridge Regression (α = 10)**  
* RMSE: **1447.78**  
* MAE: **1143.12**  
* R² Score: **0.3430**  

* Moderate performance due to dataset size and variability in demand  

##  Technologies Used

* Python  
* Pandas, NumPy  
* Scikit-learn  
* Matplotlib, Seaborn  
* XGBoost  
* Joblib  

##  Dataset

The dataset used in this project is available here:  
https://d3ilbtxij3aepc.cloudfront.net/projects/CDS-Capstone-Projects/PRCP-1018-BikeRental.zip

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook PRCP-1018-BikeRental_Notebook.ipynb

## Future Improvements
* Add external data (weather forecasts, events, holidays)
* Use advanced time-series models (ARIMA, SARIMA, LSTM, Prophet)
* Perform advanced hyperparameter tuning (Optuna)
* Deploy model using Flask API
* Build real-time prediction system
