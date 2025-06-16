# Loan_Data

📊 Feature Descriptions
Feature	Type	Description
person_age	Numeric	Age of the applicant
person_gender	Categorical	Gender of the applicant (male/female)
person_education	Categorical	Highest educational qualification
person_income	Numeric	Annual income of the applicant
person_emp_exp	Numeric	Years of employment experience
person_home_ownership	Categorical	Home ownership status (RENT/OWN/MORTGAGE/etc.)
loan_amnt	Numeric	Requested loan amount
loan_intent	Categorical	Purpose of the loan (PERSONAL, EDUCATION, MEDICAL, etc.)
loan_int_rate	Numeric	Interest rate for the loan
loan_percent_income	Numeric	Loan amount as a percentage of income
cb_person_cred_hist_length	Numeric	Length of credit history
credit_score	Numeric	Credit score of the applicant
previous_loan_defaults_on_file	Categorical	Whether the person has defaulted in the past (Yes/No)
loan_status	Binary	Target variable indicating loan approval (1) or rejection (0)

📌 Objective
To build a predictive model that can help financial institutions determine:

Whether a loan should be approved or rejected.

Identify risk factors such as poor credit history, low income, or previous defaults.

⚙️ Machine Learning Workflow
Data Preprocessing

Handling categorical variables via label encoding or one-hot encoding

Scaling numerical features (for non-tree models)

Splitting data into train/test sets

Modeling

Primary Model: Random Forest Classifier

Also tested: Logistic Regression, XGBoost (optional)

Evaluation

Accuracy

Precision, Recall, F1-Score

Confusion Matrix

📁 Example Usage (Model Training)
python
Copy
Edit
import pandas as pd
from sklearn.ensemble import RandomForestClassifier

df = pd.read_csv("loan_data.csv")
X = df.drop("loan_status", axis=1)
y = df["loan_status"]

# Encoding categorical columns
X = pd.get_dummies(X)

# Train model
model = RandomForestClassifier()
model.fit(X, y)
📈 Potential Applications
Automated loan screening systems

Credit risk analysis

Financial decision support tools

✅ Requirements
Python 3.x

pandas, scikit-learn, matplotlib, seaborn

