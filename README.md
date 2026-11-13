# Phishing Website Detection Using Machine Learning

## Project Overview

Phishing attacks are a common cybersecurity threat in which attackers create fraudulent websites to trick users into sharing sensitive information, such as login credentials, banking details, and personal data.

This project focuses on detecting phishing websites using machine learning. Multiple classification algorithms are trained and evaluated on the UCI Phishing Websites dataset to distinguish between legitimate and phishing websites.

The project also explores feature importance and feature reduction to understand whether a smaller set of features can maintain comparable prediction performance.

## Problem Statement

The objective is to develop a machine learning-based classification system that can identify phishing websites based on their characteristics.

The project aims to:
- Analyse and preprocess the phishing websites dataset.
- Train multiple machine learning classification models.
- Compare their performance using standard evaluation metrics.
- Identify the most effective classification algorithm.
- Investigate feature importance and reduce the number of input features while maintaining model performance.

## Dataset

**Dataset:** UCI Phishing Websites Dataset

**Source:** UCI Machine Learning Repository

The dataset contains:
- 11,055 records
- 30 input features
- 1 target variable (`Result`)
- 2 classification categories: legitimate and phishing websites
- No missing values

The features describe different characteristics of websites, including URL structure, SSL certificates, domain information, web traffic, and hyperlinks.

The dataset was divided into training and testing sets using an 80:20 stratified split.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## Machine Learning Models

Seven classification algorithms were implemented and evaluated:

1. Logistic Regression
2. K-Nearest Neighbors (KNN)
3. Decision Tree
4. Random Forest
5. Support Vector Machine (SVM)
6. Gaussian Naive Bayes
7. Gradient Boosting

## Project Workflow

1. **Data Loading:** Loaded the UCI Phishing Websites dataset using Pandas.

2. **Exploratory Data Analysis:** Examined the dataset structure, feature distributions, class distribution, and other relevant patterns.

3. **Data Preprocessing:** Prepared the dataset for model training and separated the input features from the target variable.

4. **Train-Test Split:** Divided the dataset into training and testing sets using an 80:20 stratified split.

5. **Model Training:** Trained seven different machine learning classification algorithms.

6. **Model Evaluation:** Evaluated the models using accuracy, precision, recall, F1-score, and ROC-AUC.

7. **Feature Importance:** Used Random Forest feature importance to identify the most influential features.

8. **Feature Reduction:** Experimented with different feature subsets to study the effect of reducing input dimensions on model performance.

## Model Performance

The following table presents the performance of the seven evaluated models.

| Model | Accuracy (%) | Precision (%) | Recall (%) | F1-Score (%) | ROC-AUC (%) |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 92.85 | 92.34 | 95.04 | 93.67 | 98.08 |
| KNN | 94.89 | 95.01 | 95.86 | 95.43 | 98.69 |
| Decision Tree | 97.11 | 97.02 | 97.81 | 97.41 | 98.05 |
| Random Forest | 97.42 | 96.96 | 98.46 | 97.70 | 99.77 |
| SVM | 95.16 | 94.18 | 97.32 | 95.73 | 98.93 |
| Gaussian Naive Bayes | 60.06 | 99.71 | 28.35 | 44.15 | 97.02 |
| Gradient Boosting | 95.30 | 95.33 | 96.26 | 95.80 | 99.21 |

### Best Performing Model

Random Forest achieved the best overall performance among the evaluated baseline models.

- Accuracy: 97.42%
- Precision: 96.96%
- Recall: 98.46%
- F1-Score: 97.70%
- ROC-AUC: 99.77%

Its strong recall indicates that it successfully identifies a high proportion of phishing websites in the test set.

## Feature Importance and Reduction

Random Forest feature importance was used to identify the features contributing most to classification.

Some of the most influential features were:

| Feature | Importance |
|---|---:|
| SSLfinal_State | 0.3197 |
| URL_of_Anchor | 0.2500 |
| web_traffic | 0.0708 |
| having_Sub_Domain | 0.0695 |
| Links_in_tags | 0.0439 |
| Prefix_Suffix | 0.0379 |

Feature reduction experiments were performed using the most important features.

| Number of Features | Accuracy (%) | F1-Score (%) |
|---|---:|---:|
| 30 | 97.42 | 97.70 |
| 20 | 97.38 | 97.66 |
| 15 | 97.01 | 97.34 |
| 10 | 95.16 | 95.70 |

### Key Finding

Reducing the number of features from 30 to 20 resulted in only a 0.04 percentage-point decrease in F1-score.

This indicates that a smaller feature set can maintain nearly the same classification performance while reducing the number of input variables.

## Installation and Execution

### 1. Clone the Repository

```bash
git clone https://github.com/Yashi-tech-ai/Phishing-Website-Detection-and-Feature-Reduction.git
cd Phishing-Website-Detection
```

### 2. Install Dependencies

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 3. Open Jupyter Notebook

```bash
jupyter notebook
```

### 4. Run the Project

Open the project notebook in Jupyter Notebook and execute the cells sequentially.

Make sure the dataset is placed in the appropriate directory and that the dataset path in the notebook is correct.

## Limitations

- The system uses pre-extracted website features rather than analysing live websites.
- The model's predictions depend on the quality and representativeness of the dataset.
- Performance on unseen or evolving phishing techniques may differ from the reported test results.

## Future Improvements

- Integrate live URL analysis and website feature extraction.
- Explore additional machine learning and deep learning approaches.
- Evaluate the system on newer phishing datasets.
- Develop a web-based interface for interactive phishing website detection.
- Investigate model explainability techniques to understand individual predictions.

## Acknowledgements

I would like to acknowledge the UCI Machine Learning Repository for providing the Phishing Websites dataset used in this project.