<div align="center">

# 🩺 Diabeta AI

### Intelligent Diabetes Prediction & Feature Importance Analysis

**Predict. Compare. Understand.**

An interactive Machine Learning project comparing Random Forest and XGBoost for diabetes prediction and model explainability.

<br>

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-Web_App-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Machine_Learning-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-Boosting-006600?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Academic_Project-00A86B?style=for-the-badge)

<br>

**🌲 Random Forest · ⚡ XGBoost · 📊 Model Analytics · 🔍 Feature Importance**

</div>

---

## 🌟 About the Project

**Diabeta AI** is a Machine Learning web application developed to study diabetes prediction using two ensemble-learning algorithms: **Random Forest and XGBoost**.

The project explores how clinical measurements can be used to classify records into two target categories and compares how both models perform on the same dataset.

Beyond prediction, Diabeta AI focuses on **model explainability** by visualizing feature importance and helping users understand which variables the trained models rely on.

The application combines machine learning, data analysis, interactive charts, and an intuitive web interface in one project.

> 🎯 **Our mission:** Make Machine Learning predictions easier to explore, compare, and understand.

---

## ✨ Features

<table>
<tr>
<td width="50%">

### 🏠 Interactive Dashboard
Explore dataset information, target distribution, and model performance through visual summaries.

</td>
<td width="50%">

### 🩺 Diabetes Prediction
Enter clinical measurements and compare predictions from Random Forest and XGBoost.

</td>
</tr>

<tr>
<td width="50%">

### 📊 Model Analytics
Compare Accuracy, Precision, Recall, F1-score, and ROC-AUC.

</td>
<td width="50%">

### 🔍 Feature Importance
Explore and compare the features used by both trained models.

</td>
</tr>

<tr>
<td width="50%">

### 📈 Interactive Visualizations
View confusion matrices, ROC curves, feature-importance charts, and dataset distributions.

</td>
<td width="50%">

### 📁 Dataset Explorer
Inspect the dataset, review descriptive statistics, and explore selected variables.

</td>
</tr>
</table>

---

## 🧠 Machine Learning Architecture

Diabeta AI follows an end-to-end Machine Learning workflow.

```text
                  ┌─────────────────────┐
                  │   DIABETES DATASET  │
                  │    diabetes.csv     │
                  └──────────┬──────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │ DATA PREPROCESSING  │
                  │ Validation & Impute │
                  └──────────┬──────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │  TRAIN / TEST SPLIT│
                  │       80 / 20       │
                  └──────────┬──────────┘
                             │
                 ┌───────────┴───────────┐
                 ▼                       ▼
       ┌──────────────────┐   ┌──────────────────┐
       │  RANDOM FOREST   │   │     XGBOOST      │
       │                  │   │                  │
       │ Decision Trees   │   │ Boosted Trees    │
       └─────────┬────────┘   └─────────┬────────┘
                 │                      │
                 └──────────┬───────────┘
                            ▼
                 ┌─────────────────────┐
                 │  MODEL EVALUATION   │
                 │ Accuracy, F1, AUC   │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ FEATURE IMPORTANCE  │
                 │  Model Comparison   │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │   DIABETA AI WEB    │
                 │     APPLICATION     │
                 └─────────────────────┘
```

---

## 🌲 Machine Learning Models

### 1. Random Forest

Random Forest is an ensemble-learning algorithm that builds multiple decision trees and combines their predictions.

**Role in this project:**
- Predict diabetes outcomes.
- Evaluate classification performance.
- Calculate built-in feature importance.
- Serve as a model for comparison with XGBoost.

### 2. XGBoost

XGBoost is a gradient-boosting algorithm that builds trees sequentially, with each stage improving the overall ensemble.

**Role in this project:**
- Generate diabetes predictions.
- Evaluate classification performance.
- Calculate built-in feature importance.
- Compare its results with Random Forest.

### ⚖️ Why Compare Both Models?

Both models can learn nonlinear relationships from tabular data, but they use different ensemble-learning strategies.

Comparing them helps us study their performance and understand whether their feature-importance rankings differ.

---

## 📂 Dataset Information

The project uses the supplied **`diabetes.csv`** dataset.

| Property | Description |
|---|---|
| Dataset file | `diabetes.csv` |
| Total records | 768 |
| Input features | 8 |
| Target variable | `Outcome` |
| Problem type | Binary classification |
| Data format | CSV |

### 🔬 Input Features

| Feature | Description |
|---|---|
| `Pregnancies` | Number of pregnancies |
| `Glucose` | Plasma glucose measurement |
| `BloodPressure` | Diastolic blood pressure measurement |
| `SkinThickness` | Skin-fold thickness measurement |
| `Insulin` | Insulin measurement |
| `BMI` | Body Mass Index |
| `DiabetesPedigreeFunction` | Dataset-provided diabetes pedigree function |
| `Age` | Age in years |

### 🎯 Target Variable: `Outcome`

| Value | Meaning |
|---|---|
| `0` | No diabetes indicated by the dataset label |
| `1` | Diabetes indicated by the dataset label |

**Data preprocessing:** Selected zero-coded clinical measurements are treated as missing values and replaced using medians calculated from the training data.

> The dataset is used for an academic Machine Learning demonstration. Its representativeness and clinical suitability have not been independently validated.

---

## 📊 Model Evaluation

The application evaluates both models using the same held-out test dataset.

| Metric | What It Measures |
|---|---|
| Accuracy | Proportion of all predictions that are correct |
| Precision | Proportion of positive predictions that are correct |
| Recall | Proportion of actual positive cases identified |
| F1-score | Harmonic mean of Precision and Recall |
| ROC-AUC | Ability to distinguish between the two target classes |

Additional visualizations include:

- 📉 ROC curves
- 🎯 Confusion matrices
- 📊 Model comparison charts
- 🔍 Feature-importance rankings

**Note:** Performance values are calculated when the application trains the models. Actual results may differ with changes to the dataset, preprocessing, model parameters, or evaluation split.

---

## 🔍 Feature Importance & Explainability

Feature importance helps show which input variables contribute to the trained models' predictions.

Diabeta AI compares the built-in importance scores from both algorithms.

The comparison helps answer questions such as:

- Which features rank highest in Random Forest?
- Which features rank highest in XGBoost?
- Do both models produce similar rankings?
- Which features receive different importance rankings across the models?

Feature importance describes **model behaviour, not causation**. An important feature is not necessarily a cause of diabetes.

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Streamlit | Interactive web application |
| Pandas | Dataset handling and analysis |
| NumPy | Numerical processing |
| Scikit-learn | Random Forest, preprocessing, splitting, and evaluation |
| XGBoost | Gradient-boosted classification |
| Plotly | Interactive charts and visualizations |

---

## 📁 Project Structure

```text
Diabeta-AI/
│
├── app.py
│
├── README.md
├── requirements.txt
├── run_project.bat
│
├── diabetes.csv
│
├── data/
│   └── diabetes.csv
│
└── models/
    └── README.txt
```

**Important:** The application loads the dataset from `data/diabetes.csv`. The root-level `diabetes.csv` is not required by the current application.

The models are trained automatically when the application starts; pre-trained model files are not required.

---

## 🚀 Installation & Setup

Follow these steps to run Diabeta AI on your local computer.

### ✅ Prerequisites

Install Python and ensure it is accessible from your terminal.

### Step 1 — Download the Project

Download and extract the project ZIP file.

### Step 2 — Open the Project

Open the extracted project folder using **VS Code or Antigravity**.

### Step 3 — Open the Terminal

Select:

`Terminal → New Terminal`

Ensure the terminal is in the folder containing `app.py`.

### Step 4 — Create a Virtual Environment

```powershell
python -m venv venv
```

### Step 5 — Activate the Environment

For Windows PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

If activation is blocked, use Command Prompt:

```bat
venv\Scripts\activate.bat
```

### Step 6 — Install Dependencies

```powershell
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### Step 7 — Launch the Website

```powershell
python -m streamlit run app.py
```

Using `python -m streamlit` also works when the standalone `streamlit` command is not recognized by PowerShell.

### Step 8 — Open Diabeta AI

Open the local URL shown in your terminal. It is normally:

**http://localhost:8501**

🎉 Your website is now running locally!

---

## 🖥️ Website Pages

| Page | Function |
|---|---|
| 🏠 Dashboard | Dataset summary and model performance |
| 🩺 Prediction | Enter clinical values and compare predictions |
| 📊 Model Analytics | Metrics, confusion matrices, and ROC curves |
| 🔍 Feature Importance | Compare model feature-importance scores |
| 📁 Dataset Explorer | Preview data and explore distributions |
| ℹ️ About | Project objective, algorithms, and methodology |

---

## 🎯 Project Objectives

1. Develop a Machine Learning system for diabetes-outcome classification.
2. Implement Random Forest and XGBoost.
3. Evaluate both models using standard classification metrics.
4. Compare their feature-importance rankings.
5. Build an interactive website to demonstrate model outputs and analytics.
6. Present model limitations and emphasize responsible use.

---

## 🔮 Future Enhancements

Potential future improvements include:

- 🧠 Add SHAP explanations for individual predictions.
- 🔁 Introduce stratified cross-validation for more robust evaluation.
- 📄 Add downloadable model evaluation reports.
- 🎨 Further improve visual design and accessibility.
- 🌐 Deploy the application to a suitable hosting platform.
- 🧪 Validate the models on an independent, representative dataset.
- ⚙️ Add automated testing and a reproducible preprocessing pipeline.

These are proposed enhancements and should not be considered implemented features unless added to the code.

---

## ⚠️ Responsible Use & Disclaimer

**Diabeta AI is an academic Machine Learning project. It is not a medical diagnostic system.**

The outputs depend on the supplied dataset and the trained models. They must not be used to diagnose diabetes, make treatment decisions, or replace professional healthcare advice.

Any real-world medical application would require appropriate clinical validation, independent testing, privacy safeguards, and qualified oversight.

---

<div align="center">

## 🩺 Diabeta AI

**Predict. Compare. Understand.**

Built with Python, Streamlit, Random Forest and XGBoost.

<br>

*Exploring Machine Learning and explainable prediction through an interactive application.*

</div>