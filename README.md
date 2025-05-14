# Data-Mining-Classification-Project
Machine learning classification project using multiple models and stacked ensemble on a cleaned and preprocessed mining dataset. Includes outlier removal, normalization, visualization, evaluation, and model comparison.

This project implements a full **machine learning pipeline** on a mining dataset, including preprocessing, visualization, model training, and evaluation. A **stacked ensemble model** was ultimately selected for its superior performance.

---

## 📊 Dataset & Context

- The dataset was sourced from an Excel file: `Mine_Dataset_edited.xlsx`, using the `Mine_Data` sheet.
- The task is **multi-class classification**, with the target column being `M`.

---

## 🔍 Project Workflow

### 1. Data Preprocessing
- Handled missing values using `.fillna()` with column means.
- Removed outliers using **Interquartile Range (IQR)** filtering.
- Normalized features using **Min-Max Scaling** for model compatibility.

### 2. Exploratory Data Analysis
- Histograms, KDE plots, boxplots for feature distributions.
- Heatmaps for correlation analysis.
- Skewness analysis using Pearson's Skewness Coefficient.

### 3. Feature Selection & Split
- Selected relevant features: `V`, `H`, and `S`.
- Split data using `train_test_split` with stratification.

### 4. Model Building & Evaluation
Trained and evaluated the following models:
- ✅ Random Forest Classifier  
- ✅ K-Nearest Neighbors (KNN)  
- ✅ Logistic Regression  
- ✅ Support Vector Machine (SVM)  
- ✅ Gradient Boosting Classifier  
- ✅ **Stacked Ensemble Model** (RF + GBC with Logistic Regression meta-model)

### 5. Evaluation Metrics
- Accuracy, Precision, Recall, F1-score
- Confusion Matrix
- 10-Fold Cross-Validation
- ROC-AUC curves (multi-class with OneVsRest)

---

## 🏆 Final Model

**Stacked Ensemble Model**  
- Accuracy: `54.8%`  
- Macro F1-score: `0.55`  
- Best performance across class metrics using ensemble learning.

---

## 💾 Exported Output
- Cleaned dataset exported to: `Mine_Cleaned_Data.xlsx`


