# Customer-Churn-Analysis-for-Telecom-Industry
Objective: Predict churn and derive actionable strategies to retain users in a highly competitive telecom environment.

1.1 Introduction

Churn prediction is a crucial challenge in the telecom industry. Retaining existing customers is more cost-effective than acquiring new ones. The aim is to analyze customer data and identify patterns associated with customer churn.

1.2 Objectives
	•	Identify key drivers of churn.
	•	Predict churn using machine learning algorithms.
	•	Develop strategies to reduce customer loss.

1.3 Dataset Features

The dataset includes customer demographics, account information, and services used. Key columns include:
	•	tenure, MonthlyCharges, TotalCharges
	•	Contract, PaymentMethod, InternetService, etc.
	•	Churn (target variable)

⸻

2. Data Preparation

2.1 Import Libraries and Dataset

All necessary Python libraries were imported, and the dataset was loaded.

2.2 Handling Missing Values
	•	Missing values in TotalCharges were imputed using median values.
	•	Null checks ensured data quality.

⸻

3. Exploratory Data Analysis (EDA)

3.1 Categorical Analysis
	•	Pie and bar plots show churn rates across Contract, PaymentMethod, and InternetService.
	•	High churn was observed in month-to-month contracts.

3.2 Numerical Analysis
	•	Histograms and boxplots showed the distribution of MonthlyCharges and TotalCharges.
	•	Churned customers typically had higher MonthlyCharges.

⸻

4. Data Preprocessing

4.1 Outlier Detection

Outliers were detected using IQR method and treated appropriately.

4.2 Rare Category Encoding

Rare categories were grouped under “Other” to reduce noise.

4.3 Encoding Categorical Variables

Used:
	•	Label Encoding for binary columns
	•	One-Hot Encoding for non-ordinal features

4.4 Balancing the Dataset

Churn class imbalance was addressed using SMOTE (Synthetic Minority Over-sampling Technique).

4.5 Feature Scaling

StandardScaler was used to normalize continuous variables for model compatibility.

⸻

5. Modeling and Evaluation

5.1 Data Splitting

Dataset split into 80% training and 20% testing.

5.2 Model Building

Models used:
	•	Logistic Regression
	•	Random Forest
	•	XGBoost
	•	SVM

5.3 Hyperparameter Tuning
	•	GridSearchCV used for optimization.
	•	Cross-validation ensured model generalizability.

5.4 Evaluation Metrics
	•	Accuracy, Precision, Recall, F1-score, ROC-AUC used.
	•	XGBoost performed best with high ROC-AUC and recall.

⸻

6. Feature Importance
	•	Top contributing features: Contract, tenure, MonthlyCharges, OnlineSecurity
	•	Visualized with bar charts and SHAP values

⸻

7. Conclusion and Recommendations
	•	Month-to-month contracts and high monthly charges increase churn.
	•	Recommend loyalty programs, bundled offers, and improved service experience.
	•	XGBoost is the best model for deployment based on performance metrics.
