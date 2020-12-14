# Bias and Variance
***

First, we will understand what defines a model’s performance, what is bias and variance, and how bias and variance relate to under-fitting and over-fitting. Then we will understand how to fix the bias variance.

**How do we know if a model is performing well?**
A machine learning model’s performance is considered good based on it prediction and how well it generalizes on an independent test dataset. Based on the performance of different models we choose the model which ranks highest in performance.

## Example :- 
Let’s understand this with an example, let’s say we want to predict who will do well in the election of 2020, will it Republican or Democrats?
We go to a neighborhood and start asking people if they would vote for a Democrat or a Republican. we interview 100 people, 47 say they will vote for Democrats, 33 say they will vote for Republican and 20 are undecided. Based on this data we can make a prediction that chances of Democrats winning is higher than Republicans.

## Can we apply this prediction to the entire county, state and then at national level?
No, because the prediction might change if we go to a different neighborhood or a different county or state. We will observe inconsistencies in the prediction. This means our model is not performing well as it cannot be used reliably to make predictions.
One of the reason for our model to performance is due to small sample size and not having enough variation in the data. This introduces error in our prediction. Error is when the predicted value is different from the actual value.

**When we have an input x and we apply a function f on the input x to predict an output y. Difference between the actual output and predicted output is the error.** Our goal with machine learning algorithm is to generate a model which minimizes the error of the test data set.

Models are assessed based on the prediction error on a new test data set.  
$ L(x,y)=∑(y-f(x))^2 $


Error = sum of all (actual output– predicted output)

Error in our model is summation of reducible and irreducible error.

$$Error = Reducible error + irreducible error$$

$$Reducible error= bias^2+variance$$

## Irreducible Error
Errors that cannot be reduced no matter what algorithm you apply is called an irreducible error. It is usually caused by unknown variables that may be having an influence on the output variable.

Reducible Error has two components bias and variance.

Presence of bias or variance causes over-fitting or under-fitting of data.

## Bias
* Bias is how far are the predicted values from the actual values. If the average predicted values are far off from the actual values, then the bias is high.
* High bias causes algorithm to miss relevant relationship between input and output variable. When a model has a high bias then it implies that the model is too simple and does not capture the complexity of data thus under-fitting the data.

## Variance
* Variance occurs when the model performs good on the trained dataset but dose not do well on a dataset that it is not trained on, like a test dataset or validation dataset. Variance tells us how scattered the predicted value from the actual value are.
* High variance causes over-fitting that implies that the algorithm models random noise present in the training data.

we would like to have a model complexity that trades bias off with variance so that we minimize the test error and would make our model perform better. This is illustrated the bias variance trade off below.

