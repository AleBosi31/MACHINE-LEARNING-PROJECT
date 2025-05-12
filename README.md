# 🩺 Predicting Cardiovascular Diseases with Machine Learning

**Authors**: Alessandro Bosi, Denis Bugaenco, Eleonora Zullo  
**University**: Università degli Studi di Milano-Bicocca – MSc Data Science  
**Exam Session**: January 2024  

## 🧠 Abstract

Cardiovascular diseases (CVDs) are the leading cause of death worldwide. In this project, we explore the potential of **machine learning models** to predict whether a patient is likely to develop cardiovascular disease based on clinical and lifestyle data. Using the **KNIME platform**, we preprocess a real-world dataset, apply multiple classification models, and evaluate their effectiveness using metrics like **accuracy**, **recall**, **precision**, and **AUC**.

---

## 📊 Dataset

- Source: [Kaggle – Cardiovascular Disease Dataset](https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset)
- Size: 70,000 patients  
- Variables:
  - Demographics (age, gender, height, weight)
  - Clinical data (blood pressure, cholesterol, glucose)
  - Lifestyle (smoking, alcohol, physical activity)
  - Target: `cardio` (0 = no disease, 1 = disease)

---

## 🧹 Data Preprocessing

1. **Missing/Duplicates**: Removed duplicates (no missing values found)
2. **Transformations**:
   - Age converted from days to years
   - Created new variable: **BMI**
3. **Outlier Handling**: Used IQR filtering (with k=2) to remove unrealistic values
4. **Normalization**: Scaled all numeric variables between 0 and 1
5. **Feature Selection**: Selected most informative features based on correlation:
   - `ap_hi`, `ap_lo`, `cholesterol`, `age_y`, `BMI`

---

## 🤖 Machine Learning Models

- **Random Forest**
- **Logistic Regression**
- **Naive Bayes**

All models were evaluated using **10-fold cross-validation** and tested on a 30% hold-out set.

### ✅ Best model: Random Forest
- **Mean Accuracy**: 72.8%
- **AUC**: 0.7656
- **Positive Recall**: 0.677
- **Positive Precision**: 0.742

---

## 📈 Evaluation Metrics

- **Confusion Matrix**
- **Precision & Recall (for both classes**
