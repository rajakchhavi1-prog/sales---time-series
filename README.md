# 📈 Retail Sales Demand Forecasting using Time Series Models

This project focuses on forecasting retail store sales using time series techniques and evaluating different forecasting models to identify the most accurate approach.

The analysis is conducted using the Rossmann Store Sales dataset, which contains daily sales data along with promotional and store-level features.

The project compares statistical and machine learning approaches to understand demand patterns and the impact of promotions on sales.

---

# 🎯 Project Objectives

The primary goals of this project are:

- Forecast daily retail sales using time series models
- Compare forecasting performance across different models
- Analyze seasonality patterns in sales
- Evaluate the impact of promotions on demand
- Provide business insights for inventory and promotion planning

---

# 📊 Dataset

Dataset used: Rossmann Store Sales (Kaggle)

The dataset contains:

| Feature | Description |
|------|------|
| Store | Unique store ID |
| Date | Date of observation |
| Sales | Daily sales revenue |
| Customers | Number of customers |
| Open | Store open/closed indicator |
| Promo | Promotion indicator |
| StateHoliday | State holiday indicator |
| SchoolHoliday | School holiday indicator |
| StoreType | Type of store |
| Assortment | Assortment level |
| CompetitionDistance | Distance to competitor store |

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Statsmodels
- Prophet
- Scikit-learn

---

# 📌 Methodology

The project follows a structured time series forecasting pipeline:

### 1. Data Preprocessing
- Merged sales and store datasets
- Converted date column to datetime format
- Selected store-level data for modeling
- Performed time-based train-test split (80%-20%)

---

### 2. Time Series Modeling

Four forecasting models were implemented:

**ARIMA**

- Classical statistical time series model
- Captures autoregressive and moving average components

**ARIMAX**

- Extension of ARIMA
- Includes promotion variable as an external regressor

**Prophet**

- Handles trend and seasonality automatically
- Designed for business forecasting problems

**Prophet + Promotion Regressor**

- Prophet model extended with promotion variable
- Allows forecasting with external drivers of demand

---

# 📊 Model Performance

Model performance was evaluated using:

- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)

| Model | MAE | RMSE |
|------|------|------|
| ARIMA | 1299 | 1926 |
| ARIMAX | 1571 | 2119 |
| Prophet | 701 | 1084 |
| Prophet + Promo | **558** | **953** |

### Best Model
Prophet with Promotion Regressor achieved the lowest forecasting error.

---

# 📈 Seasonality Analysis

Weekly seasonality was analyzed by examining average sales by weekday.

Key observation:

- Sales patterns vary significantly across weekdays.
- Demand patterns suggest strong seasonal purchasing behavior.

---

# 💰 Promotion Impact Analysis

Promotion effects were analyzed by comparing sales during promotional and non-promotional periods.

| Condition | Average Sales |
|------|------|
| No Promotion | ~3199 |
| Promotion | ~5153 |

### Promotion Uplift

Sales increase by approximately **61% during promotions**.

This demonstrates the strong influence of promotional campaigns on demand.

---

# 📌 Key Insights

- Retail sales exhibit strong seasonal patterns
- Promotional campaigns significantly increase demand
- Incorporating external variables improves forecasting performance
- Prophet models are effective for business time series forecasting

---

# 💡 Business Recommendations

- Use Prophet + Promotion model for demand forecasting
- Increase inventory planning during promotional periods
- Use promotion uplift estimates to optimize marketing strategy

---

# 📂 Project Structure
retail-demand-forecasting
│
├── data
│ ├── train.csv
│ └── store.csv
│
├── notebook
│ └── demand_forecasting.ipynb
│
├── plots
│ ├── seasonality.png
│ ├── forecast.png
│
└── README.md


---

# 🚀 Future Improvements

Potential extensions of this project:

- SARIMA seasonal modeling
- Hyperparameter optimization
- Multi-store forecasting
- Hierarchical forecasting across regions
- Deep learning models (LSTM)

---

