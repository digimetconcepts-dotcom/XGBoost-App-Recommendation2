# 📱 Mobile App Success Predictor & Recommender

A machine learning system that predicts the potential rating of a mobile app and recommends similar apps based on category and features.

---

## 🧠 Project Overview

This end-to-end AI system combines:
- **Supervised Learning** — XGBoost model to predict app ratings
- **Unsupervised Learning** — KNN-based recommendation engine to find similar apps
- **Streamlit UI** — Interactive interface for developers to test their app ideas

---

## 📁 Project Structure

```
mobile_app_predictor/
│
├── apps_data.csv               ← Google Play Store dataset (from Kaggle)
├── xgb_app_recommendation.py   ← Main notebook (preprocessing + modeling)
├── app.py                      ← Streamlit application
├── xgb_model.pkl               ← Trained XGBoost model
├── knn_model.pkl               ← Trained KNN recommender
├── scaler.pkl                  ← Feature scaler
├── df_clean.pkl                ← Cleaned dataset
├── rec_matrix.pkl              ← Recommendation feature matrix
└── README.md
```

---

## 🗂️ Dataset

 
Save as: `apps_data.csv`

---

## ⚙️ Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core language |
| Pandas / NumPy | Data preprocessing |
| Scikit-learn | KNN, encoding, metrics |
| XGBoost | Rating prediction |
| Matplotlib / Seaborn | EDA visualizations |
| Streamlit | Web application UI |
| Pickle | Model serialization |

---

## 🚀 How to Run (Google Colab)

1. Upload `apps_data.csv` to your Colab session
2. Run all cells in `xgb_app_recommendation.py` in order
3. Install pyngrok: `!pip install pyngrok -q`
4. Launch the app and open the generated public URL

---

## 🔍 Features

### Success Prediction
Input your app's category, size, price, content rating, and expected installs/reviews — the model returns a predicted rating out of 5.0.

### App Recommendations
The system returns a table of 5 similar apps already on the Play Store that you may compete with.

---

## 📊 Model Performance

| Model | MAE | RMSE |
|---|---|---|
| Random Forest | 0.3689 | 0.5342 |
| **XGBoost** ✅ | **0.3555** | **0.5198** |

XGBoost was selected as the final model for its lower error on both metrics.

---

## 📌 Key Findings

- **Reviews** and **Installs** are the strongest predictors of app rating
- **Category** and **Size** have moderate influence
- **Price** has relatively low impact on predicted rating

---

## 👤 Author

Capstone Project — Machine Learning with Streamlit  
Built as part of the Thrive Student Project Program
