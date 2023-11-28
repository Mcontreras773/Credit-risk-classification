# Credit-risk-classification

---------- Overview of the Analysis ------------
- I worked with a dataset of 77,536 entries, consisting of 75,036 low-risk loans (0) and 2,500 high-risk loans (1). Each loan had eight attributes. The goal was to create a model to predict loan status accurately. First, I split the dataset into training and testing sets using scikit-learn. I then built a basic logistic regression model on the training set and applied it to the testing set. The classification report results for this initial model are provided under the "results" header.

Next, I used the RandomOverSampler module from the imbalanced-learn library to balance the training dataset. I generated 56,277 observations for both low and high-risk loans. After this, I built a second logistic regression model (classifier) with the same goal of predicting loan status. The classification report results for both models are presented below for comparison.

------------ Results -------------

Machine Learning Model 1:

Accuracy: 94%
Precision: 93% Average | 100% in low-risk loans, 87% in high-risk loans
Recall: 95% Average | 100% in low-risk loans, 89% in high-risk loans

Machine Learning Model 2:

Accuracy: 100%
Precision: 93% Average| 100% in low-risk loans, 87% in high-risk loans
Recall: 100%

-------------- Summary ------------------

In terms of overall accuracy, the model based on the resampled data (Model 2) outperformed the first model. However, when examining the confusion matrices, Model 1 displayed 80 false positives and 67 false negatives, while Model 2 showed 91 false positives and only 2 false negatives. In essence, Model 2 had a slightly higher count of false positives but significantly fewer false negatives. This implies that while Model 2 represents an improvement, both models could prove valuable in different scenarios.

If a bank is particularly concerned about avoiding the misclassification of high-risk loans as low-risk, Model 1 demonstrated better performance. On the other hand, if a bank is mindful of the implicit costs associated with identifying low-risk loans as high-risk and prioritizes a higher overall accuracy, Model 2 stands out as the better choice. It's noteworthy that both models scored below 90% in accurately predicting high-risk loans.

