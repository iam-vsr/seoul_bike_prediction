# Seoul Bike Demand Forecasting

Forecast hourly bike rental demand in Seoul based on weather, time, and calendar features using machine learning models like **XGBoost** and **Random Forest**.

## Run on Colab (No Setup)

Just click the badge below to open the notebook in Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/iam-vsr/seoul_bike_prediction/blob/main/seoul_bike_demand_prediction.ipynb)

#### 🔽 Step-by-Step Instructions:

1. **Download the dataset**  
   → [Seoul Bike Sharing Demand](https://github.com/iam-vsr/seoul_bike_prediction/blob/main/SeoulBikeData.csv)

2.  **Run all cells in the notebook**  
   - Everything from data preprocessing, visualization, model training, and prediction is included.

---

## 📌 Project Summary

This project applies supervised machine learning models to predict hourly rental demand using the publicly available **Seoul Bike Sharing dataset**. It includes:

- Feature engineering from timestamp data
- Handling multicollinearity using VIF
- Model comparison across 8+ regressors
- Hyperparameter tuning (RandomizedSearchCV)
- Gradio-based prediction interface

---

## 📈 Best Model Performance (XGBoost)

| Metric | Value |
|--------|--------|
| **R² Score** | **0.950** |
| RMSE | 144.48 |
| MAE  | 84.72 |

> ✅ The model explains **95% of the variance** in rental demand.

---

## 🖼️ Sample Prediction Output

<p align="center">
  <img src="prediction.png" width="350"/>
</p>

---

## 📁 Folder Structure

```bash
SeoulBikeForecasting/
├── models/                             # Saved XGBoost model + feature order
│   ├── xgboost_best_model_r2_0_950.pkl
│   └── feature_order.pkl
├── plots/                              # Visualizations
│   ├── xgboost_tuned_pred_vs_actual.png
│   ├── gradio_sample_output.png  
|   ├── xgboost_tuned_residuals.png
│   └── xgboost_tuned_lineplot.png   
├── seoul_bike_demand_prediction.ipynb  # Full notebook
├── seoul_bike_sharing_demand_prediction.py     # Clean Python script version
├── prediction.png         # Screenshot of sample prediction
├── README.md
