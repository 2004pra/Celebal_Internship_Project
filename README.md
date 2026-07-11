# ⚡ Smart Meter Energy Analytics Pipeline

An end-to-end Data Engineering project built using **Databricks**, **PySpark**, and **Delta Lake** following the **Medallion Architecture (Bronze → Silver → Gold)**.

## 📌 Project Overview

This project processes smart meter electricity consumption data and transforms raw CSV files into business-ready analytics tables.

The pipeline performs:

- Raw data ingestion
- Data cleaning and validation
- Feature engineering
- Anomaly detection
- Business aggregations
- Billing summary generation
- 7-Day Simple Moving Average (SMA) forecasting
- Data visualization using Matplotlib

---

# 🏗 Architecture

```
meter_readings.csv
household_info.csv
        │
        ▼
Bronze Layer
(Raw Data)
        │
        ▼
Silver Layer
(Data Cleaning + Feature Engineering + Anomaly Detection)
        │
        ▼
Gold Layer
(Business Ready Tables + Forecast Dataset)
        │
        ▼
Matplotlib Visualizations
```

---

# 🛠 Tech Stack

- Python
- PySpark
- Spark SQL
- Databricks Community Edition
- Delta Lake
- Pandas
- Matplotlib

---

# 📂 Dataset

The project uses two CSV files.

### meter_readings.csv

Contains:

- meter_id
- household_id
- timestamp
- units_consumed

### household_info.csv

Contains:

- household_id
- city
- house_type
- avg_daily_consumption

---

# 📂 Repository Structure

```
smart-meter-energy-analytics-pipeline
│
├── notebooks
│   ├── 01_bronze_layer.ipynb
│   ├── 02_silver_layer.ipynb
│   ├── 03_gold_layer.ipynb
│   └── 04_visualization.ipynb
│
├── output_images
│
├── data
│   └── sample_data
│
├── docs
│   ├── Project_Problem_Statement.pdf
│   └── Project_Architecture.pdf
│
├── requirements.txt
│
└── README.md
```

---

# 🥉 Bronze Layer

The Bronze layer ingests the raw CSV files into Delta tables.

Operations performed:

- CSV ingestion
- Schema inference
- Ingestion timestamp
- Ingestion date
- Delta table creation
- Data partitioning

Output Table:

```
bronze.meter_readings
```

---

# 🥈 Silver Layer

The Silver layer cleans and enriches the data.

Operations performed:

- Timestamp conversion
- Null value handling
- Duplicate verification
- Household data join
- Rolling average calculation
- Meter statistics generation
- Anomaly detection

Output Table:

```
silver.meter_readings
```

---

# 🥇 Gold Layer

The Gold layer contains business-ready analytical tables.

Generated tables:

- daily_consumption
- monthly_consumption
- city_consumption
- house_type_consumption
- anomaly_summary
- billing_summary
- forecast_data

---

# 📈 Forecasting

The project prepares a forecasting dataset using a **7-Day Simple Moving Average (SMA)** to analyze short-term electricity consumption trends.

---

# 📊 Visualizations

The visualization notebook generates:

- Daily Consumption Trend
- Monthly Consumption
- City-wise Consumption
- House Type Distribution
- Anomaly Summary
- 7-Day SMA Forecast Trend

Sample outputs are available inside the **output_images** folder.

---

# 🚀 How to Run

## 1. Create a Databricks Community Edition Workspace

## 2. Create a Catalog

```
smart_meter_project_catalog
```

## 3. Create a Volume

```
meter_problem_project_volume
```

## 4. Upload the datasets

- meter_readings.csv
- household_info.csv

## 5. Run the notebooks in order

```
01_bronze_layer.ipynb

↓

02_silver_layer.ipynb

↓

03_gold_layer.ipynb

↓

04_visualization.ipynb
```

---

# 📄 Project Documents

The **docs** folder contains the supporting documents used during the project.

Documents include:

- Project Problem Statement
- Project Architecture

These documents describe the project objectives, requirements, and overall pipeline design.

---

# 💡 Skills Demonstrated

- PySpark DataFrames
- Spark SQL
- Delta Lake
- Medallion Architecture
- Window Functions
- Data Cleaning
- Feature Engineering
- Anomaly Detection
- Business Aggregation
- Time-Series Analysis
- Simple Moving Average (SMA)
- Data Visualization

---

# 🔮 Future Improvements

- Apache Kafka Integration
- Spark Structured Streaming
- Apache Airflow Orchestration
- Power BI Dashboard
- Spark ML Forecasting
- Azure Databricks Deployment

---

# 👨‍💻 Author

**Prashant Mishra**

Data Engineering Internship Project

Celebal Technologies
