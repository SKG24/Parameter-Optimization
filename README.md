# Parameter-Optimization
***Overview*** 
This project applies Support Vector Machine (SVM) classification using scikit-learn to a dataset where the target variable is letter.
***Methodology Data Preprocessing:***

The target label letter is encoded to numeric using LabelEncoder.

The feature matrix X and label vector y are split from the DataFrame.

***Model Training and Hyperparameter Tuning:***

We run the experiment over 10 different train-test splits (test_size=0.3, random_state = 0 to 9).

For each split:

A loop tries 100 values of C, linearly spaced from 0.1 to 10.

Each configuration trains an SVC model with an RBF kernel.

Test accuracy is recorded for each value of C.

The best-performing C and its corresponding accuracy are saved.

***Results Table***


***Convergence Graph***

This figure shows the accuracy at each iteration (i.e., for each value of C) for the best-performing train-test split.
