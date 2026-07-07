# 🚖 NYC Taxi Trip Duration Prediction

An end-to-end machine learning project that predicts taxi trip durations in New York City using historical trip data. The project leverages feature engineering, exploratory data analysis (EDA), geographic clustering, and gradient boosting to build an accurate regression model.

## Overview

The objective is to predict the duration of taxi trips using features such as pickup and dropoff locations, timestamps, passenger count, and routing information. This project demonstrates a complete machine learning workflow—from data preprocessing and feature engineering to model training and evaluation.

---

## Dataset

This project uses the **NYC Taxi Trip Duration** dataset from Kaggle.

**Target Variable**
- `trip_duration`

**Key Features**
- Pickup & Dropoff Coordinates
- Pickup Date & Time
- Passenger Count
- Vendor ID
- Store & Forward Flag
- OSRM Route Features

> **Note:** The dataset is not included in this repository due to Kaggle's competition terms.

---

## Project Workflow

### 1. Data Preprocessing
- Removed invalid coordinate outliers
- Filtered trips outside NYC boundaries
- Handled missing values and anomalies
- Cleaned inconsistent passenger counts

### 2. Exploratory Data Analysis (EDA)
- Trip duration distribution
- Temporal analysis
- Geographic visualization
- Vendor comparison
- Passenger count analysis
- Average speed analysis

### 3. Feature Engineering

#### Temporal Features
- Hour
- Day of Week
- Day of Month
- Month

#### Geographic Features
- Haversine Distance
- Manhattan Distance
- Bearing (Direction)
- Pickup & Dropoff Clusters (MiniBatch K-Means)

#### Route Features
- OSRM Route Distance
- OSRM Estimated Travel Time
- Number of Route Steps

#### Encoding
- One-Hot Encoding for categorical variables

---

## Model

The project uses **XGBoost Regressor** for trip duration prediction.

### Training Pipeline

- Train/Validation Split (80/20)
- Hyperparameter Tuning
- Feature Importance Analysis
- Prediction Generation

### Evaluation Metric

- Root Mean Squared Error (RMSE)

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib
- Seaborn

---

## Repository Structure

```
NYC-Taxi-Trip-Duration/
│
├── notebooks/
│   └── NYC_Taxi_Trip_Duration.ipynb
│
├── images/
│
├── README.md
└── requirements.txt
```

---

## Results

The model combines temporal, geographic, and routing features to accurately estimate taxi trip durations.

The most important features include:
- Haversine Distance
- Manhattan Distance
- Pickup Hour
- Geographic Clusters
- OSRM Route Features

---

## Future Improvements

- Hyperparameter optimization using Optuna
- Ensemble learning (XGBoost + Random Forest + LightGBM)
- Cross-validation
- Feature selection
- Deep learning approaches
- Traffic and weather data integration

---

## Installation

Clone the repository

```bash
git clone https://github.com/<your-username>/NYC-Taxi-Trip-Duration.git
```

Install dependencies

```bash
pip install -r requirements.txt
```

Run the notebook

```bash
jupyter notebook
```

or open the notebook in **Kaggle**.

---

## Acknowledgements

- Kaggle — NYC Taxi Trip Duration Competition
- XGBoost
- Scikit-learn
