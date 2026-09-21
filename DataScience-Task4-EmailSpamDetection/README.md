# Email Spam Detection with Machine Learning

## Overview

This project was completed as part of the Oasis Infobyte AICTE Data Science Internship Program.

The objective of this project is to build a machine learning classifier that distinguishes between legitimate messages (`ham`) and spam messages using Natural Language Processing (NLP).

## Dataset

The project uses the **SMS Spam Collection** dataset.

The dataset contains labeled SMS messages classified into two categories:

* `ham` – legitimate message
* `spam` – spam message

The dataset used in this project contains 5,572 messages.

## Dataset Exploration

The dataset was cleaned and inspected before modeling. The original CSV contained several unused columns, which were removed, leaving the relevant `label` and `message` columns.

No missing values were found in the relevant columns.

The class distribution was:

* Ham: 4,825 messages (86.59%)
* Spam: 747 messages (13.41%)

The distribution shows that ham messages are the majority class, so accuracy was evaluated alongside precision, recall, and F1-score.

## Text Preprocessing

The SMS messages were preprocessed using the following steps:

* Conversion of text to lowercase
* Removal of punctuation and non-alphanumeric characters while retaining numbers
* Splitting messages into individual words
* Removal of common English stopwords
* Joining the remaining words into cleaned messages

## TF-IDF Feature Extraction

TF-IDF (Term Frequency-Inverse Document Frequency) was used to convert the cleaned text into numerical features that could be used by machine learning models.

The TF-IDF vectorizer was fitted only on the training data and then used to transform the test data.

The training set produced 8,082 TF-IDF features.

## Train-Test Split

The dataset was divided into:

* 80% training data
* 20% testing data

Stratification was used to maintain a similar ham/spam class distribution in both sets.

## Machine Learning Models

Two classification models were trained:

1. Multinomial Naive Bayes
2. Logistic Regression

Both models were trained using the same TF-IDF features.

## Model Evaluation

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

### Multinomial Naive Bayes

* Accuracy: 96.23%
* Spam Precision: 1.00
* Spam Recall: 0.72
* Spam F1-score: 0.84

### Logistic Regression

* Accuracy: 96.32%
* Spam Precision: 0.99
* Spam Recall: 0.73
* Spam F1-score: 0.84

## Why Recall Matters in Spam Detection

Recall is particularly important in spam detection because it measures how many of the actual spam messages are correctly identified.

A model with low spam recall may allow many spam messages to pass through even when its overall accuracy is high. Therefore, recall helps measure how effectively the classifier detects actual spam.

Precision is also important because it indicates how often messages predicted as spam are actually spam. A balance between precision and recall helps reduce missed spam while limiting legitimate messages being incorrectly classified as spam.

## Model Comparison

Both models performed well on the test set.

Logistic Regression achieved slightly higher overall accuracy and spam recall, while Multinomial Naive Bayes achieved slightly higher spam precision. Both models achieved the same spam F1-score of approximately 0.84.

The comparison is based on this particular test split and evaluation setup.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook
* Natural Language Processing (NLP)

## Project Files

* `Email_Spam_Detection.ipynb` – Complete data preprocessing, TF-IDF feature extraction, model training, and evaluation workflow.
* `spam.csv` – Dataset used for the project.
* `README.md` – Project documentation.
* Screenshot files – Relevant project outputs and visualizations.