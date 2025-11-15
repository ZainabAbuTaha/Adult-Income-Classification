# Project 4 - Machine Learning Core

Author: Zainab Abu Taha  

This repository contains the solution for **Project 4 (Core)**, divided into three parts:
1. **Part 1:** Data exploration, cleaning, baseline model, and permutation importance.
2. **Part 2:** Feature engineering (PCA), feature selection, model comparison, and updated permutation importance.
3. **Part 3:** Neural network implementation with early stopping, training history visualization, evaluation metrics, and hyperparameter tuning using Keras Tuner.

---

## Dataset
- **Source:** UCI Adult Income dataset  
- **Target:** `income` (binary classification: `>50K` vs `<=50K`)  
- **Rows:** ~48,842 individuals  
- **Features:** 15 original features (numeric + categorical)

---

## Part 1: Baseline Model
- Preprocessing with imputation, scaling, and one-hot encoding.
- Baseline model: RandomForestClassifier.
- Evaluation metrics: Accuracy, ROC AUC, Classification Report.
- Permutation importance to identify top 10 features.
- Explanatory visualizations for stakeholders (e.g., income vs education, income vs gender).

---

## Part 2: Feature Engineering & Selection
- Applied **PCA** with 3 principal components.
- Compared baseline vs PCA-enhanced model.
- Applied **L1 Logistic Regression** for feature selection.
- Final model trained on selected features.
- Updated permutation importance showing both traditional and engineered features.

---

## Part 3: Neural Network
- Built a small NN with one hidden layer and dropout.
- Used **EarlyStopping** (patience=5, monitor=val_accuracy).
- Trained for up to 50 epochs with validation split=0.2.
- Visualized training vs validation accuracy.
- Evaluated with confusion matrix and classification report.
- Tuned hyperparameters (units, dropout rate, optimizer, learning rate) using **Keras Tuner**.
- Final tuned model achieved improved accuracy and balanced precision/recall.

---

## Key Insights
- Traditional drivers of income: age, education-num, hours-per-week, capital-gain, occupation.
- PCA components captured latent patterns across categorical features.
- Neural network captured non-linear relationships and improved generalization.
- Hyperparameter tuning showed that architecture and optimizer choices significantly affect performance.

