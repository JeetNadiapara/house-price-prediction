🏠 House Price Prediction

Predicting house sale prices from property features using Linear Regression in Python with pandas and scikit-learn.

📌 Overview

This project builds a baseline regression model to estimate the sale price of a house from features such as lot area, building type, zoning, year built and basement size. It covers the full basic machine learning workflow: loading data, cleaning, encoding, training and evaluation.

📂 Files
File	Description
house_price_predictor.ipynb	Jupyter notebook with the full workflow
HousePricePrediction.csv	Dataset (2,919 rows, 13 columns)
📊 Dataset

Features used:

MSSubClass – type of dwelling
MSZoning – zoning classification
LotArea – lot size (sq ft)
LotConfig – lot configuration
BldgType – building type
OverallCond – overall condition rating
YearBuilt / YearRemodAdd – construction and remodel year
Exterior1st – exterior covering
BsmtFinSF2 / TotalBsmtSF – basement area (sq ft)

Target: SalePrice

⚙️ Workflow
Data exploration – shape, data types, summary statistics
Data cleaning – dropped Id, handled missing values
Encoding – one-hot encoding of categorical features (pd.get_dummies)
Train/test split – 80% training, 20% testing
Model training – Linear Regression
Feature scaling – StandardScaler, to test its effect on performance
Evaluation – R², MAE, RMSE and MAPE
📈 Results
Metric	Score
R² Score	0.374
MAE	~30,830
RMSE	~41,139
MAPE	~18.7%

Feature scaling did not change the results. This is expected, because plain Linear Regression is not affected by feature scale.

🚀 Future Improvements
Remove rows with missing SalePrice instead of filling them with the mean
Try other models: Random Forest, Gradient Boosting, XGBoost
Apply regularisation (Ridge, Lasso)
Log-transform the target to reduce skew
Cross-validation and hyperparameter tuning
🛠️ Tech Stack
Python 3
pandas, NumPy
scikit-learn
Jupyter Notebook
