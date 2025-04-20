# Parameter-Optimization
***Overview*** 
This project applies Support Vector Machine (SVM) classification using scikit-learn to a dataset where the target variable is letter.
***Methodology Data Preprocessing:***

The target label letter is encoded to numeric using LabelEncoder.

The feature matrix X and label vector y are split from the DataFrame.

***Model Training and Hyperparameter Tuning:***

We run the experiment over 10 different train-test splits (test_size=0.3, random_state = 0 to 9).

For each split:

A loop tries 50 values of C, linearly spaced from 0.1 to 10.

Each configuration trains an SVC model with an RBF kernel.

Test accuracy is recorded for each value of C.

The best-performing C and its corresponding accuracy are saved.

***Results Table***
=== Best Parameters and Accuracies (Table 1) ===

   Sample  Best Accuracy                     Best Parameters
0       1       0.967333     {'C': 10.0, 'kernel': 'rbf', 'gamma': 'scale'}
1       2       0.962333     {'C': 10.0, 'kernel': 'rbf', 'gamma': 'scale'}
2       3       0.963167     {'C': 10.0, 'kernel': 'rbf', 'gamma': 'scale'}
3       4       0.961667     {'C': 10.0, 'kernel': 'rbf', 'gamma': 'scale'}
4       5       0.959167     {'C': 10.0, 'kernel': 'rbf', 'gamma': 'scale'}
5       6       0.960833  {'C': 9.595918367346938, 'kernel': 'rbf', 'gam...
6       7       0.958167     {'C': 10.0, 'kernel': 'rbf', 'gamma': 'scale'}
7       8       0.964333  {'C': 8.585714285714285, 'kernel': 'rbf', 'gam...
8       9       0.965167  {'C': 9.79795918367347, 'kernel': 'rbf', 'gamm...
9      10       0.963500     {'C': 10.0, 'kernel': 'rbf', 'gamma': 'scale'}


***Convergence Graph***
![Screenshot 2025-04-20 at 3 41 01 PM](https://github.com/user-attachments/assets/70d9a868-dac9-4fb9-852c-6a4b6265b6bd)


This figure shows the accuracy at each iteration (i.e., for each value of C) for the best-performing train-test split.
