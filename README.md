# Urban Mobility Analytics Data Platform  
### Scalable Demand Forecasting for NYC Taxi Operations

Predicting cab demand across New York City using a structured, production-ready data engineering pipeline. This platform processes large-scale NYC taxi trip records to forecast ride demand across future time intervals, enabling data-driven fleet optimization and operational planning.

---

## Project Overview

The Urban Mobility Analytics Data Platform ingests raw NYC taxi trip data, transforms it through structured ETL workflows, engineers time-series and geo-spatial features, and trains predictive models to forecast demand.

The project follows a modular, reproducible architecture inspired by enterprise data engineering practices.

---

## Key Features

- Processes **10M+ NYC taxi trip records**
- Layered data architecture: **raw → interim → processed**
- Automated ETL & feature engineering workflows
- Time-window and location-based aggregation
- Forecasting models achieving **~89% prediction accuracy**
- Reproducible environment using Makefile + modular Python structure
- Structured reporting and visualization layer

---

## Architecture
Raw Data
↓
Data Cleaning & Validation
↓
Feature Engineering
↓
Model Training
↓
Demand Forecasting
↓
Visualization & Reporting


### Data Layers

- **Raw Layer** – Immutable original trip data  
- **Interim Layer** – Cleaned and transformed intermediate datasets  
- **Processed Layer** – Final modeling-ready datasets  

This ensures:
- Reproducibility  
- Clear separation of pipeline stages  
- Maintainable analytics workflows  

---

## Project Structure


├── data
│ ├── raw # Original trip data
│ ├── interim # Cleaned & transformed data
│ └── processed # Modeling-ready datasets
│
├── src
│ ├── data # Data ingestion scripts
│ ├── features # Feature engineering workflows
│ ├── models # Model training & prediction
│ └── visualization # Analytical visualizations
│
├── models # Serialized trained models
├── reports # Generated reports & figures
├── notebooks # EDA and validation notebooks
├── Makefile # Automation commands
└── requirements.txt # Project dependencies


---

## Modeling Approach

- Time-based aggregation (hourly / interval forecasting)
- Geo-spatial demand clustering
- Temporal feature engineering (lags, rolling averages)
- Models used:
  - XGBoost
  - Random Forest
  - Logistic Regression

### Performance

- **~89% forecast accuracy**
- Reduced data preparation time by **30%** through automated workflows

---

## Setup & Usage

### Install Dependencies

```bash
pip install -r requirements.txt
Run Data Pipeline
make data
Train Model
make train
Generate Predictions
make predict

Business Impact

This platform enables:

Smarter fleet allocation

Surge demand anticipation

Peak-hour capacity planning

Reduced idle vehicle time

Data-driven mobility strategy

Future Enhancements

Distributed processing with Apache Spark

Workflow orchestration using Airflow

Cloud warehouse integration (Snowflake / BigQuery)

Real-time streaming with Kafka

REST API for demand serving

🛠 Tech Stack

Python | Pandas | Scikit-learn | XGBoost | Matplotlib | Seaborn | Modular ETL | Makefile Automation
