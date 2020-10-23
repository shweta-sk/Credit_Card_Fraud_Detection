# Credit_Card_Fraud_Detection
This dataset can be viewed at https://www.kaggle.com/mlg-ulb/creditcardfraud

The datasets contains transactions made by credit cards in September 2013 by european cardholders. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

It contains only numerical input variables which are the result of a PCA transformation. Unfortunately, due to confidentiality issues, we cannot provide the original features and more background information about the data. Features V1, V2, … V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-senstive learning. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.

When we started performing operations we found that the normal transactions were way more then the fraud transactions. Dataset is said to be balanced if both type of transactions are in 50:50 ratio or atleast 60:40 ratio, but in this case it is not. It is clearly a form of imbalance dataset.

#Dealing with imbalance dataset
To deal with imbalance dataset there are two techniques:

Under Sampling: In this form, data is randomly selected from the normal category to match the number of fraud data with a 50:50 percent ratio
Over sampling: In this form, we add more data to Fraud category, we add data in the same dimention . Suppose the ratio of normal vs fraud transaction is 9:1, so we would add 9 times same data for fraud to make it even.
There is one library in python which is used to deal with imbalance dataset which is 'imblearn' and it has two functions that deal with different types of handling imbalance dataset technique: nearmiss(for under samping) and SMOTETomake(over sampling).
