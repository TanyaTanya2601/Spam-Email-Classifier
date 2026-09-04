📧 Spam Email Classification

A machine learning project that classifies emails as spam or ham (legitimate) using natural language processing and a Naive Bayes classifier.

## Overview

Spam emails clutter inboxes and pose security risks such as phishing and malware. This project builds a text classification pipeline to automatically detect spam emails using TF-IDF feature extraction and a probabilistic machine learning model.

 ## Dataset
Size: 5,572 labeled emails
Columns: Category (spam/ham), Message (email text)
Source: emails.csv

## Tech Stack
Python
Pandas
NLTK
Scikit-learn (TF-IDF, Naive Bayes, evaluation metrics)

## Approach
Data Preparation — Loaded and explored the dataset, checked for nulls and duplicates.
Feature Extraction — Converted raw email text into numerical vectors using TfidfVectorizer.
Train/Test Split — Split data 80/20 for training and evaluation.
Model Training — Trained a baseline Multinomial Naive Bayes classifier.
Evaluation — Assessed performance using accuracy, precision, recall, and F1-score.
Threshold Tuning — Experimented with adjusting the classification threshold to address class imbalance between spam and ham emails.

## Results
Metric	Score
Accuracy	96.5%
Precision	100%
Recall	73.8%
F1 Score	0.849

Key takeaway: The model achieves perfect precision (no legitimate emails misclassified as spam) but moderate recall (some spam emails go undetected). Since the dataset is imbalanced (far more ham than spam), accuracy alone isn't the best measure of performance — precision and recall together give a clearer picture.

## Future Improvements
Address class imbalance using techniques like SMOTE or class weighting
Try ensemble models (Random Forest, XGBoost) to boost recall
Experiment with deep learning approaches (CNN/RNN) for richer text representation
Perform hyperparameter tuning and cross-validation
