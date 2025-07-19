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
- [Visualizations](#visualizations)
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
