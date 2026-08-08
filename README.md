# 🏦 Loan Approval Prediction

A machine learning project that predicts whether a loan application will be approved based on applicant and loan-related information.

## 📌 Project Overview

Loan approval is an important decision for financial institutions. This project uses **Machine Learning** to analyze applicant information and predict the likelihood of loan approval.

The project focuses on data preprocessing, categorical encoding, feature engineering, regularization, and model evaluation.

## 🎯 Objective

The main objective of this project is to:

* Analyze loan application data
* Perform data cleaning and preprocessing
* Encode categorical features
* Engineer useful features
* Train a machine learning model
* Evaluate model performance
* Predict whether a loan application will be approved

## 📊 Dataset

The dataset contains applicant and loan-related features such as:

* Employment Status
* Marital Status
* Loan Purpose
* Property Area
* Gender
* Employer Category
* DTI Ratio
* Credit Score
* Other applicant and loan-related attributes

### Target Variable

`Loan_Approved`

* `1` → Loan Approved
* `0` → Loan Not Approved

## ⚙️ Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## 🔧 Data Preprocessing

The following preprocessing techniques were applied:

* Handling missing values
* Checking and removing duplicate records
* Separating numerical and categorical features
* One-Hot Encoding of categorical variables
* Feature scaling where required
* Train-test split

For categorical variables, `OneHotEncoder` was used with:

```python
OneHotEncoder(
    drop="first",
    sparse_output=False,
    handle_unknown="ignore"
)
```

Using `drop="first"` helps avoid the dummy-variable trap.

## 🧠 Feature Engineering

Additional features were created to capture possible non-linear relationships.

For example:

```python
df["DTI_Ratio_sq"] = df["DTI_Ratio"] ** 2
df["Credit_Score_sq"] = df["Credit_Score"] ** 2
```

These squared features allow the model to capture relationships that may not be purely linear.

## 🤖 Machine Learning

The project explores regularized linear classification techniques, including:

* Logistic Regression
* L1 Regularization
* L2 Regularization
* Lasso-style feature selection
* Elastic Net
* Cross-Validation

The final model can be selected based on cross-validation and test-set performance.

## 📈 Model Evaluation

The model can be evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix
* ROC-AUC

These metrics help determine how effectively the model predicts loan approval.

## 📁 Project Structure

```text
Loan-Approval/
│
├── Data/
│   └── loan_dataset.csv
│
├── notebooks/
│   └── Loan_Approval.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/VinayShinde-cmd/Loan-Approval.git
```

### 2. Navigate to the project

```bash
cd Loan-Approval
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

Open the notebook from the `notebooks` folder and run the cells.

## 📌 Key Learning Outcomes

Through this project, I practiced:

* Data preprocessing
* Exploratory Data Analysis
* Categorical encoding
* Feature engineering
* Logistic Regression
* Regularization
* Cross-validation
* Model evaluation
* Machine Learning workflow
* Git and GitHub project management

## 🔮 Future Improvements

* Hyperparameter tuning
* Compare additional classification algorithms
* Handle class imbalance if present
* Deploy the model as a web application
* Create an interactive loan approval prediction interface

## 👨‍💻 Author

**Vinay Shinde**

B.Tech Computer Science Student | Machine Learning Enthusiast
