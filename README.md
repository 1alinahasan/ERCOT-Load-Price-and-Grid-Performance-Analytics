# Real-Time Energy Market Intelligence & Anomaly Detection for the ERCOT Grid
🚧 **Ongoing Capstone Project** 🚧

This project focuses on building a **real-time energy market intelligence platform** for the **Texas ERCOT power grid**, combining live data ingestion, short-term demand forecasting, anomaly detection, and interactive visualization. The system is designed to support proactive decision-making during periods of grid stress driven by extreme weather, renewable variability, and market volatility.

## Project Status
**Status:** In Progress  
**Timeline:** Spring 2026 Capstone  
**Program:** M.S. in Data Science, Johns Hopkins University  

## Problem Context
Texas operates a uniquely deregulated and independent electric grid through ERCOT. Grid reliability and market prices are highly sensitive to:
- Extreme weather events (heat waves, winter storms)
- High renewable energy penetration (wind and solar)
- Supply-demand imbalances
- Transmission outages

Existing tools rely heavily on historical or offline analysis and struggle to provide **real-time intelligence** during critical grid events. This project aims to address that gap.

## Project Objectives
- Build a real-time ingestion pipeline for ERCOT grid and Texas weather data  
- Develop short-term demand forecasting models (1-hour and 24-hour horizons)  
- Detect anomalous grid behavior in real time  
- Quantify potential operational and financial risk associated with anomalies  
- Design an interactive dashboard for live monitoring  
- Implement MLOps-ready, modular system components  

## System Architecture
The system is organized into three major layers:

### 1. Data Pipeline (Backend)
- Python-based ingestion microservices (Dockerized)
- Live polling of:
  - ERCOT system load, LMP prices, transmission outages
  - Texas weather data (temperature, wind, irradiance)
- Apache Kafka for real-time streaming
- TimescaleDB (PostgreSQL) for time-series storage

### 2. Data Science Core (Modeling)
**Demand Forecasting**
- Goal: Predict ERCOT load at 1-hour and 24-hour horizons
- Models:
  - XGBoost (baseline)
  - LSTM / GRU deep learning models

**Anomaly Detection**
- Goal: Identify abnormal grid and market behavior
- Models:
  - Isolation Forest
  - One-Class SVM
- Outputs real-time anomaly scores for alerting

### 3. Presentation Layer (Frontend)
- Web-based dashboard (Streamlit or React)
- Features:
  - Live vs. predicted load visualization
  - Regional grid stress indicators
  - Real-time anomaly alerts

## Data Sources
- **ERCOT API**: System-wide load, wholesale prices, outages  
- **NOAA / OpenMeteo**: Texas temperature, wind speed, solar irradiance  

## Methodology
- Real-time data ingestion and preprocessing
- Feature engineering (lags, rolling windows, calendar features)
- Model training using historical and live data
- Real-time inference and anomaly scoring
- Dashboard integration and alert testing

## Expected Outcomes
- Fully operational real-time ERCOT data pipeline
- Accurate short-term load forecasting models
- Anomaly detection engine highlighting grid stress
- Interactive monitoring dashboard
- End-to-end industry-style data science system

## Technologies Used
- Python
- SQL / TimescaleDB
- Apache Kafka
- Docker
- XGBoost
- LSTM / GRU (Deep Learning)
- Isolation Forest
- Streamlit / React
- AWS (planned deployment)

## Future Work
- Model tuning and ensemble forecasting
- Adaptive anomaly thresholds
- Region-level (zonal) ERCOT modeling
- Cloud deployment and monitoring
- Alert automation and notification systems

## Authors
**Alina Hasan**  
Sai Dinesh  

M.S. in Data Science  
Johns Hopkins University
