# Credit Card Fraud Detection using Machine Learning

## Business Problem
Credit card fraud causes significant financial losses and impacts customer trust.
The objective of this project is to detect fraudulent transactions with high recall, as missing a fraud transaction is more costly than incorrectly flagging a genuine one.

This is a highly imbalanced classification problem, where fraud cases represent a very small percentage of total transactions. Therefore, accuracy alone is not a reliable metric.

## Dataset Overview
- Total transactions: 284,807
- Fraudulent transactions: 492 (~0.17%)
- Features:
- V1–V28: anonymized transaction features
- Time: time elapsed since first transaction
- Amount: transaction amount
- Class: target variable (0 = Legit, 1 = Fraud)

## Approach & Methodology

1. Data loading and validation
2. Exploratory Data Analysis (EDA)
3. Feature engineering:
  - Hour of transaction
  - High-value transaction flag
  - Custom spend behavior feature
4. Train–test split with stratification
5. Handling class imbalance:
  - SMOTE for Logistic Regression
  - Class weighting for Random Forest
6. Model training:
  - Logistic Regression
  - Random Forest
7. Model evaluation using:
  - Precision
  - Recall
  - F1-score
  - ROC-AUC
8. Hyperparameter tuning using GridSearchCV

## Model Performance Summary
Model	                     Precision (Fraud)	Recall (Fraud)	ROC-AUC
Logistic Regression (SMOTE)	  Low	            High (0.90)	     0.97
Random Forest (Balanced)	  High (0.82)	    High (0.83)	     0.98
Recall was prioritized to minimize missed fraud cases, while Random Forest provided a strong balance between recall and precision

## Model Evaluation & Insights

- Logistic Regression achieved very high recall, making it suitable when detecting maximum fraud is the priority
- Random Forest produced fewer false positives while maintaining strong recall
- ROC-AUC scores confirmed strong discrimination between fraud and non-fraud transactions
- Feature importance analysis improved interpretability and business understanding

## Tools & Techniques

- Python
- Pandas, NumPy
- Scikit-learn
- Imbalanced-learn (SMOTE)
- Matplotlib, Seaborn
  
## Business Impact & Conclusion

- Fraud detection requires business-driven evaluation, not just accuracy
- Logistic Regression is effective when recall is the top priority
- Tuned Random Forest is recommended for deployment due to stable and balanced performance
- This approach can be extended to real-time fraud monitoring systems

 ## Future Enhancements

- Implement cost-sensitive learning
- Try XGBoost / LightGBM models
- Deploy model as an API for real-time fraud scoring
  
## Data Source
- Credit Card Fraud Detection dataset is taken from Kaggle
## About Me
 Pallavi Mali – Data Analyst skilled in Power BI, SQL, Python, Stats, ML DAX, Excel.
- LinkedIn: linkedin.com/in/pallavi-mali-4b8888272
- GitHub: github.com/pal-analytics

