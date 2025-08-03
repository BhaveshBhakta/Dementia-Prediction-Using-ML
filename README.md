## Chronic Kidney Disease Classification

### Project Overview

This project aims to classify **Chronic Kidney Disease (CKD)** based on various medical parameters. Utilizing a dataset containing features such as blood pressure, specific gravity, albumin, sugar, red blood cells, blood urea, serum creatinine, sodium, potassium, hemoglobin, white blood cell count, red blood cell count, and hypertension, the goal is to develop a machine learning model that can accurately predict the presence of CKD. This can aid in early diagnosis and management of the disease.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Chronic Kidney Disease](https://www.kaggle.com/datasets/abhia1999/chronic-kidney-disease)
  * **Size**: 400 entries, 14 columns
  * **Key Features**:
      * Bp, Sg, Al, Su, Rbc, Bu, Sc, Sod, Pot, Hemo, Wbcc, Rbcc, Htn.
  * **Approach**:
      * Data Cleaning: The dataset used appears to have already been preprocessed, as no missing values or duplicates were found in the loaded CSV.
      * Exploratory Data Analysis: Histograms, Boxplots, and Heatmaps were used for visualization to understand data distributions and correlations.
      * Label Encoding: Applied to all columns, including numerical ones and the target 'Class'.
      * Handling Class Imbalance with `SMOTE` (Synthetic Minority Over-sampling Technique) on the training data. This is important as the original dataset is imbalanced (250 Class 1 vs 150 Class 0).
      * Binary Classification: The target variable 'Class' indicates CKD (0) or no CKD (1).
      * Models Used:
          * Logistic Regression, Ridge Classifier, SVC, Random Forest, XGBoost, AdaBoost, Gradient Boosting, Bagging, Decision Tree.
  * **Best Accuracy**:
      * 100% with Random Forest Classifier and Gradient Boosting Classifier.
      * 98.8% with XGBoost Classifier, AdaBoost Classifier, Bagging Classifier, and Decision Tree Classifier.
      * The very high accuracies suggest that the medical parameters in this dataset are highly indicative of CKD, or potentially a form of data leakage.

-----

### Purpose and Applications

  * Assist medical professionals in **early diagnosis of Chronic Kidney Disease**.
  * Support screening programs to identify individuals at risk of CKD.
  * Facilitate timely intervention and management to slow disease progression.
  * Contribute to personalized medicine by identifying key indicators for individual patients.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/Dementia-Prediction-Using-ML.git
cd Dementia-Prediction-Using-ML
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn imbalanced-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Thoroughly investigating the very high accuracy to ensure no data leakage or overfitting is present, as such high performance on real-world medical data is rare.
  * Performing comprehensive hyperparameter tuning and cross-validation for all models to ensure robustness.
  * Exploring the impact of different feature selection or transformation techniques.
  * Adding explainability (e.g., SHAP or LIME) to understand which medical parameters are most critical for CKD diagnosis.
