📊 Yes Bank Stock Closing Price Prediction
🧾 Problem Statement

Yes Bank, one of India’s major private sector banks, has experienced significant market fluctuations, especially following the 2018 Rana Kapoor fraud case.
This project aims to analyze and predict the bank’s monthly closing stock prices using statistical regression models and machine learning techniques.

By leveraging historical stock data (Open, High, Low, Close), we attempt to understand market behavior, detect trends, and build predictive models that can forecast the stock’s future closing price.

🧠 Project Objective

To study the impact of financial fraud events on Yes Bank’s stock performance.

To build a predictive model that can accurately estimate monthly closing stock prices using regression techniques.

To compare Linear Regression, Lasso Regression, and Ridge Regression models and evaluate their performance.

📅 Dataset Description

Source: Monthly stock price data of Yes Bank since inception.

Attributes:

Feature	Description
Date	Month and Year of stock price record
Open	Opening price of the stock for the month
High	Highest price reached during the month
Low	Lowest price during the month
Close	Closing price of the stock (Target Variable)

Total Records: 185

Null Values: None

🔧 Methodology
1️⃣ Data Wrangling

Imported libraries (NumPy, Pandas, Matplotlib, Seaborn, Sklearn)

Loaded dataset from Google Drive

Converted Date column to datetime format (%b-%y)

Set Date as index and assigned a monthly frequency (MS)

2️⃣ Exploratory Data Analysis (EDA)

Visualized Opening, Closing, High, and Low price trends using line charts.

Observed a sharp decline after 2018 corresponding to the Rana Kapoor case.

Performed scatter plots to study correlations among features.

Created distribution plots revealing right-skewed distributions.

Generated heatmaps showing strong correlations among all numeric features (multicollinearity).

🧩 Data Modeling

Three models were implemented and compared:

🔹 Linear Regression

Fitted a baseline model with features: Open, High, Low

Achieved:

Mean Squared Error (MSE): 19.99

R² Score: 0.9978 (~99.78% accuracy)

Residual analysis showed minimal deviation — indicating a strong model fit.

🔹 Lasso Regression (L1 Regularization)

Applied Lasso to handle multicollinearity and prevent overfitting.

Used GridSearchCV to tune hyperparameter alpha.

Best Alpha: 1

Achieved:

MSE: 20.22

R²: 0.9978

🔹 Ridge Regression (L2 Regularization)

Applied Ridge Regression for coefficient shrinkage.

Optimal Alpha: 60 (via GridSearchCV)

Achieved:

MSE: 20.03

R²: 0.9978

📈 Model Evaluation
Model	MSE	RMSE	MAE	R² Score
Linear Regression	19.99	4.47	3.05	0.9978
Lasso Regression	20.22	4.49	3.07	0.9978
Ridge Regression	20.03	4.47	3.05	0.9978

All models performed exceptionally well, with R² > 99%.

Ridge Regression provided the best generalization and stability among the models.

📊 Visualization Insights

The closing price sharply declined post-2018 due to the Rana Kapoor case.

Opening and Closing prices show a strong correlation, confirming market efficiency.

Scatter plots and heatmaps reveal multicollinearity among stock attributes.

Residual plots show symmetric and centered residuals — indicating a well-fitted model.

🏁 Conclusion

The developed regression models (especially Ridge Regression) achieved over 99% accuracy, showing excellent predictive performance.

The study confirms that external events like the 2018 fraud case had a significant negative impact on stock prices.

The final model can be effectively used for monthly stock price forecasting or trend analysis for Yes Bank.

🧩 Technologies & Tools
Category	Tools Used
Language	Python
Libraries	Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Plotly
Environment	Google Colab
Techniques	Linear Regression, Lasso, Ridge, GridSearchCV, EDA
Visualization	Line charts, Scatter plots, Heatmaps, Residual plots
📘 Future Work

Implement ARIMA / LSTM (Time Series) models for temporal prediction.

Include external market indicators (e.g., NIFTY index, macroeconomic data).

Build an interactive dashboard (e.g., Streamlit / Power BI) to visualize live predictions.

💡 Key Takeaways

✅ Significant drop in Yes Bank stock prices post-2018.
✅ High correlation among stock features (multicollinearity).
✅ Ridge Regression offers robust generalization.
✅ Regression models can achieve >99% accuracy for historical data.
