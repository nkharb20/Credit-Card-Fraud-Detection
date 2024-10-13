# Credit Card Fraud Detection

## Introduction
The rise in online purchases and the widespread adoption of electronic payment systems have made credit card fraud a significant global issue. In 2022 alone, credit card fraud losses exceeded **$32 billion**, with expectations of continued growth until more sophisticated fraud detection tools are developed. As digital payments increase, there is an urgent need for advanced fraud detection systems capable of identifying fraudulent behavior in real-time and minimizing delays for legitimate transactions.

Traditional fraud detection methods rely on predefined rules to flag suspicious activity. However, these systems are often inadequate as they cannot adapt to the evolving tactics of fraudsters, resulting in a high volume of false positives that frustrate users. In contrast, **Machine Learning (ML)** offers a data-driven approach where models can learn and adapt to new behaviors. ML models are particularly effective in identifying complex fraud patterns that rule-based solutions may miss.

One of the main challenges in credit card fraud detection is the **severe class imbalance** in transaction data, where fraudulent transactions represent a small fraction of the total. This imbalance can lead to models that predominantly predict legitimate transactions, thereby failing to identify fraud. Therefore, addressing this imbalance is crucial for developing effective fraud detection methods.

This study investigates several ML techniques, including **Support Vector Machines (SVM)**, **K-Nearest Neighbors (KNN)**, **Decision Trees**, **Logistic Regression**, and **Ensemble Methods**. Models are evaluated based on their performance in binary classification tests and their ability to handle imbalanced datasets, with performance metrics such as **accuracy**, **precision**, **recall**, **F1-score**, and **AUC-ROC** being emphasized. Resampling methods, including **under-sampling**, **over-sampling**, and **SMOTE** (Synthetic Minority Oversampling Technique), are employed to address class imbalance, further enhancing model performance.

## Problem Statement
The existing dataset presents a significant class imbalance, with a disproportionate number of legitimate transactions compared to fraudulent ones. Traditional rule-based systems struggle to adapt to changing patterns, leading to missed fraud cases and an excess of false positives. This project aims to utilize various machine learning algorithms, including **Decision Trees**, **Logistic Regression**, **KNN**, and Ensemble Methods like **Random Forest** and **AdaBoost**, alongside **SVM**, to improve the accuracy and robustness of fraud detection.

The project incorporates feature scaling (normalizing 'Amount' and 'Time') and applies **SMOTE** to generate synthetic samples for the minority (fraudulent) class. By addressing class imbalance and employing multiple machine learning approaches, the goal is to develop a more accurate, adaptive, and efficient fraud detection system capable of recognizing subtle patterns of fraudulent activity.

## Proposed Methodology

### I. Data Collection
- The credit card transaction dataset is obtained from a CSV file, encompassing historical transaction data with relevant features such as **Time**, **Amount**, and the **Class** label (0 = Not Fraud, 1 = Fraud).

### II. Processing of the Dataset
1. **Data Cleaning**: Handle missing values and remove irrelevant columns.
2. **Feature Scaling**: Normalize 'Amount' and 'Time' features using **StandardScaler**.
3. **Feature Selection**: Compute the correlation matrix to select features with a correlation greater than 0.1 with the target variable (Class), eliminating insignificant features.
4. **Class Balancing (SMOTE)**: Use SMOTE to create synthetic samples of the minority class to balance the dataset.

### III. Exploratory Data Analysis (EDA)
- Analyze the distribution of valid vs. fraudulent transactions, visualize correlations using a heatmap, create histograms and box plots, and examine relationships between pairs of features to understand data patterns.

### IV. Feature Engineering
1. **Drop Unnecessary Features**: Remove redundant or uninformative features.
2. **Data Splitting**: Split the balanced dataset into training and testing sets in an 80:20 ratio, maintaining the test set for final evaluation.

### V. Model Training
- Utilize a variety of classifiers from different algorithms to enable comparative analysis of their performance while noting the training duration. Classifiers employed include:
  - Decision Tree
  - KNN
  - Logistic Regression
  - SVM
  - Ensemble Model

### VI. Model Evaluation
- Assess each model using a confusion matrix, classification report, and ROC-AUC scores, measuring model quality with **Precision**, **Recall**, **F1-Score**, and **Accuracy**. The goal is to capture the model's ability to detect fraudulent transactions, ultimately selecting the best model based on evaluation metrics, focusing on high recall and precision.

### VII. Real-time Prediction
1. **Feature Scaling for New Data**: Apply the same feature scaling used during training to new transaction data.
2. **Significant Features**: Utilize only the significant features identified during the selection process.
3. **Fraud Prediction**: Pass scaled data to the trained model for classification as fraud or not fraud. Record prediction time to ensure efficiency in real-time scenarios.

![Fraud Detection Workflow](https://github.com/user-attachments/assets/8a565b7d-220c-42dc-aefe-9eeff303762d)
