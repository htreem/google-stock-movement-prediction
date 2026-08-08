# Google Stock Movement Prediction

Predicting next-day GOOG price direction using technical indicators, feature selection, XGBoost, and time-series cross-validation.

## Approach

Data was collected using `yfinance` and engineered into return, momentum, volatility, trend, and volume-based features.

A three-stage feature-selection process combining correlation filtering, Recursive Feature Elimination (RFE), and XGBoost feature importance reduced the feature set to 10 variables. An XGBoost classifier was then trained using a chronological 80/20 train-test split and tuned with time-series cross-validation.

## Results

The tuned model achieved:

* **Test ROC AUC:** 0.5483
* **Test Accuracy:** 54.81%

The results demonstrate a modest predictive signal while highlighting the difficulty of short-term stock-direction forecasting.

## Technologies

* Python
* pandas
* scikit-learn
* XGBoost
* yfinance
* Matplotlib

See the notebook for the full feature-selection process, model development, visualisations, and evaluation.

## Installation

Clone the repository:

```bash
git clone https://github.com/htreem/google-stock-movement-prediction.git
cd google-stock-movement-prediction
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open `google-stock-movement-prediction.ipynb` and run the notebook from top to bottom.

## Disclaimer

This project is for educational purposes only and does not constitute financial or investment advice.
