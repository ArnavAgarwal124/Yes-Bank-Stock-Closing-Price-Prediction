# 📊 Yes Bank Stock Closing Price Prediction

![Python](https://img.shields.io/badge/Python-3.10-blue.svg)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Regression-green)
![Colab](https://img.shields.io/badge/Google-Colab-orange)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## 🧾 Problem Statement

**Yes Bank**, one of India’s major private sector banks, has experienced significant market fluctuations, especially following the **2018 Rana Kapoor fraud case**.  
This project aims to **analyze and predict monthly closing stock prices** using statistical regression models and machine learning techniques.

By leveraging historical stock data (Open, High, Low, Close), we attempt to:
- Understand market behavior  
- Detect trends  
- Build predictive models to forecast future closing prices  

---

## 🧠 Project Objectives

- Analyze the impact of major financial fraud events on Yes Bank’s stock performance.  
- Build regression-based models to predict monthly closing stock prices.  
- Compare **Linear Regression**, **Lasso Regression**, and **Ridge Regression** models and evaluate performance metrics.

---

## 📅 Dataset Description

**Source:** Historical monthly stock price data of Yes Bank since inception.  

| Feature | Description |
|----------|-------------|
| Date | Month and Year of stock price record |
| Open | Opening price of the stock for the month |
| High | Highest price during the month |
| Low | Lowest price during the month |
| Close | Closing price of the stock (**Target Variable**) |

- **Total Records:** 185  
- **Null Values:** None  

---

## 🔧 Methodology

### 1️⃣ Data Wrangling
- Imported libraries: `NumPy`, `Pandas`, `Matplotlib`, `Seaborn`, `Scikit-learn`
- Loaded dataset from Google Drive  
- Converted Date column to datetime (`%b-%y`)
- Set Date as index and assigned monthly frequency (`MS`)

### 2️⃣ Exploratory Data Analysis (EDA)
- Visualized Opening, Closing, High, and Low price trends  
- Observed sharp decline post-2018 (Rana Kapoor case)  
- Scatter plots and heatmaps revealed **high correlations** among numeric features  
- Distribution plots showed **right-skewed** data  

---

## 🧩 Data Modeling

### 🔹 Linear Regression
- Features: `Open`, `High`, `Low`
- **MSE:** 19.99  
- **R²:** 0.9978 (~99.78% accuracy)  
- Residuals were minimal, showing a strong model fit.  

### 🔹 Lasso Regression (L1 Regularization)
- Used `GridSearchCV` to tune **alpha**
- **Best Alpha:** 1  
- **MSE:** 20.22  
- **R²:** 0.9978  

### 🔹 Ridge Regression (L2 Regularization)
- Used `GridSearchCV` to tune **alpha**
- **Best Alpha:** 60  
- **MSE:** 20.03  
- **R²:** 0.9978  

---

## 📈 Model Evaluation

| Model | MSE | RMSE | MAE | R² Score |
|--------|------|------|------|-----------|
| Linear Regression | 19.99 | 4.47 | 3.05 | 0.9978 |
| Lasso Regression | 20.22 | 4.49 | 3.07 | 0.9978 |
| Ridge Regression | 20.03 | 4.47 | 3.05 | 0.9978 |

✅ All models performed exceptionally well (R² > 99%)  
✅ Ridge Regression provided the **best generalization and stability**

---

## 📊 Visualization Insights

- Sharp decline in closing price post-2018 (Rana Kapoor case)  
- Strong correlation between **Opening** and **Closing** prices  
- Heatmaps confirmed **multicollinearity** among features  
- Residuals were symmetric and centered → indicating **excellent model fit**

---

## 🏁 Conclusion

- Regression models achieved **>99% accuracy**  
- **Ridge Regression** was the most stable and generalizable model  
- The fraud event in 2018 had a **significant negative impact** on stock prices  
- The model can effectively forecast **monthly closing prices** for Yes Bank  

---

## 🧩 Technologies & Tools

| Category | Tools Used |
|-----------|-------------|
| **Language** | Python |
| **Libraries** | Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Plotly |
| **Environment** | Google Colab |
| **Techniques** | Linear Regression, Lasso, Ridge, GridSearchCV, EDA |
| **Visualization** | Line charts, Scatter plots, Heatmaps, Residual plots |

---

## 📘 Future Work

- Implement **ARIMA / LSTM (Time Series)** models for time-based forecasting  
- Integrate external indicators (NIFTY, inflation, macroeconomic data)  
- Build an **interactive dashboard** (Streamlit / Power BI) for live predictions  

---

## 💡 Key Takeaways

✅ Significant drop in Yes Bank stock prices post-2018  
✅ High correlation among stock features (multicollinearity)  
✅ Ridge Regression offered robust generalization  
✅ Regression models achieved **>99% accuracy** on historical data  

---

## 🧰 How to Run the Project

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/YesBank-Stock-Prediction.git
cd YesBank-Stock-Prediction

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the notebook
jupyter notebook YesBank_Price_Prediction.ipynb
