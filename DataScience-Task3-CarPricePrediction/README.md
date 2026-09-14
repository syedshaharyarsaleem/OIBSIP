# Car Price Prediction

## Overview

This project was completed as part of the Oasis Infobyte AICTE Data Science Internship Program.

The objective of this project is to predict the selling price of used cars using machine learning regression models. The project covers data exploration, cleaning, feature engineering, categorical variable encoding, correlation analysis, model training, evaluation, and feature-importance analysis.

## Dataset

The project uses the publicly available "Vehicle Dataset from Cardekho".

The dataset contains information about used cars, including:

* Car name
* Year
* Selling price
* Present price
* Kilometers driven
* Fuel type
* Seller type
* Transmission
* Number of previous owners

The target variable is `Selling_Price`.

## Data Cleaning

The dataset was inspected for missing values and duplicate records.

No missing values were found. Two duplicate rows were identified and removed, reducing the dataset from 301 rows to 299 rows.

## Feature Engineering

A new `car_age` feature was created from the `Year` column using 2026 as the reference year.

The `Car_Name` column was excluded from model training because it contains many unique categories relative to the dataset size. The original `Year` column was also excluded because its information is represented by the newly created `car_age` feature.

## Categorical Encoding

The categorical variables `Fuel_Type`, `Seller_Type`, and `Transmission` were converted into numerical indicator variables using one-hot encoding with `drop_first=True`.

## Exploratory Data Analysis

The analysis included:

* Dataset overview
* Data type inspection
* Missing-value analysis
* Duplicate-value analysis
* Categorical value distributions
* Correlation analysis
* Correlation heatmap
* Feature-importance visualization

The correlation analysis showed a strong positive relationship between `Present_Price` and `Selling_Price`.

## Machine Learning Models

Two regression models were trained:

1. Linear Regression
2. Random Forest Regression

The dataset was divided into 80% training data and 20% testing data.

## Model Evaluation

The models were evaluated using:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* R² Score

The results from the completed notebook showed that Linear Regression performed better than Random Forest on the test set.

Linear Regression achieved approximately:

* MAE: 1.47
* RMSE: 2.52
* R²: 0.75

Random Forest achieved approximately:

* MAE: 1.48
* RMSE: 3.58
* R²: 0.50

Based on these evaluation metrics, Linear Regression provided the better fit for this dataset and test split.

## Feature Importance

The Random Forest feature-importance analysis identified `Present_Price` as the most influential feature for predicting `Selling_Price`, which is consistent with the strong positive correlation observed during the correlation analysis.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## Project Files

* `Car_Price_Prediction.ipynb` – Complete data analysis and machine learning workflow.
* `car data.csv` – Dataset used for the analysis and model training.
* `README.md` – Project documentation.
* Screenshot files – Relevant project outputs and visualizations.
