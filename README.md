# 📊 Customer Churn Prediction & Analysis

## 📌 Project Overview

Customer churn is one of the major challenges faced by telecom companies. Losing customers can directly impact revenue and increase customer acquisition costs.

This project focuses on **analyzing customer churn behavior and building machine learning models to predict whether a customer is likely to churn or stay**.

The project follows an end-to-end data science workflow including:

* Data loading
* Data cleaning
* Exploratory Data Analysis (EDA)
* Correlation analysis
* Feature importance analysis
* Data preprocessing
* Feature scaling
* PCA dimensionality reduction
* Multiple machine learning models
* Model evaluation
* ROC-AUC analysis
* Hyperparameter tuning
* Churn prediction
* Business insights

---

## 🎯 Objectives

The main objectives of this project are:

1. Understand customer churn patterns.
2. Identify factors associated with customer churn.
3. Explore relationships between customer characteristics and churn.
4. Build multiple machine learning classification models.
5. Compare model performance.
6. Tune the XGBoost model using GridSearchCV.
7. Predict whether an individual customer is likely to churn.
8. Generate business insights that can support customer retention strategies.

---

## 📂 Dataset

The project uses the **Telco Customer Churn** dataset.

The dataset contains customer-level information related to:

* Customer demographics
* Account information
* Contract type
* Internet service
* Tenure
* Monthly charges
* Total charges
* Churn status

### Target Variable

**Churn**

* `Yes` → Customer has churned
* `No` → Customer has stayed

---

## 🛠️ Technologies & Libraries

### Programming Language

* Python

### Data Analysis

* Pandas
* NumPy

### Data Visualization

* Matplotlib
* Seaborn

### Machine Learning

* Scikit-learn
* XGBoost

### Techniques Used

* Label Encoding
* Standardization
* PCA
* Train-Test Split
* Cross-Validation
* GridSearchCV

---

## 🔄 Project Workflow

```text
Dataset
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Correlation Analysis
   ↓
Feature Importance
   ↓
Train-Test Split
   ↓
Feature Scaling
   ↓
PCA
   ↓
Machine Learning Models
   ↓
Model Evaluation
   ↓
Hyperparameter Tuning
   ↓
Churn Prediction
   ↓
Business Insights
```

---

## 🧹 Data Cleaning

The following preprocessing steps were performed:

* Removed the `customerID` column because it is an identifier rather than a predictive feature.
* Converted `TotalCharges` into numeric format.
* Invalid/missing values generated during conversion were handled.
* Missing `TotalCharges` values were replaced using the median.
* Categorical variables were converted into numerical values using `LabelEncoder`.

---

## 📈 Exploratory Data Analysis

Several visualizations were created to understand customer behavior.

### 1. Churn Distribution

Analyzed the overall distribution of customers who stayed versus customers who churned.

### 2. Contract Type vs Churn

Examined how different contract types relate to customer churn.

### 3. Internet Service vs Churn

Analyzed churn behavior across different internet service types.

### 4. Monthly Charges Distribution

Studied the distribution of customers' monthly charges.

### 5. Tenure vs Churn

Compared customer tenure between churned and non-churned customers.

### 6. Correlation Heatmap

A correlation matrix was created to understand relationships between numerical features.

---

## ⭐ Feature Importance

An `ExtraTreesClassifier` was used to estimate feature importance.

The analysis helps identify which customer attributes contribute more strongly to predicting churn.

The notebook particularly highlights:

* Contract type
* Monthly charges
* Tenure
* Internet service

as important factors associated with customer churn.

---

## 🤖 Machine Learning Models

The project evaluates multiple classification algorithms:

| Model               | Purpose                              |
| ------------------- | ------------------------------------ |
| Logistic Regression | Linear classification baseline       |
| Decision Tree       | Tree-based classification            |
| Random Forest       | Ensemble tree-based model            |
| SVM Linear          | Linear support vector classification |
| SVM RBF             | Non-linear classification            |
| XGBoost             | Gradient boosting classification     |

---

## 📏 Model Evaluation

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix
* ROC Curve
* ROC-AUC

### Confusion Matrix

Confusion matrices were generated for each model to analyze:

* True Positives
* True Negatives
* False Positives
* False Negatives

### ROC Curve

ROC analysis was performed to evaluate the classification performance of the selected XGBoost model.

---

## 🚀 Hyperparameter Tuning

`GridSearchCV` with 5-fold cross-validation was used to tune the XGBoost model.

The parameters explored were:

```python
n_estimators = [100, 200, 300]
max_depth = [3, 5, 7]
```

The best parameter combination and cross-validation score were obtained through grid search.

---

## 🔮 Predictive Test

A final predictive test was performed using an SVM RBF model.

The model predicts whether a sample customer is likely to:

```text
⚠️ Churn
```

or

```text
✅ Stay
```

---

## 💡 Business Insights

Based on the analysis performed in the notebook:

* Customers with **month-to-month contracts** show higher churn behavior.
* **Higher monthly charges** are associated with increased churn behavior.
* Customers with **longer tenure** show greater loyalty.
* **Fiber optic users** show higher churn behavior in the analyzed dataset.
* **Contract type** is identified as one of the important predictors of churn.

These insights can help telecom businesses focus on customer retention and identify customers who may be at higher risk of leaving.

---

## 📌 Business Applications

A churn prediction system can potentially help telecom companies:

* Identify customers at risk of churn.
* Prioritize retention campaigns.
* Develop targeted offers.
* Improve customer experience.
* Reduce customer loss.
* Support data-driven retention decisions.
* Protect recurring revenue.

---

## 📁 Project Structure

```text
Telco-Customer-Churn/
│
├── Telco_Customer_Churn.ipynb
├── Telco-Customer-Churn.csv
└── README.md
```

---

## ▶️ How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/your-username/Telco-Customer-Churn.git
```

### 2. Navigate to the project directory

```bash
cd Telco-Customer-Churn
```

### 3. Install required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost jupyter
```

### 4. Open the notebook

```bash
jupyter notebook
```

Open:

```text
Telco_Customer_Churn.ipynb
```

### 5. Dataset Path

The notebook currently loads the dataset using:

```python
pd.read_csv("/content/Telco-Customer-Churn.csv")
```

If running locally, update the path according to the location of your CSV file.

---

## 📊 Key Skills Demonstrated

This project demonstrates practical experience in:

* Python
* Data Cleaning
* Exploratory Data Analysis
* Data Visualization
* Feature Engineering
* Classification
* Machine Learning
* Model Comparison
* Model Evaluation
* Hyperparameter Tuning
* PCA
* Business Analytics
* Customer Churn Analysis

---

## 👩‍💻 Author

**Gaytri Farde**

Aspiring Data Analyst | Data Science & AI/ML

**Skills:** Python • SQL • Power BI • Tableau • Machine Learning • Data Analysis

---

## ⭐ Project Highlights

> An end-to-end machine learning project that analyzes telecom customer behavior and builds classification models to predict customer churn.

If you found this project useful, feel free to ⭐ the repository.
