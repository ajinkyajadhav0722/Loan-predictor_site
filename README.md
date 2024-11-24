# Loan Approval Prediction using Machine Learning

## 📄 **Project Overview**

This project focuses on building a machine learning pipeline to predict loan approval status for customers based on their demographic and financial information. Using advanced data preprocessing techniques, feature engineering, and various machine learning models, the project aims to improve decision-making in loan approval processes.

---

## 📊 **Dataset Overview**

- **Source**: Kaggle dataset
- **Rows**: 614
- **Columns**: 13
- **Target Variable**: `Loan_Status` (1 for Approved, 0 for Not Approved)

---

## 🔧 **Steps and Methodology**

### 1️⃣ **Data Preprocessing**
- Handled missing values for both categorical and numerical columns:
  - Categorical: Imputed with mode values.
  - Numerical: Imputed with mean values.
- Dropped redundant columns (`Loan_ID`, `Dependents`) for cleaner analysis.
- Normalized and encoded categorical features using `OrdinalEncoder`.

### 2️⃣ **Exploratory Data Analysis (EDA)**
- **Visualizations**:
  - Bar plots to analyze the relationship between gender, marital status, and loan approval.
  - Distribution of numerical features such as `ApplicantIncome` and `LoanAmount`.
- **Insights**:
  - Higher loan approvals for urban areas and applicants with graduate-level education.
  - A strong correlation between `Credit_History` and loan approval.

### 3️⃣ **Feature Engineering**
- Created a cleaned dataset with numerical and encoded categorical features for model training.

### 4️⃣ **Modeling**
- Split data into training (80%) and testing (20%) sets.
- Trained and evaluated multiple machine learning models:
  - **Naive Bayes**:
    - Precision: 77.7%
    - Recall: 95.2%
    - Accuracy: 78.0%
  - **Support Vector Machine (SVM)**:
    - Best Hyperparameters (via Grid Search): `C=0.1`, `gamma=1`, `kernel='rbf'`
    - Precision: 68.3%
    - Recall: 100%
    - Accuracy: 68.3%
  - **XGBoost**:
    - Precision: 79.7%
    - Recall: 84.5%
    - Accuracy: 74.8%
  - **Decision Tree**:
    - Precision: 75.9%
    - Recall: 97.6%
    - Accuracy: 77.2%
  - **Random Forest**:
    - Precision: 77.2%
    - Recall: 97.6%
    - Accuracy: 77.2%

### 5️⃣ **Model Export**
- The best-performing model (Decision Tree Classifier) was exported using `joblib` for deployment.

---

## 📈 **Key Insights**
1. **Education Matters**: Graduate applicants have a higher likelihood of loan approval.
2. **Credit History is Crucial**: Applicants with a credit history (`Credit_History=1`) are significantly more likely to get their loans approved.
3. **Income Distribution**:
   - Applicants with moderate income levels (~`ApplicantIncome` between 4000 and 8000) have higher approval rates.
4. **Property Location**:
   - Loans are approved more frequently for applicants from urban areas compared to rural areas.

---

## 🛠️ **Technologies Used**
- **Languages**: Python
- **Libraries**: 
  - Data Processing: `pandas`, `numpy`
  - Visualization: `matplotlib`, `seaborn`
  - Machine Learning: `scikit-learn`, `XGBoost`
- **Deployment**: `joblib`

---

## 🚀 **How to Run**
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/loan-approval-prediction.git
