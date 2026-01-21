
# Robust Ensemble Feature Selection Technique with Explainable AI for Dyslexia Prediction Using Eye Movements

## 📌 Overview

This repository contains the implementation of the research work titled:

**“Robust Ensemble Feature Selection Technique with Explainable AI for Dyslexia Prediction Using Eye Movements”**

The project proposes a **robust ensemble feature selection framework** that combines traditional machine learning, explainable AI (XAI), and rank aggregation techniques to accurately predict dyslexia using **eye-movement data recorded during reading tasks**.

The approach focuses on:

* Optimal feature selection from high-dimensional eye-tracking data
* Improved classification accuracy with reduced feature set
* Transparency and interpretability using SHAP-based explainable AI

---

## 🎯 Objectives

* Extract meaningful **statistical, dispersion-based, and velocity-based eye-movement features**
* Rank features using multiple techniques:

  * Principal Component Analysis (PCA)
  * Random Forest Feature Importance (RF-FI)
  * Explainable AI using SHAP
* Aggregate feature rankings using **Robust Rank Aggregation (RRA)**
* Identify the **optimal feature subset** using accumulation effect analysis
* Build reliable dyslexia prediction models using ensemble machine learning classifiers

---

## 🧠 Methodology

### 1. Feature Extraction

A total of **57 eye-tracking features** are extracted:

* **Statistical features** (30)
* **Dispersion-based features** (16)
* **Velocity-based features** (11)

These features capture fixation behavior, saccadic movement, and reading dynamics relevant to dyslexia.

---

### 2. Feature Ordering Techniques

Three complementary feature ranking approaches are used:

| Method   | Description                                         |
| -------- | --------------------------------------------------- |
| PCA      | Unsupervised ranking based on variance contribution |
| RF-FI    | Supervised feature importance using Random Forest   |
| XAI-SHAP | Model-agnostic explainable feature contribution     |

---

### 3. Ensemble Rank Aggregation

Multiple ranked feature lists are fused using:

* Borda Count
* Robust Rank Aggregation (RRA)
* Markov Chain-based ranking
* Bayesian rank aggregation

Among these, **RRA** demonstrated superior robustness and consistency.

---

### 4. Accumulation Effect Analysis

Features are incrementally added based on ranking order to analyze:

* Classification accuracy vs number of features
* Optimal stopping point for feature inclusion

This process resulted in:

* **~58% feature reduction**
* **24 optimal features selected**

---

### 5. Classification Models

The selected features are evaluated using:

* Random Forest (RF)
* Support Vector Machine (SVM)
* K-Nearest Neighbors (KNN)
* Ensemble classifiers:

  * Soft Voting
  * **Stacking classifier (best performance)**

---

## 📊 Key Results

* **Best accuracy:** 96.36%
* **Optimal features:** 24 out of 57
* **Feature reduction:** ~58%
* **Best model:** Stacking classifier (RF + SVM + KNN with LR meta-classifier)

Velocity-based eye movement features were found to be the most influential indicators for dyslexia prediction.

---


## 🛠️ Requirements

* Python 3.8+
* NumPy
* Pandas
* Scikit-learn
* Matplotlib
* SHAP

Install dependencies using:

```bash
pip install numpy pandas scikit-learn matplotlib shap
```

---

## ▶️ How to Run

1. Clone the repository:

```bash
git clone https://github.com/your-username/dyslexia-feature-selection.git
```

2. Open the notebook or run the script:

```bash
python Dyslexia_PCA_Accumulation_RRA.py
```

3. Replace placeholder data loading with your actual feature dataset.

---

## 📚 Dataset

The eye-tracking dataset used in this study is sourced from:

> Nilsson Benfatto et al., *“Screening for dyslexia using eye tracking during reading”*, PLOS ONE, 2016.

The dataset includes recordings from **185 children (ages 9–10)** categorized as:

* High-Risk Dyslexia (HR-D)
* Low-Risk Dyslexia (LR-D)

---

## 📚 Dataset Availability

The dataset used in this project is not included in the repository due to its large size and usage restrictions.

This study uses the publicly available eye-tracking dataset from:

Nilsson Benfatto et al.,  
“Screening for dyslexia using eye tracking during reading”,  
PLOS ONE, 2016.

Researchers can request or download the dataset from the official source and place it in the appropriate data directory to reproduce the results.


## 🔍 Explainability

SHAP (SHapley Additive exPlanations) is used to:

* Interpret feature contributions
* Provide transparency in model decisions
* Identify key dyslexia indicators from eye movement patterns

---

## 🧪 Future Work

* Integration of multimodal data (EEG, neuroimaging, behavioral data)
* Adaptive and confidence-driven feature selection
* Real-time dyslexia screening using edge devices
* Extension to adult dyslexia datasets

---



