# google-stock-movement-prediction
Predicting next-day GOOG price direction using technical indicators, feature selection, XGBoost, and time-series cross-validation.

Approach: Data was collected using yfinance and engineered into return, momentum, volatility, trend, and volume-based features. A three-stage feature-selection process combining correlation filtering, Recursive Feature Elimination (RFE), and XGBoost feature importance reduced the feature set to 10 variables. An XGBoost classifier was then trained using a chronological 80/20 train-test split and tuned with time-series cross-validation.

Results: The tuned model achieved a test ROC AUC of 0.5483 and accuracy of 54.81%, demonstrating a modest predictive signal while highlighting the difficulty of short-term stock-direction forecasting.

Tech: Python, pandas, scikit-learn, XGBoost, yfinance, Matplotlib.

See the notebook for the full feature-selection process, model development, visualisations, and evaluation.
