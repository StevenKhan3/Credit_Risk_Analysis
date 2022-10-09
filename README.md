# Credit_Risk_Analysis

## Overview
The aim of this investigation was to develop and assess alternative machine learning models to assess the credit risk of each individual consumer. The dataset from LendingClub, "a peer-to-peer loan services company," was utilized to train the models. The dataset, which included 68,817 entries after cleaning, was severely uneven, with only 0.5% of them being designated as "high-risk."

The machine learning algorithms used were:
* RandomOverSampler
* SMOTE
* ClusterCentroids
* SMOTEENN
* BalancedRandomForestClassifier
* EasyEnsembleClassifier

The models were run and then evaluated for performance and accuracy at predicting credit risk.

## Results
Based on their Balanced Accuracy Scores, the results below are presented in descending order of performance, starting with the model that performed the poorest and working up to the best.

* **Cluster Centroids Undersampling**had the worst outcomes for us, with an accuracy rating of 0.5295. This suggests that it had a 50/50 chance of correctly predicting credit risks, or it fared little better than that. Its F-scores were also unimpressive, coming in at only 0.56 on average and 0.01 for high-risk prediction.

* **Combination Sampling**with an accuracy score of 0.6529, gave us the second-worst outcomes. This means that it had a prediction accuracy of only 65%, or around two thirds. Its F-scores were nevertheless poor, coming in at only 0.72 on average and 0.02 for high-risk prediction.

* **SMOTE Oversampling**with an accuracy score of 0.662, gave us the third-worst outcomes. This performance is comparable to that of **Combination Sampling**. This indicates that its ability to estimate credit risks was only slightly above 66%, or 2/3rds, accurate. Its F-scores were likewise poor, with a 0.80 average improvement on the previous F-score and a 0.02 F-score for high-risk prediction.

* **Naive Random Oversampling** brings our model performances to a halfway point. We received the third-best results from the ROS model, which had an accuracy rating of 0.6732. This performance is still comparable to what we observed using combination sampling and SMOTE oversampling. This indicates that its ability to estimate credit risks was only slightly above 67%, or 2/3rds, accurate. Also worse or comparable to **SMOTE Oversampling** were its F-scores.The ROS model achieved an average of 0.76 and another F-score for high-risk prediction of only 0.02.

* **Balanced Random Forest Classifier**gave us the second-best outcomes, with an accuracy score of 0.7615 demonstrating a substantial improvement. This is still far from ideal, though. This suggests that only 76% of the necessary levels of credit risks could be accurately predicted, or 3/4 of them. Where there was the most improvement was in its F-scores (relatively). The average F-score for the BRFC model was 0.92, which is at least in the 90s. Its F-score for high-risk prediction was only 0.06, which is still very low.

* **Easy Ensemble AdaBoost Classifier**was, by far, the model that performed the best. The outcomes much beyond those of any other models that had been tried. We received a score of 0.9319 for accuracy. While not flawless, this indicates that it could correctly estimate the right levels of credit risks at a rate of more than 93%.    It's F-scores were also fairly impressive. The EEC model achieved an average F-score of 0.97. However, while the best performing, it's F-score for high-risk prediction was still low, at only 0.16.      

## Summary 
In conclusion, credit-risk is a difficult thing to predict, even for advanced machine learning algorithms with 93 columns of data to process. While the **Easy Ensemble AdaBoost Classifier** model had the highest overall accuracy, this was largely due to the fact that the dataset was so radically unbalanced. Even when it's balanced accuracy and average F-score were above 90%, it's F-score for high-risk prediction was no better than 0.16. In the end, I would advise against using any of these algorithms, as it would put creditors as too great of risk being unable to accurately predict who the high-risk clients/debtors would be.
