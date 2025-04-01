# Health_Insurance_Fraud_Detect_R-Paython
Predicting fraudulent health insurance claims using machine learning (Decision Tree &amp; Random Forest) with Python and R, including EDA, model evaluation, and feature importance analysis.

# Health Insurance Fraud Detection 

## 📌 Objective

This project aims to develop a predictive model that can accurately identify potentially fraudulent health insurance claims. By using machine learning algorithms like Decision Tree and Random Forest, we aim to support insurers in proactively flagging suspicious claims, thus reducing fraud-related losses.

---

## 💼 Why This Project Matters

Insurance fraud costs the industry billions each year, leading to higher premiums and distrust. By detecting fraud early:
- Insurers can reduce costs
- Investigators can prioritize cases
- Honest policyholders are protected
- Regulatory compliance and efficiency improve

---

## 📊 Dataset Description

The dataset used contains 1,000 anonymized insurance claim records, with features such as:

- **Demographics:** Age, gender, education, relationship
- **Policy Info:** Deductibles, coverage limits, premiums
- **Incident Details:** Time, severity, location, number of vehicles involved
- **Claim Information:** Property damage, injury, total claim amount
- **Fraud Label:** Binary label `Y`/`N` indicating if the claim was reported as fraud

---

## 🔁 Process and Workflow

The project was implemented in both **R** and **Python (Colab)** and includes:

### 1. Data Cleaning
- Replaced `"?"` with `NaN`
- Dropped rows with missing values
- Removed non-informative and high-cardinality fields like IDs and dates
- Encoded categorical variables

### 2. Exploratory Data Analysis (EDA)
- Visualized fraud distribution
- Analyzed claim amounts and severity
- Identified patterns in fraudulent behavior

### 3. Modeling
- Split data into training (70%) and testing (30%) sets
- Trained:
  - `DecisionTreeClassifier`
  - `RandomForestClassifier`
- Evaluated models using confusion matrix and classification report

### 4. Feature Importance
- Extracted top predictors from the Random Forest
- Visualized them to interpret fraud signals

---

## 📊 Model Performance & Evaluation

| Model           | Accuracy | Sensitivity | Specificity | Precision (Fraud=N) | Precision (Fraud=Y) | Notes                              |
|----------------|----------|-------------|-------------|----------------------|----------------------|-------------------------------------|
| Decision Tree  | 78.85%   | 88.79%      | 50.00%      | 83.74%               | 60.61%               | Better balance, interpretable      |
| Random Forest  | 76.92%   | 91.38%      | 35.00%      | 80.30%               | 58.33%               | Higher recall, but more false alarms |


---

## 📌 Key Insights

- **Fraudulent claims often involve higher total claim amounts** and more severe reported incidents.
- **Incident severity, property claim value, and number of vehicles involved** were among the top predictors of fraud.
- **Random Forest** showed stronger recall (91%)—useful for fraud detection where missing a fraud is costlier than a false alarm.
- Combining behavioral and contextual features (like hobbies and car model) improved prediction quality.



