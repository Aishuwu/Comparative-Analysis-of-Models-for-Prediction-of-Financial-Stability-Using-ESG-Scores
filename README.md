# 📊 Comparative Analysis of Models for Prediction of Financial Stability Using ESG Scores

This project explores the use of Environmental, Social, and Governance (ESG) indicators to assess a company's financial stability using supervised machine learning models. It compares the performance of popular ensemble learning algorithms to identify the most accurate and interpretable model.

## 📁 Repository Structure

- `Comparative_Analysis_of_Models_for_Prediction_of_Financial_Stability_Using_ESG_Scores.ipynb` — Main Jupyter notebook with all experimentation and results.

## 🔍 Objective

The aim of this project is to predict financial risk using ESG scores, providing sustainable investment insights for stakeholders by:

- Evaluating and comparing multiple ML models.
- Interpreting key features using SHAP values.
- Offering a scalable risk prediction prototype using FastAPI.

## 🧠 Models Used

| Model               | MSE       | R² Score  |
|--------------------|-----------|-----------|
| Gradient Boosting  | 0.011     | 0.9969    |
| Random Forest      | 0.0306    | 0.9915    |
| CatBoost           | 0.2345    | 0.9352    |
| LightGBM           | 0.2425    | 0.9330    |
| XGBoost            | 0.2609    | 0.9279    |

Gradient Boosting emerged as the best performer with the lowest error and highest explanatory power.

## 🧰 Tech Stack

- Python (Pandas, NumPy, Scikit-learn)
- SHAP (for model interpretability)
- FastAPI (for API deployment)
- Matplotlib / Seaborn (for EDA and visualizations)

## 📈 Key Features

- ESG scores used as primary predictors for financial risk.
- Dimensionality reduction via PCA.
- Feature importance and interpretability using SHAP.
- Deployment-ready with FastAPI for real-time scoring.

## 🚀 How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/Aishuwu/Comparative-Analysis-of-Models-for-Prediction-of-Financial-Stability-Using-ESG-Scores.git
   cd Comparative-Analysis-of-Models-for-Prediction-of-Financial-Stability-Using-ESG-Scores
