# BAQ-EXPERIMENT: LSTM-Based PM2.5 Forecasting

This repository contains experimental notebooks, models, and utilities used to build and evaluate LSTM-based time-series forecasting models for PM2.5 air pollution prediction in Bangkok.

---

## 📂 Repository Structure

```
BAQ-EXPERIMENT/
├── data/
│   └── baq_dataset.csv            # Cleaned input dataset
│
├── models/
│   ├── feature_scaler.pkl         # Scaler for input features
│   ├── target_scaler.pkl          # Scaler for target (PM2.5)
│   └── label_encoder.pkl          # Encoder for categorical variables (if any)
│
├── notebooks/
│   ├── baq_lstm.ipynb             # 1-step LSTM model training and evaluation
│   └── baq_lstm_multistep.ipynb   # Multi-step LSTM model (e.g. 24h or 48h ahead)
│
├── predict.py                     # Python script to load model & make predictions
├── .gitignore
├── LICENSE
└── README.md
```

---

## 🧠 Model Overview

* Deep learning approach using **LSTM (Long Short-Term Memory)** networks
* Input features include weather variables and air pollutant levels
* Separate models trained for:

  * 1-step ahead prediction
  * 24-step ahead prediction (1 day)
  * 48-step ahead prediction (2 days)
* Scalers and encoders saved to disk for consistent preprocessing

---

## 📊 Dataset

* `baq_dataset.csv`: Final dataset containing weather & air quality features

---

## 🧪 Experiments & Results

* Trained on hourly data
* Evaluation metrics include MAE, RMSE, and R2
* Visualizations include prediction vs. ground truth line charts
