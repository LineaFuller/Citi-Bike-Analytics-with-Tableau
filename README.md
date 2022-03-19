# Predicting Credit Risk 

I built a machine learning model that attempts to predict whether a loan from LendingClub will become high risk or not.

LendingClub is a peer-to-peer lending services company that allows individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. LendingClub offers their previous data through an API.
I used data to create machine learning models to classify the risk level of given loans. Specifically, I compared my Logistic Regression model to my Random Forest Classifier.

## Retrieved the data

I retrieved the data from the provided 2019loans.csv and 2020Q1loans.csv files that contained an entire year's worth of data (2019) to predict the credit risk of loans from the first quarter of the next year (2020).

## Converted categorical data to numeric

I created a training set from the 2019 loans using pd.get_dummies() to convert the categorical data to numeric columns. Similarly, I created a testing set from the 2020 loans, also using pd.get_dummies().

## Compared the models

Before fitting and scoring my models, I made a prediction as to which of my models, my logistic regression or my random forests classifier would perform better. My prediction was not correct since I hypothesized that my logistic regression model would initially perform better. However, my Random Forests model performed better.


## Scale the data

Since the data going into my models was never scaled, I reprocessed the data by scaling it. I used StandardScaler to scale the training and testing sets. Before re-fitting the LogisticRegression and RandomForestClassifier models on the scaled data, I made another prediction as to which would perform better. This time my preidication was correct! After fitting and scoring my LogisticRegression and RandomForestClassifier models on the scaled data, my LogisticRegression model performed better.
