# 🫁 Chronic Kidney Disease Classification
### SENG 352 — Data Analysis Term Project | Çankaya University

![Python](https://img.shields.io/badge/Python-3.14-blue?logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.8.0-orange?logo=scikit-learn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📌 Project Overview

This project applies machine learning techniques to classify patients as having **Chronic Kidney Disease (CKD)** or **not**, using clinical measurements. Six different ML models are trained, evaluated, and compared using cross-validation and multiple metrics.

| | |
|---|---|
| **Dataset** | Chronic Kidney Disease Dataset |
| **Source** | [Kaggle — CK Disease](https://www.kaggle.com/datasets/mansoordaku/ckdisease) |
| **Samples** | 400 patients |
| **Features** | 24 clinical features |
| **Task** | Binary Classification (ckd / notckd) |

---

## 📊 Results Summary

| Model | CV Accuracy | Test Accuracy | ROC-AUC | F1-Score |
|---|---|---|---|---|
| Logistic Regression | 99.06% | 98.75% | 1.000 | 0.9899 |
| K-Nearest Neighbors | 95.94% | 96.25% | 1.000 | 0.9691 |
| Decision Tree | 96.56% | 97.50% | 0.973 | 0.9800 |
| SVM (RBF) | 99.38% | 97.50% | 1.000 | 0.9796 |
| **Random Forest ⭐** | **99.06%** | **100%** | **1.000** | **1.000** |
| Gradient Boosting | 98.44% | 98.75% | 1.000 | 0.9899 |

> ✅ **Random Forest** achieved perfect **100% test accuracy** and **1.000 ROC-AUC**.

---

## 🗂️ Project Structure

```
📦 kidney-disease-classification/
├── 📓 kidney_disease_project.ipynb   ← Main Jupyter notebook
├── 📄 kidney_disease.csv             ← Dataset
├── 📄 README.md                      ← This file
└── 📊 figures/
    ├── fig1_missing_heatmap.png
    ├── fig2_numeric_distributions.png
    ├── fig3_categorical_distributions.png
    ├── fig4_correlation_heatmap.png
    ├── fig5_model_comparison.png
    ├── fig6_confusion_matrices.png
    └── fig7_roc_curves.png
```

---

## 🔬 Dataset Features

| Feature | Description | Type |
|---|---|---|
| `age` | Age of patient | Numeric |
| `bp` | Blood pressure | Numeric |
| `sg` | Specific gravity | Numeric |
| `al` | Albumin | Numeric |
| `su` | Sugar | Numeric |
| `rbc` | Red blood cells | Categorical |
| `pc` | Pus cell | Categorical |
| `pcc` | Pus cell clumps | Categorical |
| `ba` | Bacteria | Categorical |
| `bgr` | Blood glucose random | Numeric |
| `bu` | Blood urea | Numeric |
| `sc` | Serum creatinine | Numeric |
| `sod` | Sodium | Numeric |
| `pot` | Potassium | Numeric |
| `hemo` | Hemoglobin | Numeric |
| `pcv` | Packed cell volume | Numeric |
| `wc` | White blood cell count | Numeric |
| `rc` | Red blood cell count | Numeric |
| `htn` | Hypertension | Categorical |
| `dm` | Diabetes mellitus | Categorical |
| `cad` | Coronary artery disease | Categorical |
| `appet` | Appetite | Categorical |
| `pe` | Pedal edema | Categorical |
| `ane` | Anemia | Categorical |

---

## ⚙️ Pipeline

```
Raw Data
   ↓
Data Quality Assessment
  • Fix dirty labels (whitespace/tab noise)
  • Convert mistyped numeric columns (pcv, wc, rc)
  • Strip whitespace from categorical columns
   ↓
Exploratory Data Analysis
  • Missing value heatmap
  • Feature distributions by class
  • Categorical feature analysis
  • Correlation matrix
   ↓
Pre-processing
  • Numeric  → Median imputation + StandardScaler
  • Categorical → OrdinalEncoder + Mode imputation
  • 80/20 stratified train/test split
   ↓
Modeling (Baseline → Improved → Advanced)
  • Logistic Regression (baseline)
  • K-Nearest Neighbors
  • Decision Tree
  • SVM (RBF kernel)
  • Random Forest
  • Gradient Boosting
   ↓
Evaluation
  • 5-Fold Stratified Cross-Validation
  • Confusion Matrix
  • ROC-AUC Curve
  • Classification Report
```

---

## 🚀 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/berkay-bostan/Kidney_Disease.git
cd kidney-disease-classification
```

### 2. Create and activate virtual environment
```bash
python3 -m venv kidney_env
source kidney_env/bin/activate      # Mac/Linux
kidney_env\Scripts\activate         # Windows
```

### 3. Install dependencies
```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter jinja2
```

### 4. Launch the notebook
```bash
jupyter notebook kidney_disease_project.ipynb
```

---

## 🛠️ Technologies Used

- **Python 3.14**
- **pandas** — data manipulation
- **numpy** — numerical operations
- **matplotlib / seaborn** — visualization
- **scikit-learn** — machine learning models & evaluation
- **Jupyter Notebook** — interactive development

---

## 👥 Team

| # | Name | Student ID | Role |
|---|---|---|---|
| 1 |Senanur Çinkil | 202228011|Leader |
| 2 | Berkay Bostan| 202228401| |



