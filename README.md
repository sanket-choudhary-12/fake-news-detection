Fake News Detection by Machine Learning

Overview
This project implements a machine learning model to classify news articles as fake or real based on their content. It utilizes natural language processing (NLP) techniques and logistic regression for classification.

Dataset
The dataset (train.csv.zip) consists of news articles with the following columns:

id: Unique identifier
title: Title of the news article
author: Author of the news article
text: Full text content of the news article
label: Binary label (1 for fake news, 0 for real news)
The dataset initially contains 20,800 articles, with preprocessing steps including handling missing values and combining title and author into a unified content column.

Approach
Data Preprocessing:

Loaded the dataset using pandas.
Filled missing values in title, author, and text columns.
Combined title and author columns into a single content column for analysis.
Feature Engineering:

Applied stemming to the content column using NLTK's PorterStemmer to reduce words to their base form and remove stopwords.
Model Training:

Utilized TF-IDF (Term Frequency-Inverse Document Frequency) vectorization to convert text data into numerical features.
Split the dataset into training and testing sets (80% training, 20% testing) using stratified sampling to maintain class distribution.
Trained a logistic regression model on the TF-IDF transformed data to predict whether news articles are fake or real.
Evaluation:

Evaluated the model's performance using accuracy score metrics, achieving approximately 97.91% accuracy on the test set.
Prediction:

Demonstrated a sample prediction where a news article was classified as fake or real based on the trained logistic regression model.
