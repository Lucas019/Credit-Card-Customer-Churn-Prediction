# Credit-Card-Customer-Churn-Prediction
This project is a customer churn prediction model for credit card, the dataset is collected from [Kaggle](https://www.kaggle.com/datasets/sakshigoyal7/credit-card-customers)

## Approach to the problem
First, we explore the dataset through univariate analysis to find features we'd like to include in the model.

Then, since lots of features are proxies for the customer historical activity, we calculate a correlation matrix heatmap to see whether we should use PCA to capture most of the variance in fewer number of features (here since we only have a few features, it eventually turned out to be less effective to linear combine those features).

After that, we built 4 candidate classification models: Logistic Regression, Gaussian Naive Bayes, Random Forest, and XGBoost. We found that XGBoost turned out to the most accurate and robust model.

Finally, we shortlisted features via permutation feature importance and provide recommendations through SHAP analysis.

## Recommendations and insights

3 recommendations are provided as follows:

1. **Total transaction amount** in the last 12 months is the most important feature we need pay attention to the customers, customers with low transaction amount should be incentivized to use credit card more through promotion messages or emails.

2. **Comparison with previous quarters** is also important, if the transaction shows a downward trend (less transaction in Q4 comparing to Q1), we should take actions to remind customers.

3. **Increasing the number of products** held by the customer can also increase the chance of retention.
