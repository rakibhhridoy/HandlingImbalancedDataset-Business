# Handling Imbalanced Data
<img src="/images/roc_auc.jpg" alt="" height="500px" width="800px">
It is important that credit card companies are able to recognize fraudulent credit card transactions so that
customers are not charged for items that they did not purchase. <br>
This dataset is a bespoke dataset which contains transactions made by credit cards. This dataset contains transactions, where we have 180 frauds out of 4700 transactions. The dataset is highly imbalanced, the positive class (frauds) account for 3.83% of all transactions.
It contains only numerical input variables which are the result of a PCA transformation. The input features are transformed to maintain the confidentiality of the original features and more background information about the data. Features PC1, PC2, … PC5 are the principal 
components obtained with PCA, the only feature which have not been transformed with PCA is 'ID' and 'Class'. Feature 'Class' is the response variable and it takes value ```1 in case of fraud and 0 otherwise```.



### Handling Overview
For this dataset let's consider fraudulent transactions (which are denoted as 1 in the dataset) is positive class and the non fraudulent transactions (which are denoted as 0 in the dataset) is negative class.
    -    ```TP``` - transactions which are actually fraudulent and the model also able correctly identify them as fraudulent transactions
    -    ```FP``` - transactions which are actually non fraudulent transactions but the model is predicting them as fraudulent transactions
    -    ```TN``` - transactions which are actually non fraudulent transactions and model is also predicting them as non fraudulent transactions
    -    ```FN``` - transactions which are actually fraudulent but the model is predicting them as non fraudulent transactions.

<hr>
<img src="/images/confusion_matrix.PNG" alt="" height="200px" width="400px">


### Before Imbalancing solved model accuracy

```
                precision       recall      f1-score        support

            0   0.97            0.99        0.98            1360
            1   0.15            0.04        0.06            50


    accuracy                                0.96            1410
   macro avg    0.56            0.52        0.52            1410
weighted avg    0.94            0.96        0.95            1410
```



### After Solving Imbalanced Issue
##### Applying oversampling method ```SMOTE```

```
                precision    recall  f1-score   support

           0       0.98      0.95      0.96      1360
           1       0.23      0.42      0.30        50

    accuracy                           0.93      1410
   macro avg       0.60      0.68      0.63      1410
weighted avg       0.95      0.93      0.94      1410
```
<hr>

Applying Hyperparameter Tuning
```
                precision    recall  f1-score   support

           0       1.00      0.82      0.90      1360
           1       0.17      1.00      0.29        50

    accuracy                           0.83      1410
   macro avg       0.59      0.91      0.60      1410
weighted avg       0.97      0.83      0.88      1410
```

#### Our Target was correctly identified transactions as normal or TPR. After Tuning our TPR/Recall became 1.00.. So our model is now well generalized.

<hr>
<br>
<br>
Connect with me- https://linkedin.com/in/rakibhhridoy 
<br>
Website- https://rakibhhridoy.github.io 