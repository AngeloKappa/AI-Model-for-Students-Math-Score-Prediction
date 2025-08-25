# AI-Model-for-Students-Math-Score-Prediction
# Student Performance Prediction

A Python-based data science project that analyzes the Student Performance dataset from Portugal and builds machine learning models to predict final math exam scores. The project explores various preprocessing techniques, model selection strategies, and hyperparameter tuning, with a focus on interpretability and model performance. This project is part of my Msc programme in Artificial Inteligence and Deep Learning

## Dataset

The dataset used in this project is publicly available from the UCI Machine Learning Repository:

🔗 [Student Performance Dataset (UCI)](https://archive.ics.uci.edu/dataset/320/student+performance)

This dataset contains student achievement in secondary education (Math and Portuguese language) and includes attributes like demographic, social, and academic-related features.

---

## Features

- **Data Preprocessing:**
  - Mapping binary categorical features to numerical (e.g., yes/no, M/F)
  - One-hot encoding of nominal categorical variables
  - Feature standardization using `StandardScaler`

- **Modeling Approaches:**
  - **Linear Regression**: Baseline model to establish a performance benchmark
  - **Ridge Regression**: L2-regularized model to reduce overfitting
  - **XGBoost Regressor**: Tree-based ensemble model to capture nonlinear relationships

- **Model Evaluation:**
  - Train/validation/test split with stratification on the target variable
  - Performance metrics: RMSE (Root Mean Squared Error) and R² Score
  - Feature importance analysis for linear and tree-based models
  - Hyperparameter tuning using `RandomizedSearchCV`

---

## Getting Started

### Prerequisites

Ensure you have the following installed:

- Python 3.8+
- pip or conda package manager
- Jupyter Notebook (optional, but recommended)

## Example Results

| Model              | Validation RMSE | Test RMSE | Test R²  |
|-------------------|-----------------|-----------|----------|
| Linear Regression | ~2.1            | ~2.0      | ~0.81    |
| Ridge Regression  | ~2.0            | 1.9854    | 0.8176   |
| XGBoost Regressor | ~1.9            | 1.9162    | 0.825+   |

> **Note**: Results may vary depending on random seeds and train/val/test splits.

---

## Key Takeaways

- **Tree-based models like XGBoost** can better capture nonlinear relationships compared to linear models.
- **Ridge Regression** provides a good balance between interpretability and performance.
- **Stratified splits** help maintain consistent target distribution across train/val/test sets.
- **Feature engineering** (e.g., using G1 and G2 as predictors) plays a major role in model performance.

---

## Room for Improvement

- Add support for predicting Portuguese grades (`student-por.csv`)
- Experiment with other models (e.g., Lasso, SVR, LightGBM)
- Apply SHAP values for deeper model explainability
- Deploy as a simple web app using Streamlit or Flask

---

## Acknowledgments

- 📚 Data provided by **Paulo Cortez** and the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/320/student+performance).
- 💡 Project inspired by real-world applications of **education analytics**.
