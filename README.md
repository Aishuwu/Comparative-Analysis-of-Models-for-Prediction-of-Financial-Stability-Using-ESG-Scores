# Comparative Analysis of Models for Predicting Financial Stability Using ESG Scores

## Introduction

This project presents a machine learning framework for predicting corporate financial stability by integrating traditional financial metrics with Environmental, Social, and Governance (ESG) scores. The analysis evaluates multiple regression models and identifies the most effective one for deployment via a FastAPI-based API. The system is designed for real-time financial risk assessment and decision support.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Configuration](#configuration)
- [Data Overview](#data-overview)
- [Modeling Approach](#modeling-approach)
- [Deployment](#deployment)
- [Results Summary](#results-summary)
- [Troubleshooting](#troubleshooting)
- [License](#license)

## Features

- Predictive modeling of financial stability using both financial and ESG data.
- Evaluation of multiple machine learning models.
- SHAP-based interpretability for feature impact analysis.
- Real-time prediction via a RESTful API using FastAPI.
- PCA for dimensionality reduction and model efficiency.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Aishuwu/financial-stability-esg.git
   cd financial-stability-esg
   ```

2. Set up and activate a virtual environment:
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```

3. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Run the Jupyter Notebook to preprocess data and train models:
   ```
   Comparative_Analysis_of_Models_for_Prediction_of_Financial_Stability_Using_ESG_Scores.ipynb
   ```

2. Launch the FastAPI service:
   ```bash
   uvicorn app:app --reload
   ```

3. Optionally expose the API to the web using Ngrok:
   ```bash
   ngrok http 8000
   ```

## Dependencies

Key Python libraries used:

- pandas, numpy
- scikit-learn
- xgboost, catboost, lightgbm
- shap, optuna
- fastapi, uvicorn, pyngrok
- joblib, matplotlib, missingno

All dependencies are listed in `requirements.txt`.

## Configuration

- PCA is used to reduce the dataset to 13 principal components.
- The API accepts JSON input structured according to predefined models using Pydantic.
- Endpoints available for each trained model:
  - `/predict/random_forest`
  - `/predict/gradient_boosting`
  - `/predict/xgboost`
  - `/predict/catboost`
  - `/predict/lightgbm`

## Data Overview

- Structured data from 2006 to 2022 on financial and ESG metrics of various companies.
- ~51,000 records across multiple sectors.
- Target variable: `financial_stability`, a weighted composite of financial ratios including ROE, Debt-to-Equity, Profit Margin, etc.
- Engineered features include growth rates, leverage ratios, and ESG interactions.

## Modeling Approach

- Data preprocessing includes imputation, normalization, and feature engineering.
- PCA applied for dimensionality reduction, retaining 95% of variance.
- Trained models:
  - Random Forest
  - Gradient Boosting
  - XGBoost
  - CatBoost
  - LightGBM
- Model tuning performed using Optuna.
- SHAP used for interpretability and feature attribution.

## Deployment

- Trained models are saved using `joblib`.
- FastAPI is used to serve model endpoints.
- API accepts JSON input and returns predicted financial stability scores.
- Ngrok used to expose the API publicly for testing.

## Results Summary

| Model           | MSE     | R²     |
|----------------|---------|--------|
| Gradient Boosting | 0.0151  | 0.9958 |
| Random Forest     | 0.0317  | 0.9913 |
| XGBoost           | 0.2576  | 0.9288 |
| CatBoost          | 0.2281  | 0.9342 |
| LightGBM          | 0.2380  | 0.9342 |

Gradient Boosting demonstrated the best predictive performance and is the default model used for deployment.

## Troubleshooting

- **API not responding**: Ensure `uvicorn` is running and ports are not blocked.
- **Ngrok errors**: Confirm internet connectivity and correct tunnel configuration.
- **Input errors**: Validate that JSON data matches the expected schema defined in the Pydantic model.

## License

This project is open for educational and non-commercial research purposes. For any commercial use, please ensure proper authorization.

