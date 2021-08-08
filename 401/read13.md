# Read 13: Linear Regressions

## Linear Regression

- A predictive analysis technique which uses a model(mathematical equation, that shows the relationship between the output and the input.

- Formula(simplest):
```
- y = c + b*x
```
### What is Scikit-learn?
- It's a powerful Python module for machine learning. 
It contains function for regression, classification, clustering, model selection and dimensionality reduction.

- In linear regression Scikit-learn used for fitting the model and predicting the output.
### Things to do & functions to use:

- Import (LinearRegression) from sklearn.linear_model.
- create a linear regression object
- lm.fit() --> fits a linear model
- lm.predict() --> Predict Y using the linear model with estimated coefficients
- lm.score() --> Returns the coefficient of determination. 

### Training and validation data sets

- data sets should to be split, such a certain percentage is used for the purpose of training the model and the remaining percentage is used for the purpose of testing and validating the model.
```
    lm = LinearRegression()
    lm.fit(x_train, y_train)
    pred_train = lm.predict(x_train)
    pred_test = lm.predict(x_test)
```
### Residual Plots
- Residual plots is a good way to visualize the errors in data. Good job's data should be randomly scattered around line zero.

### Simple Linear Regression With scikit-learn :
There are five basic steps when you’re implementing linear regression:

1. Import the packages and classes.
2. Provide data to work with and eventually do appropriate transformations.
3. Create a regression model and fit it with existing data.
4. Check the results of model fitting to know whether the model is satisfactory.
5. Apply the model for predictions.


 