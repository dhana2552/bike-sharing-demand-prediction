# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
The submission wont be accepted if the counts have negative values

### What was the top ranked model that performed?
The model with hyperparameter tuning

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
In Exploratory analysis, the histograms were used to display the distribution of each one relative to the data. Also, separating the date field into day, month, hour increased the value to the project. As the project was all about getting the counts based on certain features, this split gave a better insight when checked with the histogram again.

### How much better did your model preform after adding additional features and why do you think that is?
As we have more feature relavent features, the score of the model can be increased which is an evident in this project. 

## Hyper parameter tuning
### How much better did your model perform after trying different hyper parameters?
Found an increase in overall performance when checked in leaderboard and summary

### If you were given more time with this dataset, where do you think you would spend more time?
Hyperparameter tuning

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|Default Values|Default Values|Default Values|1.39764|
|add_features|Default Values|Default Values|Default Values|0.54073|
|hpo|GBM: 'num_boost_round': 100,
    'num_leaves': ag.space.Int(lower=26, upper=66, default=36)
    |NN: 'num_epochs': 10,
    'learning_rate': ag.space.Real(1e-4, 1e-2, default=5e-4, log=True),
    'activation': ag.space.Categorical('relu', 'softrelu', 'tanh'),
    'layers': ag.space.Categorical([100], [1000], [200, 100], [300, 200, 100]),
    'dropout_prob': ag.space.Real(0.0, 0.5, default=0.1)
    |Default Values
    |0.52616|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![model_test_score.png](img/model_test_score.png)

## Summary
The model was performing well with its auto tuned hyperparameter. However, with manually tuning on individual models like GBM and NN, it was not so well even after trying with various parameter values. Hence, there is a need to do a better feature engineering and trying with more hyperparameter tuning can help on improving the performance. 
