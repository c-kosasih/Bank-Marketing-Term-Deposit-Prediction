# 🏦 Bank-Marketing-Term-Deposit-Prediction

This project analyzes a dataset related to direct marketing campaigns (based on phone calls) of a Portuguese banking institution. The goal is to predict whether a client will subscribe to a term deposit (`y` variable).  

## Project Overview

The core of this project is to build and evaluate several machine learning models to accurately predict customer subscription to a term deposit. This involves:
1.  **Data Preprocessing**: Cleaning and preparing the data for modeling. This includes handling unknown values and encoding categorical features.
2.  **Exploratory Data Analysis (EDA)**: Visualizing the data to understand the relationships between different client attributes (like age, job, marital status) and the outcome (subscription to a term deposit).
3.  **Model Training**: Implementing and training multiple classification algorithms:
    * KNeighborsClassifier
    * Random Forest
4.  **Model Evaluation**: Assessing the performance of each model using metrics like accuracy, precision, and recall.
5.  **Hyperparameter Tuning**: Optimizing the best-performing model using GridSearchCV to find the most effective parameters.

## 📊 Key Features

* **Data Cleaning**: Replaces 'unknown' values in categorical columns with the mode (most frequent value) to ensure data completeness.
* **Feature Engineering**: Converts categorical variables (like 'job', 'marital', 'education', etc.) into numerical format using one-hot encoding so they can be used by machine learning models.
* **Model Comparison**: Implements and compares two classification models (KNeighborsClassifier and Random Forest) to identify the most suitable one for this dataset.
* **Performance Metrics**: Uses a comprehensive set of metrics (Accuracy, Precision, Recall, F1-Score) to evaluate and compare the models' effectiveness.
* **Hyperparameter Tuning**: Utilizes `GridSearchCV` to fine-tune the models, significantly improving its predictive accuracy.
* **Final Model**: Selects the tuned KNeighborsClassifier as the best-performing model for predicting customer subscription.

## Data

The dataset is from [kaggle](https://www.kaggle.com/datasets/saranyaponnarasu/bank-marketing-term-deposits-classification/data).

**Attributes:**
* `age`: Age of the client (numeric)
* `job`: Type of job (categorical)
* `marital`: Marital status (categorical)
* `education`: Education level (categorical)
* `default`: Has credit in default? (categorical: 'yes', 'no', 'unknown')
* `balance`: Average yearly balance, in euros (numeric)
* `housing`: Has housing loan? (categorical: 'yes', 'no')
* `loan`: Has personal loan? (categorical: 'yes', 'no')
* `contact`: Contact communication type (categorical)
* `day`: Last contact day of the month (numeric)
* `month`: Last contact month of year (categorical)
* `duration`: Last contact duration, in seconds (numeric)
* `campaign`: Number of contacts performed during this campaign (numeric)
* `pdays`: Number of days passed since the client was last contacted from a previous campaign (-1 means client was not previously contacted)
* `previous`: Number of contacts performed before this campaign (numeric)
* `poutcome`: Outcome of the previous marketing campaign (categorical)

**Target Variable:**
* `y`: Has the client subscribed a term deposit? (binary: 'yes', 'no')

## Model Results
KNeighborsClassifier is selected as the best model with accuracy 0.91 and macro f1-score 0.73 (see the rest in the notebook).
