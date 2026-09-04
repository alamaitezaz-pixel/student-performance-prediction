# Student Performance Prediction

A machine learning project that predicts student exam scores using academic, behavioral, demographic, and socioeconomic factors.

## Project Overview

This project builds and evaluates multiple regression models to predict students' exam scores.

The complete machine learning workflow includes:

* Data exploration and analysis
* Exploratory Data Analysis (EDA)
* Data preprocessing
* Handling missing values
* Feature scaling and encoding
* Baseline model development
* Training multiple regression models
* Hyperparameter tuning with GridSearchCV
* Cross-validation
* Model comparison
* Final model evaluation
* Actual vs. predicted analysis

## Problem Statement

Student performance can be influenced by several factors, including study habits, parental involvement, motivation, attendance, and other academic and socioeconomic characteristics.

The goal of this project is to use these available features to build a regression model capable of predicting a student's exam score.

## Dataset

The project uses a student performance dataset containing academic, behavioral, demographic, and socioeconomic features.

The target variable is:

`Exam_Score`

The dataset is downloaded programmatically using KaggleHub.

## Machine Learning Models

The following regression models were evaluated:

* Linear Regression
* Ridge Regression
* Lasso Regression
* SGDRegressor
* Random Forest Regressor

Hyperparameter tuning was performed using `GridSearchCV`, and models were compared using 5-fold cross-validation.

## Model Evaluation

The final model was selected based on the lowest cross-validation RMSE.

| Model             | CV RMSE | Test RMSE | Test MAE | Test R² |
| ----------------- | ------: | --------: | -------: | ------: |
| Ridge             |  1.9973 |    2.1633 |   0.4990 |  0.6861 |
| Linear Regression |  1.9973 |    2.1634 |   0.4990 |  0.6860 |
| Lasso             |  1.9974 |    2.1631 |   0.4990 |  0.6861 |
| SGDRegressor      |  2.1306 |    2.2079 |   0.6610 |  0.6730 |
| Random Forest     |  2.3184 |    2.4304 |   1.1303 |  0.6038 |

The three linear models performed very similarly. Ridge Regression was selected as the final model because it achieved the lowest cross-validation RMSE.

## Final Model

The final Ridge Regression model achieved:

* **Test RMSE:** 2.1633
* **Test MAE:** 0.4990
* **Test R²:** 0.6861

The model was saved using `joblib`.

## Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* KaggleHub
* Joblib
* Google Colab

## Project Structure

```text
student-performance-prediction/
│
├── student_performance_prediction.ipynb
├── README.md
└── .gitignore
```

## Future Improvements

Possible improvements include:

* Feature engineering
* More extensive hyperparameter tuning
* Testing additional ensemble models
* Error analysis
* Model interpretability
* Building an interactive prediction application
* Deploying the model as an API

## Author

**Aitezaz Alam**

BS Computer Science
