# Data Mining Project: Wine Quality Dataset Analysis

---

## Overview

This project involves the analysis and modeling of the "Wine Quality Dataset" to predict the quality of wines based on their chemical properties. The dataset comprises data related to the chemical properties and quality ratings of red and white variants of Portuguese "Vinho Verde" wine. Our goal is to explore various data analysis and machine learning techniques to build robust models for predicting wine quality.

---

## Introduction

The "Wine Quality Dataset" is a well-known dataset in the field of machine learning and data analysis. It contains data related to the chemical properties and quality ratings of red and white variants of Portuguese "Vinho Verde" wine. The quality of each wine sample is rated on a scale from 0 to 10 by professional wine tasters. This dataset offers a rich opportunity to explore various data analysis and machine learning techniques.

---

## Dataset Information

### Dataset Name and URL

- **Dataset Name:** Wine Quality Dataset
- **Dataset URL:** [Wine Quality Dataset](https://archive.ics.uci.edu/dataset/186/wine+quality)

### Data Dictionary

The dataset consists of the following features:

- **fixed acidity:** Fixed acidity (g(tartaric acid)/dm³)
- **volatile acidity:** Volatile acidity (g(acetic acid)/dm³)
- **citric acid:** Citric acid (g/dm³)
- **residual sugar:** Residual sugar (g/dm³)
- **chlorides:** Chlorides (g(sodium chloride)/dm³)
- **free sulfur dioxide:** Free sulfur dioxide (mg/dm³)
- **total sulfur dioxide:** Total sulfur dioxide (mg/dm³)
- **density:** Density (g/cm³)
- **pH:** pH level
- **sulphates:** Sulphates (g(potassium sulphate)/dm³)
- **alcohol:** Alcohol content (% vol.)
- **quality:** Wine quality (score between 0 and 10)
- **color:** Wine color (red/white)

**Additional Features:**

- **acidity_ratio:** Ratio of fixed acidity to volatile acidity
- **sulfur_dioxide_ratio:** Ratio of free sulfur dioxide to total sulfur dioxide

---

## Initial Data Exploration

An initial exploration of the dataset was performed using statistical measures and visualizations to understand the distribution and characteristics of the data.

### Key Steps:

1. **Loading the Dataset**
2. **Descriptive Statistics**
3. **Checking for Missing Values**
4. **Handling Duplicates**
5. **Visualizing Feature Distributions**
6. **Analyzing Correlations**

---

## Data Cleaning

The data cleaning process included:

- **Checking for missing values:** None were found.
- **Checking for duplicates:** 1,177 duplicate rows were found, but were not removed in order to produce a better model performance due to the combination of two datasets.

---

## Feature Engineering

Additional features were created to enhance the dataset:

- **acidity_ratio:** Ratio of fixed acidity to volatile acidity
- **sulfur_dioxide_ratio:** Ratio of free sulfur dioxide to total sulfur dioxide

---

## Building Classification Models

Several machine learning algorithms were used to predict wine quality, including:

1. **Logistic Regression**
2. **Decision Tree Classifier**
3. **Random Forest Classifier**
4. **Support Vector Machine (SVM)**

### Data Preparation

The data was split into training and testing sets, with a test size of 20%. The features were standardized to improve model performance.

### Performance Metrics

The models were evaluated using the following metrics:

- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**

These metrics are essential for multiclass classification problems where a balance between precision and recall is desired.

---

## Model Evaluation

### Default Model Training

Initially, the models were trained with default parameters. The Random Forest classifier achieved the highest accuracy, followed by Logistic Regression, SVM, and Decision Tree.

### Default Repeated Stratified K-Fold Cross Validation vs. Best Hyperparameter Repeated Stratified K-Fold Cross Validation

Cross-validation and hyperparameter tuning were applied to improve model performance. The best hyperparameters were identified using GridSearchCV. The results showed that both Random Forest and SVM classifiers performed the best, with the SVM showing significant improvement due to proper hyperparameter tuning.

---

## Statistical Tests

**Friedman Test**

The Friedman test was used to evaluate whether the differences in model performance were statistically significant. The results indicated no statistically significant differences in performance metrics (Accuracy, Precision, Recall, F1 Score) among the classifiers.

**Bayesian Test**

We also performed Bayesian testing using the baycomp library to compare the classifiers. The Bayesian test results provided additional insights into the relative performance of the models.

---

## Conclusion

The most promising features for classifying wine quality are alcohol, sulphates, citric acid, volatile acidity, and density. Additional features like acidity ratio and sulfur dioxide ratio can also provide valuable insights. These features are chosen based on their correlation with wine quality and their unique contribution to the dataset.

The implementation of cross-validation and hyperparameter tuning has reinforced the Random Forest classifier's position as the best model for predicting wine quality, achieving the highest accuracy and balanced performance metrics. However, the SVM model has shown substantial improvement and is now a close second, indicating its potential with proper parameter tuning. Logistic Regression and Decision Tree, while useful, did not perform as well as the ensemble and kernel-based methods.

For practical applications, we recommend using the Random Forest model due to its robustness and high performance. The SVM model is also a strong candidate, especially for datasets where non-linear relationships are prevalent. Further fine-tuning and exploration of additional features could enhance these models' performance even more.

---

## Dependencies

- **Python**: 3.x
- **pandas**: Data manipulation and analysis
- **matplotlib**: Plotting and visualization
- **seaborn**: Statistical data visualization
- **sklearn**: Machine learning library
- **scipy**: Scientific computing and statistics
- **baycomp**: Bayesian comparison of classifiers

---

This project demonstrates the power of data cleaning, feature engineering, and model tuning in achieving accurate predictions for wine quality. The methodologies and results can be extended to other datasets and applications in the field of machine learning and data science.
