# Iris Flower Classification

## Overview

This project was completed as part of the Oasis Infobyte AICTE Data Science Internship Program. The objective is to build machine learning models that can classify Iris flowers into their respective species using their physical measurements.

## Dataset

The Iris dataset is a built-in dataset provided by scikit-learn. It contains 150 flower samples from three species:

* Setosa
* Versicolor
* Virginica

Each sample contains four numerical features:

* Sepal length
* Sepal width
* Petal length
* Petal width

## Exploratory Data Analysis

The dataset was explored using Pandas, Matplotlib, and Seaborn. The analysis included:

* Dataset shape and column information
* Data type inspection
* Missing-value analysis
* Descriptive statistics
* Species distribution
* Pairplot visualization
* Box plots for the numerical features

The dataset contains 150 samples with 50 samples from each species and no missing values.

## Feature Selection

The pairplot showed that petal length and petal width provide clearer separation between the three Iris species compared with the sepal measurements. However, all four numerical features were retained for model training so that the models could use all available information.

## Machine Learning Models

Two classification models were trained and evaluated:

1. Logistic Regression
2. K-Nearest Neighbors (KNN)

The dataset was divided into 80% training data and 20% testing data.

## Model Evaluation

Both models were evaluated using:

* Accuracy
* Confusion Matrix
* Precision
* Recall
* F1-score

Both Logistic Regression and KNN achieved **100% accuracy** on the test set. Their confusion matrices and classification metrics were also identical. Therefore, neither model outperformed the other based on the evaluation metrics used.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## Project Files

* `Iris_Flower_Classification.ipynb` – Jupyter Notebook containing the complete analysis and machine learning workflow.
* `README.md` – Project documentation.
