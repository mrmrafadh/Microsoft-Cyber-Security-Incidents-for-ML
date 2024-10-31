# Microsoft-Cyber-Security-Incidents-for-ML

Problem Statement

As a data scientist at Microsoft, your goal is to improve the efficiency of Security Operation Centers (SOCs) by creating a machine learning model that accurately predicts the triage grade of cybersecurity incidents. Using the comprehensive GUIDE dataset, we aim to develop a classification model that categorizes incidents as true positive (TP), benign positive (BP), or false positive (FP) based on historical evidence and customer responses.

Training Model Step by Step

Handling Large Dataset: Since the dataset is quite large, I split the data into smaller chunks using pandas and then combined all the chunks into a single DataFrame. This was necessary because my PC couldn't handle large datasets all at once.

Data Cleaning: I removed duplicate rows and dropped columns that had more than 55% missing values to clean up the data.

Encoding Categorical Values: I used Label Encoding to convert categorical values into numeric ones.

Under Sampling: Due to my PC's limitations in handling big data, I used the imblearn RandomUnderSampler package to under-sample the data.

Feature Selection: Given that our target feature is categorical, I used the Chi-Squared test for categorical columns and the ANOVA test for numerical columns to find the p-values. I then selected the top features with p-values less than 0.05.

Creating a New DataFrame: With the selected features, I created a new DataFrame for training. I also checked the correlation between features using a heatmap.

Splitting the Data: I split the DataFrame into target and label features.

Training Models: I trained the data using three classification models and selected the best one based on performance.

Saving the Model: Finally, I saved the best model using JOBLIB for testing purposes.

Note: As a fresh graduate and a curious learner, I experimented with various techniques in undersampling and feature selection. The steps above reflect the finalized approach I used to train the model.

Metrics for Test Data:

Accuracy: 0.9257820344308735
Recall: 0.9203978879535909
F1 Score: 0.9180690192423975
Precision: 0.915933680899041


Thank You

Rafadh Rafeek
