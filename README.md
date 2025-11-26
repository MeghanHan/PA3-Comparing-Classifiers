# PA3-Comparing-Classifiers
This study compares the performance of the classifiers (k-nearest neighbors, logistic regression, decision trees, and support vector machines). The dataset is related to the marketing of bank products over the phone.

Links to [prompt](https://github.com/MeghanHan/PA3-Comparing-Classifiers/blob/main/comparing_classifiers.ipynb), [data](https://github.com/MeghanHan/PA3-Comparing-Classifiers/tree/main/data), and [images](https://github.com/MeghanHan/PA3-Comparing-Classifiers/tree/main/images)


## Data
The dataset comes from the UC Irvine Machine Learning Repository. It is from a Portuguese banking institution and is a collection of the results of multiple marketing campaigns.
## Business Objective
The Business Objective of the task is to identify the classifier (k-nearest neighbors, logistic regression, decision trees, and support vector machines) that is most suitable to predict whether a bank's client has subscribed to a term deposit based on bank information features.

## Findings
### Logistic Regression Model Coefficients
From analyzing the coefficients of the simple regression model, we have the following observations:
1) Employment status has the biggest predictive power on whether a client will subscribe to term deposit. Students and retirees have stronger preference for term deposits compared to people with jobs. Unemployed people prefer term deposits. Entrepreneurs especially dislike term deposits, which can be explained by their high-risk tolerance.
2) Credit is another strong indicator. People with good credit are more likely to subscribe to a term deposit. Data visualization shows that people who have credit in default don't have term deposits without exception. This can be explained by lack of self-discipline in spending.
3) Clients' education, age and whether they have housing or personal loans are less important when it comes to choosing to subscribe to a term deposit.
4) The effect of marital status is less obvious because there are more married clients in the dataset and one of the couples can hold term deposits for both.
   
### Comparing Models with Default Settings
When using the default setting of each model, Logistic Regression has the best performance on this dataset with high accuracy, only second to SVM classifier and much faster training speed, since Logistic Regression has much lower training complexity compared to SVM. Logistic Regression is also superior among these classifiers due to its high interpretability. 

KNN and Decision Tree models also have short fit time. But their test accuracy is below the baseline. The Decision Tree classifier appears to be overfitted.

### Comparing Models after Improvement
Grid search was conducted to fine tune the hyperparameters and improve the models. The performance of Decision Tree Classifier improved by limiting tree depth to reduce overfitting. Its accuracy is above baseline. The test accuracy of KNN model also improved after changing the number of neighbors, but the test accuracy is still below baseline and the average train time got much longer.

The performance of Logistic Regression didn't change after tightening and relaxing regularization hyperparameter. And the performance of SVM didn't change after testing out linear and polynomial kernels.

Logistic Regression is the best classifier for predicting whether a client would subscribe to term deposit based on banking information. It has the second highest test accuracy, and the lowest train time. The result has high interpretability. Logistic Regression is great for classifying linear features.
