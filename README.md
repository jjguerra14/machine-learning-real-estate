# 🏡 Machine Learning Real Estate Price Prediction in Medellín

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)
![Scikit Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?style=for-the-badge&logo=scikitlearn)
![XGBoost](https://img.shields.io/badge/XGBoost-Regression-green?style=for-the-badge)
![CatBoost](https://img.shields.io/badge/CatBoost-Gradient_Boosting-yellow?style=for-the-badge)
![Random Forest](https://img.shields.io/badge/Random_Forest-Ensemble-darkgreen?style=for-the-badge)
![Pandas](https://img.shields.io/badge/Pandas-Data_Processing-purple?style=for-the-badge&logo=pandas)
![GitHub](https://img.shields.io/badge/GitHub-Portfolio-black?style=for-the-badge&logo=github)

---

## 📌 Project Overview

This project focuses on predicting **real estate price per square meter (COP/m²)** in **Medellín, Colombia**, using supervised Machine Learning regression models.

The objective is to estimate property market values based on project-level commercial and structural features, enabling data-driven real estate pricing analysis.

The project compares multiple regression models to identify the most accurate predictive approach.

---

## 🎯 Business Objective

The real estate market is highly influenced by location, project characteristics, inventory dynamics, and commercial performance.

This project aims to answer:

> **Given the characteristics of a real estate project in Medellín, what is the expected offer price per square meter?**

Example use case:

- Zone: El Poblado
- Subzone: Castropol
- Property Type: Apartment
- Area: 95 m²
- Construction Stage: Presale
- Sales Dynamics

Predicted output:

```text
Expected price ≈ COP/m²
```

---

## 📂 Dataset

The dataset contains real estate market information including:

### Features used:

- Zone
- Sub Zone
- Socioeconomic Stratum
- Average Offer Area
- Active Months
- Average Monthly Sales
- Total Project Units
- Available Units
- Units Yet to Launch
- Total Sold Percentage
- Property Type
- Housing Category (VIS / Non-VIS)
- Construction Status

### Target Variable:

```python
$ Prom. Oferta m2
```

(Price per square meter)

---

## 🧹 Data Preprocessing

The data pipeline includes:

✅ City filtering (**Medellín only**)  
✅ Missing value handling  
✅ Numeric type conversion  
✅ Categorical cleaning  
✅ Outlier removal using IQR method  
✅ Feature engineering preparation  
✅ Train/Test split  
✅ Cross-validation  

---

## 🤖 Machine Learning Models

Three supervised regression models were implemented:

### 1️⃣ CatBoost Regressor
Used because:

- Native categorical feature handling
- Strong performance on tabular data
- Minimal preprocessing
- Excellent with heterogeneous real estate datasets

---

### 2️⃣ XGBoost Regressor
Used because:

- High predictive performance
- Strong gradient boosting framework
- Handles complex nonlinear relationships
- Competitive benchmark model

---

### 3️⃣ Random Forest Regressor
Used because:

- Strong ensemble baseline
- Robust against overfitting
- Interpretable feature importance
- Stable performance

---

## 📊 Evaluation Metrics

Models were evaluated using:

### MAE
Mean Absolute Error

Measures average prediction error.

---

### RMSE
Root Mean Squared Error

Penalizes larger prediction mistakes.

---

### R² Score
Coefficient of Determination

Measures explained variance.

---

### MAPE
Mean Absolute Percentage Error

Measures average percentage prediction error.

---

## 📈 Example Results (CatBoost)

```text
MAE:   536,910 COP
RMSE:  761,061 COP
R²:    0.9316
MAPE:  9.54%
```

Interpretation:

- The model explains over **93%** of price variability.
- Average pricing error is below **10%**.
- Strong predictive performance for real estate pricing.

---

## 🔍 Cross Validation

A 5-Fold Cross Validation strategy was used to validate model robustness:

```python
KFold(n_splits=5, shuffle=True, random_state=42)
```

This ensures the model generalizes well beyond a single train/test split.

---

## 📌 Feature Importance Analysis

Feature importance was analyzed to understand the main drivers of real estate pricing.

Key variables typically include:

- Zone
- Sub Zone
- Stratum
- Area
- Sales velocity
- Inventory availability
- Construction status

---

## 🛠 Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- CatBoost
- XGBoost
- Random Forest
- Git
- GitHub
- VS Code

---

## 📁 Project Structure

```bash
machine-learning-real-estate/
│
├── catboost_model.py
├── xgboost_model.py
├── randomforest_model.py
├── notebook_analysis.ipynb
├── requirements.txt
├── README.md
└── dataset/
```

---

## 🚀 How to Run

Clone repository:

```bash
git clone https://github.com/jjguerra14/machine-learning-real-estate.git
```

Move into project:

```bash
cd machine-learning-real-estate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run models:

```bash
python catboost_model_medellin.ipynb
```

or

```bash
python xgboost_model.ipynb
```

or

```bash
python randomforest_model.ipynb
```

---

## 📍 Future Improvements

Potential enhancements:

- Hyperparameter optimization
- SHAP explainability
- Geospatial features (latitude/longitude)
- Property-level prediction instead of project-level prediction
- Deployment as web application
- Streamlit dashboard
- API integration

---

## 👨‍💻 Author

**Juan José Guerra Bermúdez**

Civil Engineer | Data Analytics | Machine Learning | Credit Risk Analytics

GitHub:
https://github.com/jjguerra14

**Karla Maria Castaño**

---

## ⭐ Repository Purpose

This project was developed as part of my Machine Learning learning portfolio to demonstrate practical skills in:

- supervised learning
- regression modeling
- data preprocessing
- real-world predictive analytics
- model comparison and validation

---

# Thanks for visiting 🚀
