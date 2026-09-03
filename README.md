# Phishing Website Detection Using Machine Learning

## Overview

This project investigates the use of machine learning algorithms for detecting phishing websites based on website-related features.

The study focuses on comparing multiple classification algorithms and investigating whether feature reduction can maintain or improve classification performance while using fewer input features.

## Research Question

> How effectively can different machine-learning classification algorithms detect phishing websites, and how does reducing the number of input features affect their performance?

## Dataset

The project uses the **Phishing Websites** dataset from the UCI Machine Learning Repository.

- Instances: 11,055
- Input features: 30
- Target variable: `Result`
- Missing values: 0
- Classes: 2

The dataset contains pre-extracted website characteristics rather than raw website URLs.

## Project Workflow

The project will follow these major stages:

1. Dataset inspection
2. Exploratory Data Analysis (EDA)
3. Data preprocessing
4. Baseline machine learning models
5. Model evaluation and comparison
6. Feature selection/reduction
7. Final performance analysis
8. Research paper and documentation

## Machine Learning Models

The study will compare several classical machine learning classification algorithms, including:

- Logistic Regression
- K-Nearest Neighbors
- Decision Tree
- Random Forest
- Support Vector Machine
- Naive Bayes
- Gradient Boosting

## Evaluation

Models will be evaluated using metrics such as:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix

## Project Status

**Current stage:** Dataset inspection completed.

The dataset has been successfully loaded and inspected. It contains 11,055 instances, 30 input features, and no missing values.

More experiments and results will be added as the project progresses.