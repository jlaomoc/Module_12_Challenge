# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

## Purpose:
The purpose of this analysis was to use various types of supervised machine learning architures to create a model that can evaluate the creditworthiness of borrowers. In order to create this model, I used the Linear Regression model and noticed the model would be baised towards healthy loans due to healthy loans having significant higher count compared risky loans. To offset the balanced, I used Random Oversampler to balance the dataset to ensure the model can results in a less bias and higher recall. 

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
In model 1 I used Linear Regression to split the model into features (X) and my label(y). Where my features X would determine if my label would be healthy loan or risky loans. Than I split the data into testing and training datasets to train the model to see if it could correctly predict if the outcome should be healthly loan or high risk loans. I used the testing data to predict the outcomes and compared it with my testing data to ensure the machine can accuratly label a healthy or high risk loan. 

Regardless of the precision and accuracy being high the recall was quite low. With that being said the model's accuracy was 95% with a precision of 100% and a recall of 91% for healthy loans. The model produced great results but considering the recall being at 91% for risky loans and a precision of 85% the model still would have inncorrectly identifed 9% of loan borrowers are healthy loans when in reality their loans should have be rejected. In turn these loans can have a negative impact on profit resulting in a greater loss for the company, for 9% of borrowers would not be able to pay back their loans. 

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

In model 2 I used the same method but instead used Random Oversampling to balance the dataset before using Liner Regression to predict the outcome of healthy loan and risky loans. The precision for heatlhy loans was 100%, with an accuarcy of 99% and a recall of 99%. Which has the same results found in Model 1. For risky loans the results differ slightly from Model 1, with the precision going down 84%, but the recall increasing to 99% and an accuarcy of increasing to 99%. Which is good because that means the the model was able to correctly idenifty high risk loans by 8%. Which is beneifical considering I wanted a model with a higher recall because that meant my false negatives would decrease. Resulting in the model having a higher accuracy of idenfity if a borrower is high risk.


## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

To summarize my results, Random Oversampling with Linear Regression was a better model to use compared to Linear Regression using my original value counts. Model 1 dataset was biased and unbalanced which lead to the model not being the best one to use. Using the original dataset without resampling and balancing the dataset resulted in a lower recall and accuracy for risky loans at 91% and 95%. The model still preformed well but considering it mislabelled 9% as healthy opposed from risky can lead to a greater impact in loss in the future. When I used Random Oversampling with Linear Regression you notice a significant increase with the accuracy and recall scores to 99%. Indicating random over sampling and linear regression preformed better because the model was able correctly idenfity 99% risky loan borrowers which would in turn would have a less negative impact in gain and losses for the company. In conclusion, by balancing the dataset I was able to remove the biases which lead to a greater outcome for the model 2. Therefore, I found model 2 to perform better because it was able to increase the recall and accuracy to correctly identify high risk loans borrowers which in turn would be better for companies to migate their loss for a borrower who would not be able to pay back their loan. 

I would recommend Random Forest because it combines mutliple decisions into a single result, which is useful because there are a lot of factors that come into play when deciding the creditworthness of a borrower. Random forest increases diversity leading to a more robust overall prediction and thakes an average of all the individual decisions in each trees. It can also provides feature importance, which can be valuable for understanding the key factors influencing creditworthiness.

References:
- https://williamkoehrsen.medium.com/random-forest-simple-explanation-377895a60d2d#:~:text=The%20fundamental%20idea%20behind%20a,to%20the%20mark%20on%20average.
- https://towardsdatascience.com/performance-metrics-confusion-matrix-precision-recall-and-f1-score-a8fe076a2262

