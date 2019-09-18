1. **What is the approximate depth of a decision tree trained (without restrictions) on a training set with 1 million instances?**
the depth is approx. `log(m)^3`, so in this case `log(10^6)` ~ 20.

2. **Is a node's Gini impurity generally lower or greater than its parents? Is it generally lower/greater, or always lower/greater?**
As you traverse down the list, the chances of an instance being another class increases as the depth increases, therefore it is generally the case that as you traverse down the Gini index becomes less pure (ie Gini index increases), however this is not always the case, especially in bivariate classifications, where the gini index at the root is less, and it's children will be 0. 

3. **If a Decision Tree is overfitting the training set, is it a good idea to try decreasing the `max_depth`**
Reducing the depth reduces the degrees of freedom the tree has, in doing so will being to reduce overfitting. 

4. **If a decision tree is underfitting, is it a good idea to try scaling the input features?**
Scaling has no effect on decision trees, however you can try changing the min_* max_* hyperparamters

5. **If it takes one hour to train a Decision Tree on a training set containing 1 million instances, roughly how much time will it take to train another Decision Tree on a training set containing 10 million instances?**
Training the decision tree unlike predicting compares all features (unless `max_features` is set), this results in a complexity of `O(n * m*log(m))`

6. **If your training set contains 100,000 instances will setting presort=True speed up training?**
No this will slow down the training considerably. 