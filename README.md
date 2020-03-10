# whelan_Credit_Risk

## Module 17 Challenge Analysis

### Part 1: Resampling

#### Naive Oversampling

Accuracy Score: 66.03%

Our first method of identifying loan risk, naive oversampling, achieves nearly a 2/3 accuracy score. This method correctly flags 75 of 101 high risk loans for a high-risk recall rate of 74%; however, by falsely flagging over 7000 low-risk loans it only achieves a precision score of 1%. For our first attempt at this problem, this is a fairly good outcome. The cost to LendingClub of falsely flagging a low-risk loan for additional scrutiny is much lower than not flagging a high-risk loan and having it god bad. However, we should strive to improve the number of flasley flagged loans while not reducing the number of correctly flagged ones.

#### SMOTE Oversampling

Accuracy Score: 65.37%

The second method, SMOTE Oversampling, improves on our first method by reducing the number of falsely flagged loans to 5400; however, in doing so it also reduces the high risk recall score to 62%. This is likely not an effective trade-off for LendingClub as a higher recall score is more desireable than a higher precision score.


#### Undersampling

Accuracy Score: 53.30%

Undersampling is significantly less effective than naive oversampling by every metric and should not be used.

#### SMOTEEN Combination Resampling

Accuracy Score: 64.48%

SMOTEEN Combination Resampling achieves a marginally lower accuracy score, high-risk precision score, and high-rish recall score than naive oversampling. With this data set, naive oversampling proves superior, but the difference is within a reasonable margin of error so the two methods should be tested on additional data sets. 


### Part 2: Ensemble Classifiers

#### Balanced Random Forests

Accuracy Score: 78.55%

Balanced Random Forest Classification improves significantly on the high-risk precision scores of the resampling methods, only falsely flagging 1749 low risk loans. However, with a high-risk recall score of 67%, it correctly flags fewer loans than naive oversampling and SMOTEEN resampling. The margin here is significant enough though that the reduced man hours necessary to scrutinize the falsely flagged loans may make up for missing the several high-risk loans the others catch with their significantly wider nets.

#### Easy Ensemble AdaBoost Classifier

Accuracy Score: 93.17%

Our last method proves itself to be the most effective by every metric and the comparison to the others methods is not even close. This method correctly flags 92% of the high-risk loans while achieving a high-risk precision score of 9%. By using this method to calculate lending risk, LendingClub can correctly capture the vast majority of risky loans while minimizing the amount of man-hours necessary to provide additional scrutiny to good loans.


One final note, further analysis comparing the loans correctly and incorrectly flagged by each of the models could prove elucidating to see if some combination of the models could increase the accuracy of our predictions even further.

