# Credit-Card-Fraud-Detection
## Introduction
Increased online purchases and the widespread use of electronic payment systems have made credit card fraud a severe problem. Global credit card fraud losses topped $32 billion in 2022, and until more sophisticated fraud detection tools are created, these losses are expected only to increase. Advanced fraud detection systems that can spot fraudulent behavior in real-time and minimize delays to legal transactions are becoming increasingly necessary as digital payments increase. This type of traditional fraud detection relies on predefined rules and guidelines for determining suspicion. Such systems are impractical because they cannot learn from the changing trends of fraudsters. They also produce a high number of false positives that bother users. In contrast, ML can provide a platform through which the learning model learns and adapts new behaviors by being driven by data. ML models are more successful because they can identify complex fraud patterns that rule-based solutions fail to spot . The extremely uneven nature of the data, where fraudulent transactions make up a small fraction of the total, is one of the main challenges in credit card fraud detection. This imbalance may lead to models that predict many legitimate transactions and miss many fraud cases . Most of the models considered, in their attempts to achieve high accuracy, place more emphasis on the majority class that has greater relevance to less consideration of the crucial minority class. Addressing this asymmetry thus is imperative in the development of effective methods for fraud detection. This study investigates several ML techniques to detect fraud, like SVM, KNN, Decision Tree, Logistic Regression, and Ensemble Methods [4]. Models were chosen based on their performance in binary classification tests and their capacity to manage datasets with imbalances. Their performance is assessed using key performance metrics like accuracy, precision, recall, F1-score, and AUC-ROC, emphasizing striking a balance between precision (which lowers false positives) and recall (which finds actual fraud cases). Resampling methods such as under-sampling, oversampling, and SMOTE resolve class imbalance to enhance model performance further. To lessen false positives and negatives for practical use, decision threshold tuning is being investigated to optimize the trade-off between recall and precision.

## Problem Statement
There is a huge class imbalance in the transaction data. While fraudulent transactions were few in the past, most have traditionally been classified as valid; these models are poor fraud identifiers [9]. Traditional rule-based systems miss changing patterns, and then there are lost fraud cases and too many false positives . This project utilizes a range of machine learning algorithms, including Decision Tree, Logistic Regression, KNN, and Ensemble Methods like Random Forest and AdaBoost, along with SVM, with the aim to improve the accuracy and robustness of fraud detection. The project incorporates feature scaling (scaling 'Amount' and 'Time') to standardize the input data, followed by oversampling using SMOTE (to address the class imbalance by generating synthetic samples for the minority (fraudulent) class . This project addresses class imbalance and the utilization of more than one approach to machine learning toward developing an even more accurate, adaptive, and efficient fraud detection system that can recognize subtle patterns of fraudulent activities .

## Proposed Methodology
I.	Data Collection:
The credit card transaction dataset is collected from a CSV file to gather historical transaction data with relevant features such as Time, Amount, and transaction details, including the Class label (0 = Not Fraud, 1 = Fraud).

II.	 Processing of the DataSet:
    i.	  Data Cleaning - Handling missing values by removal of any irrelevant columns.
    ii.	  Feature Scaling - We use the 'StandardScaler' transform to normalize 'Amount' and 'Time' features so that all features are at the same scale.
    iii.	Feature Selection - We compute the correlation matrix and select only those features That have a correlation greater than 0.1 with the target variable (Class) and            eliminate 
          insignificant features with very low correlation.
    iv.	  Class Balancing (SMOTE) - Since fraudulent transactions are rare, we use SMOTE to create synthetic samples of the minority class to make the dataset balanced.

III.	 EDA: We capture the distribution of valid vs. invalid transactions, study the correlations among features by a correlation, heatmap create histograms and box plots                and examine relationships between pairs to better understand the data patterns.
      
IV.	 Feature Engineering
    i.	Drop Unnecessary Features: Remove redundant or uninformative features.
    ii.	Data Splitting:Divide the balanced dataset into training and testing parts, with an 80:20 ratio.The test set has to be maintained separately for testing how well the         model functions.

V.	 Model Training:A variety of classifiers from different algorithms are used, allowing a comparative analysis of their performance while noting the training duration for each, hence assessing their efficiency. The classifiers utilized in this study include:-
  a.	Decision Tree
  b.	KNN
  c.	Logistic Regression
  d.	SVM
  e.	Ensemble Model
   
VI.	 Model Evaluation:
We evaluate each model using a confusion matrix, classification report, and ROC-AUC scores and measure model quality with Precision, Recall, F1-Score, and Accuracy to capture the ability to detect fraudulent transactions, followed by selecting the best Model based on the evaluation metrics, emphasizing high recall and precision for fraud detection.


VII.	 Real-time Prediction:
  a.	Feature Scaling for New Data - The same feature scaling used during training is applied 
      to the provided new transaction data. 
  b.	Significant Features - We use only the significant features during feature selection.
  c.	Fraud Prediction - Scaled data is passed to the trained model to classify the transaction 
      as fraud or not fraud. Finally, prediction time is recorded to ensure the model is efficient 
      for real-time scenarios.


    ![image](https://github.com/user-attachments/assets/8a565b7d-220c-42dc-aefe-9eeff303762d)

