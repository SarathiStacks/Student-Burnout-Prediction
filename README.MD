# 🎓 Student Burnout Risk Prediction using Support Vector Machines

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.11-blue?logo=python">
  <img src="https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?logo=scikitlearn">
  <img src="https://img.shields.io/badge/Status-Completed-success">
  <img src="https://img.shields.io/badge/License-MIT-green">
</p>

---

# 📌 Project Overview

Student burnout has become one of the most significant challenges in modern education due to increasing academic pressure, stress, lifestyle imbalance, financial concerns, and mental health issues.

This project develops a **Machine Learning classification system** capable of predicting a student's burnout risk level using **Support Vector Machines (SVM)**.

Rather than simply training a model, this project follows a complete machine learning pipeline including:

- Data Exploration
- Feature Engineering
- Data Preprocessing
- Feature Scaling
- Model Training
- Model Evaluation
- Handling Class Imbalance
- Comparison of Multiple SVM Variants
- Business-Oriented Model Selection

---

# 🎯 Objectives

The primary objectives of this project are:

- Predict student burnout risk using demographic, academic and psychological attributes.
- Understand the working principles of Support Vector Machines.
- Compare Linear SVM and RBF Kernel SVM.
- Investigate the impact of class imbalance on model performance.
- Improve minority class detection using balanced class weights.
- Evaluate models using multiple performance metrics instead of relying only on accuracy.

---

# 🧠 Machine Learning Workflow

```text
Dataset
      │
      ▼
Exploratory Data Analysis (EDA)
      │
      ▼
Data Cleaning & Feature Selection
      │
      ▼
Encoding Categorical Variables
      │
      ▼
Train-Test Split
      │
      ▼
Feature Scaling
      │
      ▼
Linear SVM
      │
      ▼
Balanced Linear SVM
      │
      ▼
RBF Kernel SVM
      │
      ▼
Performance Evaluation
      │
      ▼
Model Comparison & Final Selection
```

---

# 📂 Dataset

The dataset contains student information collected across multiple dimensions.
Note: The original dataset contains approximately 1 million records. Since classical Support Vector Machines have high computational complexity on very large datasets, a reproducible random sample of 50,000 observations (random_state=42) was used for model development and evaluation.

### Features include:

### 👤 Demographics

- Age
- Gender
- Academic Year

### 📚 Academic Factors

- Study Hours per Day
- Exam Pressure
- Academic Performance

### 🧠 Mental Health Indicators

- Stress Level
- Anxiety Score
- Depression Score

### 🏃 Lifestyle Factors

- Sleep Hours
- Physical Activity
- Social Support

### 💻 Behavioral Factors

- Screen Time
- Internet Usage

### 🌍 Environmental Factors

- Financial Stress
- Family Expectations

### 🎯 Target Variable

```
Risk Level

• Low
• Medium
• High
```

---

# ⚙️ Data Preprocessing

The following preprocessing steps were performed before model training:

- Removal of target leakage features
- One-Hot Encoding for Gender
- Ordinal Encoding for Risk Level
- Train-Test Split (80:20)
- Feature Standardization using StandardScaler

Feature scaling was performed **after splitting** the dataset to avoid data leakage.

---

# 📊 Exploratory Data Analysis

EDA was performed to better understand the dataset before training.

Analysis included:

- Dataset Overview
- Missing Value Analysis
- Duplicate Detection
- Statistical Summary
- Feature Distribution
- Boxplots
- Correlation Heatmap
- Target Class Distribution

Key observations:

- No missing values
- No duplicate records
- Significant class imbalance
- Strong correlation between Stress Level and Anxiety Score
- Positive relationship between Study Hours and Exam Pressure

---

# 🤖 Models Implemented

## 1️⃣ Linear Support Vector Machine

The baseline classifier assumes that classes are linearly separable using a single hyperplane.

---

## 2️⃣ Balanced Linear SVM

To address severe class imbalance, class weights were automatically balanced.

This increased the importance of minority classes during optimization and significantly improved High Risk student detection.

---

## 3️⃣ RBF Kernel SVM

The Radial Basis Function kernel enables SVM to learn nonlinear decision boundaries using the Kernel Trick.

This allows the classifier to model more complex relationships without explicitly constructing higher-dimensional features.

---

# 📈 Model Evaluation

Each model was evaluated using:

- Accuracy
- Confusion Matrix
- Precision
- Recall
- F1-Score
- Support

The project emphasizes **business-oriented evaluation** rather than relying solely on accuracy.

---

# 📊 Model Comparison

| Model | Accuracy | Key Observation |
|--------|----------|----------------|
| Linear SVM | 86.43% | High accuracy but failed to detect High Risk students |
| Balanced Linear SVM | 80.08% | Significant improvement in High Risk Recall |
| RBF Kernel SVM | 80.61% | Better nonlinear modelling with balanced performance |

---

# 🏆 Final Model Selection

Although the baseline Linear SVM achieved the highest overall accuracy, it completely failed to identify High Risk students due to class imbalance.

The **Balanced Linear SVM** was selected as the preferred model because:

- Higher Recall for High Risk students
- Better suitability for real-world educational support systems
- More reliable detection of students requiring intervention

This project demonstrates that **accuracy alone is not sufficient** when evaluating models for real-world healthcare or educational applications.

---

# 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Google Colab
- Jupyter Notebook

---

# 📁 Project Structure

```
Student-Burnout-Prediction/
│
├── notebooks/
│     └── Student_Burnout_SVM.ipynb
│
├── images/
│     ├── correlation_heatmap.png
│     ├── linear_confusion_matrix.png
│     ├── balanced_confusion_matrix.png
│     └── rbf_confusion_matrix.png
│
├── data/
│     └── dataset_link.txt
│
├── requirements.txt
│
├── LICENSE
│
└── README.md
```

---

# 🚀 Installation

Clone the repository

```bash
git clone https://github.com/SarathiStacks/Student-Burnout-Prediction.git
```

Navigate to the project

```bash
cd student-burnout-prediction
```

Install dependencies

```bash
pip install -r requirements.txt
```

Run the notebook using Jupyter Notebook or Google Colab.

---

# 💡 Future Improvements

- Hyperparameter Optimization using GridSearchCV
- Cross Validation
- SMOTE for minority class oversampling
- Probability Calibration
- Model Explainability using SHAP
- Compare with Random Forest, XGBoost and CatBoost
- Deploy using Streamlit or Flask
- Real-time Burnout Risk Prediction API

---

# 📚 Key Machine Learning Concepts Demonstrated

- Supervised Learning
- Classification
- Support Vector Machines
- Hyperplane
- Support Vectors
- Margin Maximization
- Kernel Trick
- RBF Kernel
- Feature Scaling
- One-Hot Encoding
- Ordinal Encoding
- Class Imbalance Handling
- Confusion Matrix
- Precision
- Recall
- F1 Score
- Model Comparison
- Business-Oriented Evaluation

---

# 🎓 Learning Outcome

This project was developed not only to build a predictive model but also to deeply understand the mathematics, intuition and practical implementation of Support Vector Machines.

It demonstrates the complete workflow of a classical machine learning project—from raw data exploration to model evaluation and informed model selection based on real-world objectives.

---

# 👨‍💻 Author

**Sarathi R N**

---