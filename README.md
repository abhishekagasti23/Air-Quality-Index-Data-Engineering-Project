# Capstone---Air-Quality-Index              


# Air Quality Index Forecasting – End-to-End Azure Data Engineering Project

## 📌 Project Overview
This project demonstrates a complete end-to-end **Azure-based Data Engineering and Analytics pipeline** for processing and forecasting Air Quality Index (AQI) data across 28+ Indian cities using the **Medallion Architecture (Bronze, Silver, Gold)**.

The solution ingests raw environmental data, performs scalable transformations using Apache Spark on Databricks, stores optimized datasets in Delta Lake, and enables analytical reporting and forecasting using Power BI and time series models.

---

## 🏗️ Architecture

**Medallion Architecture:**
- **Bronze Layer** – Raw ingestion from Azure Blob Storage  
- **Silver Layer** – Cleaned, validated, and standardized datasets  
- **Gold Layer** – Aggregated, analytics-ready and forecast-ready data  

**Tech Stack:**
- Azure Data Lake / Blob Storage  
- Azure Databricks (PySpark)  
- Delta Lake  
- Azure Data Factory  
- Power BI  
- Python (ARIMA, SARIMA, SARIMAX, Prophet)

---

## 📊 Dataset

- Source: Indian city-wise AQI historical data  
- Records: 10M+  
- Cities: 28+  
- Granularity: Daily city-level AQI and pollutant measures  

---

## 🔄 Data Pipeline

### 1️⃣ Bronze → Silver
Notebook: `bronze_to_silver.ipynb`
- Data cleansing and null handling
- Schema enforcement
- Type casting and normalization
- Duplicate removal
- Partitioning by year

### 2️⃣ Silver → Gold
Notebook: `Silver_to_Gold.ipynb`
- Aggregations by city, month, and year
- Feature engineering for forecasting
- Delta format optimization
- Final analytical tables

---

## 📈 Forecasting Models

The following models were implemented and evaluated:

| Model     | Use Case |
|-----------|----------|
| ARIMA     | Baseline univariate forecasting |
| SARIMA    | Seasonal AQI patterns |
| SARIMAX   | Multivariate forecasting with exogenous variables |
| Prophet   | Trend & seasonality modeling |

**Evaluation Metrics:**
- MAE
- RMSE

---

## 📊 Power BI Dashboard

File: `Air Quality Index Dashboard.pbix`

Visualizations include:
- City-wise AQI trends
- Pollutant distribution
- Seasonal variation analysis
- Forecast vs actual AQI
- High pollution alerts

---

## 🔐 Security & Best Practices

- No credentials hardcoded in notebooks  
- Secrets managed via environment variables / Azure Key Vault  
- GitHub Secret Scanning compliant  
- Clean Git history with no sensitive data  

---

## 🚀 How to Run This Project

### Prerequisites
- Azure Account
- Databricks Workspace
- Python 3.8+
- Power BI Desktop

### Steps
1. Upload raw AQI dataset to Azure Blob Storage
2. Configure Databricks cluster
3. Run `bronze_to_silver.ipynb`
4. Run `Silver_to_Gold.ipynb`
5. Open Power BI dashboard and connect to Gold layer

---

## 📌 Future Enhancements

- Real-time AQI streaming with Kafka
- Azure Synapse integration
- CI/CD pipeline for Databricks notebooks
- ML-based forecasting (XGBoost, LSTM)
- API for AQI predictions

---

## 👨‍💻 Author

**Abhishek Agasti**  
MBA (Advanced Construction Management) – NICMAR  
PG Diploma in Data Engineering – IIT Jodhpur  
Project Sales Engineer – Asian Paints  

🔗 LinkedIn: https://www.linkedin.com/in/abhishekagasti  
📧 Email: (optional)

---

## ⭐ If you found this project useful, give it a star!
