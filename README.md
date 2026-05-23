# 🧬 GeneReveal — Genome-Based Disorder Prediction System
### Machine Learning Research Project · IT3080 · SLIIT 2025

![Python](https://img.shields.io/badge/Python-ML%20Pipeline-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML%20Models-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-Frontend-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![SLIIT](https://img.shields.io/badge/SLIIT-Year%203%20Sem%201-3B82F6?style=for-the-badge&logoColor=white)

---

## 📌 Overview

**GeneReveal** is a machine learning pipeline for predicting genetic disorders from high-dimensional genomic datasets (30,000+ features). The system applies advanced dimensionality reduction, class balancing, and multi-model comparison to deliver accurate disorder classifications through a full-stack web application.

> *"From 30,000+ genomic features to actionable clinical predictions — powered by PCA, SMOTE, and ensemble ML."*

---

## 🎯 My Contributions

As the **project lead**, I was responsible for:

- ✅ **ML Pipeline Architecture** — designed and implemented the end-to-end prediction pipeline
- ✅ **PCA Dimensionality Reduction** — reduced feature space from 37 → 18 features (~60% reduction) while preserving predictive performance
- ✅ **SMOTE Class Balancing** — addressed class imbalance in genomic data using Synthetic Minority Oversampling
- ✅ **Model Comparison** — evaluated and benchmarked Random Forest, SVM, and MLP classifiers
- ✅ **Hyperparameter Tuning** — optimised models using cross-validation and grid/random search
- ✅ **Team Leadership** — oversaw a 4-member team, coordinated modeling strategy and experimental pipelines

---

## 📊 Model Performance

| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| Random Forest | 79% | 0.81 | 0.79 | 0.80 |
| SVM | 74% | 0.76 | 0.74 | 0.75 |
| MLP (Neural Network) | 67% | 0.69 | 0.67 | 0.68 |
| **Best Model** | **79%** | | | |

*Evaluated using 5-fold cross-validation across multiple disorder classes.*

---

## 🔬 ML Pipeline

```
Raw Genomic Data (30K+ features)
        ↓
Data Preprocessing & Cleaning
        ↓
Feature Selection & Engineering
        ↓
PCA Dimensionality Reduction
  37 features → 18 features (~60% reduction)
        ↓
SMOTE Class Balancing
        ↓
Model Training & Comparison
  Random Forest | SVM | MLP
        ↓
Cross-Validation & Hyperparameter Tuning
        ↓
Best Model Selection (Random Forest — 79%)
        ↓
FastAPI Backend → React Frontend
```

---

## 🧪 Key Techniques

### PCA — Principal Component Analysis
- Reduced feature dimensionality from **37 → 18 components**
- Achieved **~60% reduction** while preserving predictive variance
- Eliminated multicollinearity in high-dimensional genomic features
- Significantly reduced model training time and overfitting risk

### SMOTE — Synthetic Minority Oversampling Technique
- Addressed class imbalance across multiple disorder classes
- Generated synthetic genomic samples for underrepresented disorders
- Improved model recall and F1-score across all classifiers
- Applied before cross-validation to prevent data leakage

### Model Comparison Framework
```python
models = {
    'Random Forest': RandomForestClassifier(n_estimators=200, max_depth=15),
    'SVM':           SVC(kernel='rbf', C=10, probability=True),
    'MLP':           MLPClassifier(hidden_layer_sizes=(256, 128), max_iter=500)
}
# Evaluated with StratifiedKFold(n_splits=5)
# Metrics: accuracy, precision, recall, F1-score
```

---

## 🏗️ System Architecture

```
GeneReveal System
├── ML Pipeline (Python)
│   ├── preprocessing.py      ← Data cleaning & feature engineering
│   ├── pca_reduction.py      ← PCA dimensionality reduction
│   ├── smote_balancing.py    ← Class balancing
│   ├── model_training.py     ← RF, SVM, MLP training
│   ├── evaluation.py         ← Cross-validation & metrics
│   └── model_export.py       ← Save trained models
├── Backend (FastAPI)
│   ├── main.py               ← API entry point
│   ├── predict.py            ← Prediction endpoint
│   └── models/               ← Serialised ML models
├── Frontend (React)
│   ├── src/components/       ← UI components
│   └── src/App.jsx           ← Main application
└── Database (MySQL)
    └── patient_records       ← Prediction history
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **ML** | Scikit-learn, Pandas, NumPy, Matplotlib |
| **Dimensionality Reduction** | PCA (sklearn.decomposition) |
| **Class Balancing** | SMOTE (imbalanced-learn) |
| **Models** | Random Forest, SVM, MLP |
| **Backend** | FastAPI, Python 3.10 |
| **Frontend** | React.js, Chart.js |
| **Database** | MySQL |
| **Visualisation** | Matplotlib, Seaborn |

---

## 🚀 Getting Started

### Prerequisites
```
Python 3.8+
Node.js 16+
MySQL
```

### Backend Setup
```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload --port 8000
```

### Frontend Setup
```bash
cd frontend
npm install
npm run dev
```

### Run ML Pipeline
```bash
# Preprocess and train
python preprocessing.py
python pca_reduction.py
python model_training.py

# Or use the notebook
jupyter notebook notebooks/GeneReveal_Pipeline.ipynb
```

---

## 📁 Repository Structure

```
genereveal-genome-prediction/
├── README.md
├── backend/
│   ├── main.py
│   ├── predict.py
│   ├── requirements.txt
│   └── models/
│       └── rf_model.pkl
├── frontend/
│   ├── src/
│   └── package.json
├── ml_pipeline/
│   ├── preprocessing.py
│   ├── pca_reduction.py
│   ├── smote_balancing.py
│   ├── model_training.py
│   └── evaluation.py
├── notebooks/
│   └── GeneReveal_Pipeline.ipynb
└── results/
    ├── model_comparison.png
    ├── pca_variance.png
    └── confusion_matrices.png
```

---

## 📋 Module Details

- **Module:** IT3080 — Research Project
- **Year:** Year 3, Semester 1 · Jun–Oct 2025
- **Role:** Team Leader · 4-member group
- **Institute:** Sri Lanka Institute of Information Technology (SLIIT)

---

## 👩‍💻 Developer

**Ranushi Amanda (Hasangani WRA)** · IT23224384 · Team Leader

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Ranushi%20Amanda-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ranushi-amanda-b135572ba)
[![GitHub](https://img.shields.io/badge/GitHub-RanushiAmanda-100000?style=flat&logo=github&logoColor=white)](https://github.com/RanushiAmanda)
[![Blog](https://img.shields.io/badge/Blog-InsightForge-FF5722?style=flat&logo=blogger&logoColor=white)](https://ranu001coding.blogspot.com)

---

> *"Reducing 30,000+ genomic features to 18 meaningful components — then letting the data speak."*
