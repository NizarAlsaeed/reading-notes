# How to run Linear regression in Python scikit-Learn 

Scikit-learn is a powerful Python module for machine learning, we will use sklearn at first (not pandas).

data is loaded as dictionary in sklearn so you can use `.keys()` and `.values()`.

to print the feature names (headers) of the data set. use `.feature_names` properity

to see the description of this data set, use `.DESCR` properity

to convert the data into a pandas data frame.

df = pd.DataFrame(`<name>.data`)


### steps into a LinearRegression model 
1. import
```python 
from sklearn.linear_model import LinearRegression
```

LR.fit() -> fits a linear model

LR.predict() -> Predict Y using the linear model with estimated coefficients

LR.score() -> Returns the coefficient of determination (R^2). 
>A measure of how well observed outcomes are replicated by the model, as the proportion of total variation of outcomes explained by the model. 


2.`LR.fit(X,y)`

3.`LR.predict(X)`


### train-test split
You can create training and test data sets manually, but this is not the right way to do because You have to divide your data sets randomly. Scikit learn provides a function called train_test_split to do this.

```python
X_train, X_test, y_train, y_test = sklearn.cross_validation.train_test_split(X,y, test_size=0.33, random_state = 5) 
```




