## Training Models

1. **What Linear Regression training algorithm can you use if you have a training set with millions of features?**
Stochastic Gradient Descent is a viable option, since it only loads a single instance into memory at a time.

2. **Suppose the features in your training set have very different scales. What algorithms might suffer from this, and how? What can you do about it?**
Algorithms such as Ride, Lasso and most regularized models, because it is sensitive to the scale of the input features. As this may causes erratic behaviour when trying to minimize the cost function. 
Options you could take would be to apply a transformer such as `StandardScaler` or `MinMaxScaler` to the features. 

3. **Can Gradient Descent get stuck in a local minimum when training a Logisitic Regression Model?**
Log Reg uses Gradient Descent and in doing so has the potential of being stuck in a local minimum depending on the hyperparameters you use, and the time you take to try to find it.
**A.** Log Reg cannot get stuck in a local minium because the cost function is convex.

4. **Do all Gradient Descent algorithms lead to the same model provided you let them run long enough?**
Yes, if time was not an issue, you could set any hyperparameter and you will find that the model will eventually converge to a global minimum, if time was an issue, there are chances it will get stuck in a local minimum.

5. **Suppose you use Batch Gradient Descent and you plot the validation error and each epoch. If you notice the validation error consistently goes up, what is likely going on? How can you fix this?**
This means you have over shot the global minimum, and this is usually due to setting a learning rate that is too high, try lowering the learning rate and increasing the number of iterations. 

**A**. If the validation error goes up, that means the learning rate may be too high and the algorithm is diverging. It the Training error also goes up too, then you should reduce the learning rate.

6. **Is it a good idea to stop Mini-Batch Gradient Descent immediately when the validation error goes up?**
Since Mini-Batch gradient is based random instance in every iteration, stopping the algorithm immediately when the validation error goes up may leave you stuck in a local minima. 

7. **Which Gradient Descent algorithm will reach the vicinity of the optimal solution the fastest? Which will actually converge? How can you make the others converge as well?**
Mini-Batch gradient descent will react the vicinity of the optimal solution the fastest because it only loads single random instances and perform gradient descent. Batch Gradient descent will actually converge, the other algorithms can converge too depending on their learning rate and num of iterations.

**A**: SGD is the fastest to converge since it considers only on training instance at a time. 

8. **Suppose you are training polynomial regression. You plot the learning curves and you notice that there is a huge gap between the training error and validation error. What is happening? What are the three ways to solve this?**
The gap suggests the model is overfitting the data. You could add more features to the data, add more data or increase the degrees of freedom for the model. 

**A**: you should try to reduce the degrees of freedom not increase it, because a model with less degrees of freefom is less likely to overfit. You can also try to regularize the model eg. add a l2 penalty (Ridge) or an l1 penalty (Lasso). This will reduce the degrees of freedom. 

9. **Suppose you are using Ridge Regression and you notice that the training error and the validation error are almost equal and fairly high. Would you say that the model suffers from high bias or high variance? Should you increase the regularization hyperparameter or reduce it?**
High Bias indicates the data is underfitting, as does having almost equal training and validation errors. This model is High Bias, you should decrease the reg param in order to get more degrees of freedom ie higher variance, b/c it may be that a linear model is attempting to fit a quadratic curve.

10. Why would you want to use:
* Ridge Regression instead of Plain Linear Reg (without regularization)
* Lasso Instead of Ridge
* Elastic Net instead of Lasso?
Using Ridge is always a better idea than using plain Linear Regression, because of regularization, it will help you model fit the data accurately. 
Use Lasso Over Ridge in cases where you are sure which features are useful and which features aren't.
Elastic Net is a combination of both Lasso and Ridge when you use the `r` hyperparameter, this is for more fine tuning. 

**A** Lasso uses an l1 penalty which tends to push the weights down to exactly zero This leads to sparse models, where all weights are zero except for the most important weights. Lasso performs feature selection on its own this way. 
Elastic Net is generally preffered over Lasso, b/c lasso may behave erractilly in some cases (where several features are strongly correlated)

11. **Suppose you want to classify pictures as Outdoor/Indoor and daytime/nighttime. Should you implement two Logistic Regression classifiers or one softmax regression classifier?**
Softmax is a multiclass predictor not a multioutput, ie you cannot use softmax to classify different people in the same picture. so in this case, one picture can have a combination of either inside and daytime, inside and nighttime, or outside and daytime and outside and nighttime. Therefore you would have to use two log reg classifiers to determine this. 
