**Loan Prediction Project**

**Overview**
This project aims to predict loan approval status based on various applicant features. The dataset used contains information about applicants including personal details, income, loan details, and loan approval status.

**Dataset**
The dataset loan-train.csv includes the following columns:

Loan_ID: Unique identifier for each loan application
Gender: Gender of the applicant
Married: Marital status of the applicant
Dependents: Number of dependents
Education: Education level of the applicant
Self_Employed: Employment status of the applicant
ApplicantIncome: Income of the applicant
CoapplicantIncome: Income of the coapplicant
LoanAmount: Amount of loan requested
Loan_Amount_Term: Term of the loan
Credit_History: Credit history of the applicant
Property_Area: Area where the property is located
Loan_Status: Loan approval status (target variable)
Data Exploration

****Data Loading and Initial Exploration:**

The dataset contains 614 entries and 13 features.
Missing values are present in several columns and are handled through imputation.

****Feature Engineering:**

Applied log transformation to ApplicantIncome and LoanAmount for better distribution.
Categorical features are encoded using Label Encoding.
Data Preprocessing:

Missing values are imputed with the mode for categorical features and mean for numerical features.
Features are standardized using StandardScaler.
Model Building

**Decision Tree Classifier:**

A Decision Tree model is trained and evaluated, providing an initial accuracy of 72% on the test set.
Classification report includes precision, recall, and F1-score for both classes.
Hyperparameter Tuning with GridSearchCV:

GridSearchCV is used to find the best hyperparameters for the Decision Tree model.

**The best parameters found are:**
criterion: 'gini'
max_depth: 4
max_features: 'log2'
splitter: 'random'
The optimized Decision Tree model achieves an accuracy of 80% on the test set, with improved performance metrics.

**Logistic Regression:**

A Logistic Regression model is also trained and evaluated, achieving an accuracy of 80%.
The classification report indicates better performance in predicting the positive class compared to the Decision Tree model.
Results

****Decision Tree Classifier with GridSearchCV Performance:**
Accuracy: 80%
Precision for class 0: 0.94
Precision for class 1: 0.77
Logistic Regression Performance:

Accuracy: 80%
Precision for class 0: 0.94
Precision for class 1: 0.77

**Visualizations**
Boxplots and histograms are used to visualize the distribution of ApplicantIncome and LoanAmount.
Heatmap of correlations between features.
Decision Tree plot for visualization of the decision-making process.

**Conclusion**
The project demonstrates the use of different machine learning models and hyperparameter tuning techniques to predict loan approval status. Both Logistic Regression and the optimized Decision Tree model show similar accuracy, but the tuned Decision Tree model provides better interpretability with its visualization.
