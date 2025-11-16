Telco Customer Churn Analysis & Prediction

1. Project Overview
Telecom companies often lose revenue due to customer churn. Predicting churn helps identify at-risk customers and engage them with targeted retention offers.
In this project, I:

* Explored customer demographics, account information, service usage, and billing details
* Created visualizations to understand churn patterns
* Engineered new features for improved model performance
* Built a Random Forest classifier to predict churn
* Analyzed feature importance to identify key churn drivers

This project demonstrates my ability to solve real-world business problems using data analysis and machine learning.

2. Dataset

The dataset consists of 7,043 customers with 21 features including:

Demographics: gender, senior citizen, dependents
Account information: tenure, contract, billing method
Services: phone services, internet services, streaming services
Charges: MonthlyCharges, TotalCharges
Target variable: Churn (Yes/No)

Dataset source:  Telco Customer Churn

3. Key Steps

A. Data Cleaning
Converted `TotalCharges` to numeric
Handled blank/invalid values
Checked for duplicates and null values
Transformed binary fields into categorical
Prepared dataset for modeling using encoding techniques

B. Exploratory Data Analysis (EDA)

Performed visual analysis to understand churn patterns:
Churn distribution across demographics
Churn vs contract type
Churn vs tenure
Churn vs MonthlyCharges and TotalCharges
Analysis of service usage patterns (OnlineSecurity, TechSupport, etc.)
Payment method impact on churn

C. Feature Engineering
Created additional features to enhance model performance:
NumServices: count of services subscribed
AvgChargePerMonth: TotalCharges / tenure
These features added more context to the model and improved interpretability.

D. Model Building
Built a Random Forest classifier using Scikit-Learn:
Train-test split using stratified sampling
One-hot encoding for categorical variables
Baseline Random Forest classifier
Evaluated using:
	Accuracy
	Precision
	Recall
	F1-score
	ROC AUC

E. Feature Importance Analysis
Key churn drivers identified:

1. TotalCharges
2. Tenure
3. MonthlyCharges
4. PaymentMethod (Electronic Check)
5. InternetService (Fiber Optic)

These variables strongly influence customer churn behaviour.

4. Business Insights

From the analysis:

Customers with short tenure are more likely to leave
Month-to-month contract customers have the highest churn rate
High monthly charges increase churn likelihood
Customers paying via electronic check churn more frequently
Lack of value-added services (security, tech support) correlates with churn

These insights can guide:
Retention campaigns
Pricing strategy
Service improvements
Better onboarding for new customers

5. Tools & Technologies

Python 3
Pandas
NumPy
Matplotlib / Seaborn
Scikit-Learn
Jupyter Notebook

7. Future Improvements

Add Logistic Regression baseline comparison
Hyperparameter tuning (GridSearchCV / RandomizedSearchCV)
Apply class imbalance techniques (class weights / SMOTE)
SHAP explanations for interpretability
Deploy the model via Flask/Streamlit
Build an interactive dashboard for insights


