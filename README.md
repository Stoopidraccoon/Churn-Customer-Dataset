# Customer Churn Prediction Dataset

# Objective
The goal of this project is to build a machine learning model that can accurately predict whether a bank customer is likely to leave (churn) or stay. By identifying potential churners in advance, banks can take proactive steps to improve customer retention and reduce revenue loss.


# Dataset Description

- **Dataset Name:** Churn Modelling Dataset available on Kaggle 
- **Total Rows:** Approx 10,000 records


#  Key Features
**Column Name**         **Description** 

RowNumber           Unique row ID |
CustomerId          Unique customer ID |
Surname             Customer’s surname |
CreditScore         Customer's credit score |
Geography           Country (France, Germany, Spain) |
Gender              Male / Female |
Age                 Customer’s age |
Tenure              Number of years with the bank |
Balance             Account balance |
NumOfProducts       Number of bank products used |
HasCrCard           Whether customer has credit card |
IsActiveMember      Active status in bank |
EstimatedSalary     Salary of the customer |
Exited              Target variable (1 = Churn, 0 = Not churn) |



# Approach

1. **Data Cleaning & Preparation**
   - Checked for missing or inconsistent data (none found).
   - Removed non-relevant identifiers like RowNumber, CustomerId, and Surname.

2. **Categorical Encoding**
   - Geography: One-Hot Encoding
   - Gender: Label Encoding (Male = 1, Female = 0)

3. **Model Training**
   - Logistic Regression
    

# Results & Insights
**Classification Report**
              precision    recall  f1-score   support

           0       0.81      0.98      0.89      1607
           1       0.45      0.07      0.12       393

    accuracy                           0.80      2000
   macro avg       0.63      0.53      0.51      2000
weighted avg       0.74      0.80      0.74      2000


**Accuracy**
Accuracy: 80.05

**Confusion Matrix**
[[1573   34]
 [ 365   28]]
**Top Influential Features:**
  - Age
  - Balance
  - IsActiveMember
  - Geography (Germany most likely to churn)

 **Insight:** Older customers and those with high balance but low activity are more likely to leave the bank.


