# Logistic-regression-Random-forest-classifier

**Objective**:
The goal was to predict whether a tumor is **benign** or **malignant** based on diagnostic features using machine learning techniques, focusing on improving classification performance.

**Dataset**: Breast Cancer Wisconsin (Diagnostic) Data Set (https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data/data)

**Data Preprocessing**:
1. **Handling Missing Values**:
   - We identified and removed missing values from the `diagnosis` column, reducing the dataset to 271 samples from the original 569.
2. **Outlier Removal**:
   - Using the **IQR (Interquartile Range)** method, we removed extreme outliers, reducing the dataset further to ensure a more robust model.
3. **Handling Class Imbalance**:
   - The dataset was imbalanced, with more benign tumors. We applied **SMOTE** (Synthetic Minority Over-sampling Technique) to balance the classes, generating 192 instances each for benign and malignant tumors.
4. **Feature Scaling**:
   - Features were standardized using **StandardScaler** to ensure that all features had the same scale, preventing any one feature from dominating the model.

**Modeling**:
- We trained two models:
  - **Logistic Regression**, which achieved an accuracy of **65%**, with moderate precision and recall for both benign and malignant predictions.
  - **Random Forest**, which improved performance, yielding an accuracy of **73%** and higher precision, recall, and f1-scores, especially for malignant cases.
  
**Cross-Validation**:
- Logistic Regression was evaluated with **5-fold cross-validation**, producing an average score of **64%**, indicating moderate generalizability.
