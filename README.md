# ESG-Based Financial Stability Prediction

This project explores how Environmental, Social, and Governance (ESG) scores can be leveraged to assess a company's financial stability using a suite of machine learning models. Built as part of my master's dissertation, the project compares the predictive performance of several regression algorithms and explains the impact of ESG factors using SHAP.

## 📌 Problem Statement

With rising attention on sustainable finance, ESG factors are increasingly used to assess long-term risk. This project aims to predict a company's financial stability score using ESG data and identify the most influential ESG indicators.

## 🧠 Machine Learning Models Used

- Random Forest Regressor
- Gradient Boosting Regressor
- XGBoost
- LightGBM
- CatBoost

## 📊 Key Results

| Model              | MSE      | R² Score |
|-------------------|----------|----------|
| Gradient Boosting | 0.0110   | 0.9969   |
| Random Forest      | 0.0306   | 0.9915   |
| CatBoost           | 0.2345   | 0.9352   |
| LightGBM           | 0.2425   | 0.9330   |
| XGBoost            | 0.2609   | 0.9279   |

Gradient Boosting achieved the highest performance with **R² = 0.9969** and **MSE = 0.0110**.

## 🔍 Tools & Technologies

- Python, Pandas, NumPy, Scikit-learn
- XGBoost, LightGBM, CatBoost
- SHAP (for interpretability)
- PCA (for dimensionality reduction)
- FastAPI (for deploying prediction endpoint)
- Jupyter Notebook

## 📈 Methodology

1. **Data Preprocessing**: Cleaned and normalized ESG data; handled missing values.
2. **Feature Engineering**: Applied PCA to reduce multicollinearity and improve performance.
3. **Model Training & Evaluation**: Used 5 regression models, evaluated with MSE and R².
4. **Model Interpretability**: Employed SHAP values to analyze feature importance.
5. **Deployment**: Built a FastAPI-based interface to serve predictions in real-time.

## 📄 Project Deliverables

- 📓 [Notebook: ESG Model Comparison](./Comparative_Analysis_of_Models_for_Prediction_of_Financial_Stability_Using_ESG_Scores.ipynb)
- 📘 [Dissertation Report](./Aishwarya_Shrigiri_221037997_Dissertation_Paper.pdf)

## 🚀 How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/esg-financial-stability.git
   cd esg-financial-stability
