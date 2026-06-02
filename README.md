# Ashrae-Energy-Prediction
# Energy Consumption Prediction & Building Efficiency Analysis

## Overview

This project is an end-to-end machine learning system designed to predict building energy consumption and analyze building efficiency using historical energy usage, weather conditions, and building metadata.

The system processes large-scale building energy data and generates actionable insights such as:

* Energy consumption prediction
* Building efficiency scoring
* Waste pattern detection
* Savings estimation
* Retrofit prioritization

The project uses machine learning to transform raw energy readings into meaningful business intelligence for energy management and sustainability.

---

## Problem Statement

Buildings contribute significantly to global energy consumption, yet many facilities struggle to identify inefficiencies and predict future energy demand.

Without reliable prediction systems:

* Energy waste remains undetected
* High-consumption buildings are difficult to identify
* Retrofit decisions lack data-driven support
* Nighttime and off-hour overconsumption often goes unnoticed

This project addresses these issues through predictive analytics and efficiency benchmarking.

---

## Features

### Energy Consumption Prediction

* Predicts hourly energy usage for buildings
* Supports multiple energy meter types:

  * Electricity
  * Chilled Water
  * Steam
  * Hot Water

### Feature Engineering

Creates 60+ engineered features including:

* Temporal features (hour, weekday, seasonality)
* Weather features (temperature, humidity, cooling/heating degree days)
* Building characteristics (age, size, floor count)
* Interaction features

### Building Efficiency Analysis

* Generates efficiency scores (0–100)
* Benchmarks buildings against similar peers
* Identifies inefficient buildings

### Waste Pattern Detection

Detects:

* Excessive weekend energy usage
* High nighttime consumption
* High baseline energy loads

### Savings Estimation

* Estimates energy savings potential
* Calculates possible annual cost reductions
* Prioritizes buildings for retrofit investment

---

## Dataset

The project uses the **ASHRAE Great Energy Predictor III Dataset** from Kaggle.

Dataset includes:

* **20M+ hourly energy readings**
* **1,449 buildings**
* **Weather data**
* **Building metadata**

### Data Sources

* `train.csv` → Meter readings
* `building_metadata.csv` → Building details
* `weather_train.csv` → Weather conditions

---

## Machine Learning Approach

The project follows a **three-stage pipeline**:

### 1. Data Exploration & Feature Engineering

* Data cleaning
* Missing value handling
* Outlier removal
* Feature generation

### 2. Predictive Modeling

Trains separate **LightGBM models** for each meter type.

Techniques used:

* Log transformation
* Time-based validation
* Bias correction
* Early stopping
* Feature selection

### 3. Building Diagnostics

* Efficiency benchmarking
* Waste detection
* Savings quantification
* Priority building recommendations

---

## Tech Stack

**Programming Language**

* Python

**Libraries**

* Pandas
* NumPy
* Scikit-learn
* LightGBM
* Matplotlib
* Seaborn

**Environment**

* Jupyter Notebook

---

## Project Structure

```bash
├── data/
│   ├── train.csv
│   ├── weather_train.csv
│   └── building_metadata.csv
│
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_modeling.ipynb
│   └── 03_building_diagnostics.ipynb
│
├── models/
│   └── trained_models.pkl
│
├── outputs/
│   ├── validation_predictions.csv
│   ├── building_efficiency_scores.csv
│   └── priority_buildings.csv
│
└── README.md
```

---

## Results

The system:

* Processed **20M+ rows of energy data**
* Generated efficiency scores for **1,442 buildings**
* Detected major operational inefficiencies
* Estimated **multi-million dollar annual savings potential**

Example insights:

* Buildings with excessive nighttime usage
* HVAC scheduling inefficiencies
* High baseline consumption patterns

---

## Future Improvements

* Deep Learning models (LSTM, Transformers)
* Real-time monitoring dashboard
* Anomaly detection system
* Carbon emissions tracking
* ROI calculator for retrofits
* Integration with Building Management Systems (BMS)

---

## Applications

* Smart Buildings
* Energy Management Systems
* Sustainability Analytics
* Climate Tech
* Commercial Facility Optimization

---

## Contributors

* Diya Bhutani
* Manasvi Arora

---

## License

This project is intended for educational and research purposes.
