# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
The submission wont be accepted if the counts have negative values

### What was the top ranked model that performed?
The model with hyperparameter tuning

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
Splitting the date field into DAy, Month and Year and then plotting the histogram with new set of features helped on analyzing the data further

### How much better did your model preform after adding additional features and why do you think that is?
The day, month, year field had a better correlation with counts (label) then the date

## Hyper parameter tuning
### How much better did your model perform after trying different hyper parameters?
Found an increase in overall performance when checked in leaderboard and summary

### If you were given more time with this dataset, where do you think you would spend more time?
Hyperparameter tuning

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|None|None|None|1.39764|
|add_features|None|None|None|0.54073|
|hpo|GBM|NN|None|0.52616|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](img/model_test_score.png)

## Summary
Autogluon is a library that allows you to easily create and train machine learning models. It is a wrapper around scikit-learn, XGBoost, and other popular machine learning libraries. It is a Python library that allows you to easily create and train machine learning models. It is a wrapper around scikit-learn, XGBoost, and other popular machine learning libraries.
