### Exercises pg.57

1. **How would you define machine learning?**
ML is the process of giving a machine data so that it can find underlying patterns and use these patters improve the performance of future data.

2. **Can you name four types of problems where it shines?**
* Supervised Learning - Where the data used for training is labelled with the expected results. Eg. Spam Filter for emails.
* Unsupervised Learning - The machine tries to find appropriate boundaries given unlabelled data - Identifying topics from newspaper articles.
* Semi-Supervised - A machine is given some labelled and some unlabelled data. - Stock Price Forecasting, Weather Prediction
* Reinforcement Learning - A model is set up into an environment and is forced to learn from actions, rewards and punishments.

3. **What is a labelled Training Set?**
A labelled training set is a set of data which contains expected outputs for a machine learning process.

4. **What are two most common supervised tasks?**
* Spam Filters
* Image classification

5. **Can you name four common unsupervised tasks?**
* Topic modelling of News Paper articles
* music recommendation


6. **What type of ML Algorithm would you use to allow a robot to walk in various unknown terrains?**
Reinforcement Learning 

7. **What type of algorithm would you use to segment your customers into multiple groups?**
KNN - Where you could identify boundaries on the different types of customers.

8. **Would you frame the problem of spam detection as supervised or unsupervised?**
It would be more accurate if it were supervised, because you could label a bunch of spam emails manually which will result in a more accurate model when predicting future spam/ham emails.

9. **What is an online learning system?**
An online learning system is where a machine learning model is put to use in the real world, and is given data real time to be processed and trained. 

10. **What is out-of-core learning?**
OOC is a form of online learning, where the data is so big, that it cannot all fit in memory, so the algorithm loads only part of the data, trains it and then repeats it on all segments of data.

11. **What type of learning algorithm relies on a similarity measure to make predictions?**
K-Nearest Neighbour

12. **What is the difference between a model parameter and a learning algorithms hyperparameter?**
A Learning algorithms hyperparameters concerns itself of the degrees of freedom the model has, so it doesn't overfit the data. 

13. **What do model-based learning algorithms search for? What is the most common strategy they use to succeed? How do they make predictions?**
Model based learning search for underlying patterns in the data, instead of memorizing the data by heart. So they rely on effective evaluations and performance measures to succeed. ie they need to be able to fit the data both in a training set and a test set. So that they make it reliable predictions on unseen data. 
Model based algorithms make predictions by applying the fine tuned hyperparameters and model parameters to new data. 

14. **Name four main challenges in Machine Learning?**
    1. Models over generalise data, 
    2. Sometimes more data is required for a better model, this is time consuming and expensive
    3. It can be labour intensive with labelling a lot of data before applying models
    4. No Free Lunch. There is no optimal machine learning model that will get you the answers you need. It is all based off assumptions. 

15. **If your model performs great on the training data but generalizes poorly to new instances, what is happening? Name three solutions**
The model is overfitting, this means it has generalised to the training set, and is unable to recognise the patterns in unseen data. 
To solve this you could:
    1. Get more data
    2. extract more features
    3. fine tune the hyperparameters so there is more freedom in the model.

16. **What is the test set and why would you use it?**
The test set is a set of unseen data you apply your model to. The test set is a good way to confirming your model hasn't overfit the training data.

17. **What is the purpose of a validation set?**
When you apply a bunch of hyperparameters to models to try and reduce overfitting, you will usually test the validity of the hyperparameters on the test set, however this causes an issue because the model begins to overfit the test set too. So a validation set is a whole new set of unseen data where you can test the hyperparameters with, and once you have the optimal hyperparameter you can test it using the test data.

18. **What can go wrong if you tune hyperparameters to the test set?**
Your model starts to generalise with the test set.

19. **What is cross-validation and why would you prefer it to a validation set?**
Cross validation is the process of creating a new set of unseen data for each hyperparameter test, this is an ideal way to prevent overfitting. 