# 📊 Business Forecasting – Seasonal Trend Analysis Using ARIMA

![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
![Model](https://img.shields.io/badge/Model-ARIMA(3,1,0)-blue)
![Tool](https://img.shields.io/badge/Tool-SPSS-orange)

This project performs seasonal trend analysis and forecasting on quarterly business investment data using:

- **Additive Decomposition**
- **Dummy Variable Regression (Linear, Quadratic, Cubic)**
- **ARIMA Modeling (Box–Jenkins Method)**

After comparing several forecasting models, the final selected model is **ARIMA (3,1,0)** — chosen based on the lowest BIC, significant AR parameters, and clean white-noise residuals.

---

## 📄 Full Report
📘 The complete analysis including graphs, SPSS outputs, and statistical reasoning is available here:

👉 **[`report/ARIMA_Seasonal_Trend_Analysis_Report.pdf`](#)**

---

## 📁 Project Structure

📦 business-forecasting-arima-project
│
├── 📘 report/
│ └── ARIMA_Seasonal_Trend_Analysis_Report.pdf
│
└── 📄 README.md

---

## 📌 Overview

This project answers important forecasting questions:

- Does the quarterly data show consistent seasonal patterns?
- What type of trend-cycle component (linear, quadratic, cubic) best fits the data?
- Which forecasting model gives the lowest out-of-sample error?
- Why is ARIMA (3,1,0) more reliable than dummy-variable regression models?

---

## 🧩 Methodology Summary

### **1️⃣ Decomposition (Additive Model)**
- Seasonal, trend, and irregular components extracted  
- Additive model preferred because seasonal variation remained constant  
- Seasonal indices calculated  
- Deseasonalized dataset created  

---

### **2️⃣ Dummy Variable Regression**

| Model Type | Adjusted R² | Notes |
|------------|-------------|-------|
| Linear Trend + Dummies | 0.392 | Poor fit, strong autocorrelation |
| Quadratic Trend + Dummies | 0.711 | Better but still not ideal |
| **Cubic Trend + Dummies** | **0.940** | Best in-sample accuracy |

**Why cubic was not selected:**  
Despite high in-sample R², the model produced unstable holdback forecasting errors — meaning it overfitted.

---

### **3️⃣ ARIMA Modeling**

**Models tested:**

- ARIMA (1,0,0)  
- **ARIMA (3,1,0)**  
- ARIMA (0,1,5)  
- ARIMA (4,1,0) — overfitted  
- ARIMA (3,1,1) — overfitted  

**Why ARIMA (3,1,0) is the final model:**

✔ Lowest Normalized BIC  
✔ Significant AR(3) parameter  
✔ Residuals show white noise  
✔ Better holdback performance  
✔ More stable than cubic dummy regression  

---

## 📉 Forecast Comparison (Holdback Data)

| Model | MAPE | MAD | MSE |
|-------|------|------|-----------|
| Linear Dummy | **4.65%** | **171.9** | **38,701** |
| Cubic Dummy | 16.25% | 586.4 | 452,248 |
| **ARIMA (3,1,0)** | 7.31% | 269.2 | 96,862 |

**Final choice:**  
➡️ **ARIMA (3,1,0)** — best balance of reliability & generalization

---

## 🛠 Tools & Skills Demonstrated

- SPSS Forecasting  
- Time Series Decomposition  
- ARIMA (Box–Jenkins Method)  
- ACF/PACF Analysis  
- Regression Modeling  
- Holdback Forecast Validation  
- Error Metrics: MAD, MSE, MAPE  

---

## 👤 Author

**Lakshmi Chittem**  
Business Analytics | Data Analysis  
