# Linear Regression
## Introduction to linear regression
Linear regression is a model that assumes a linear relationship between the input variables (x) and the single output variable (y).

x: independent variable (explanatory variable)

y: dependent variable (response variable)

x variable is used to predict the y variable.

![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/Prices.png)

[simple regression](https://www.youtube.com/watch?v=KsVBBJRb9TE&ab_channel=jbstatistics)

## Running Linear regression in Python scikit-Learn
 You can do linear regression using numpy, scipy, stats model and sckit learn.
 
 [Sourse of scikit-learn](https://scikit-learn.org/stable/)
 
 
 - import libraries.
 
 ![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/Explore-1.png)
 
 - download data set.
 - convert data to pandas data frame.
 - determine dependent and independent variables.
 - import linear regression from sci-kit learn module.

![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/Skitlearn-linear-model1.png)

 - make a plot of your data.
 - create a line that takes most of the points on the plot.
 - notice the relationship between variables.
 
> Important functions to keep in mind while fitting a linear regression model are:

> lm.fit() -> fits a linear model

> lm.predict() -> Predict Y using the linear model with estimated coefficients

> lm.score() -> Returns the coefficient of determination (R^2). A measure of how well observed outcomes are replicated by the model, as the proportion of total variation of outcomes explained by the model.
 
 ### How to do train-test split:
 You have to divide your data sets randomly. Scikit learn provides a function called train_test_split to do this.
 ![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/Xtrain-and-Xtest.png)
 
 - building a linear regression model using my train-test data sets.
 
 ![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/Linear-reg.png)
 
 ## Residual plots
 - Residual plots are a good way to visualize the errors in your data.
 - your data should be randomly scattered around line zero

![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/Plt-scatter.png)

this would result as follows:

![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/Residual-plot.png)

[More](https://bigdata-madesimple.com/how-to-run-linear-regression-in-python-scikit-learn/)


## Conclusion
Linear regression is a basic and commonly used type of predictive analysis.

it is used to test the following:
1. does a set of predictor variables do a good job in predicting an outcome (dependent) variable?
2. Which variables in particular are significant predictors of the outcome variable?

   a. in what way do they–indicated by the magnitude and sign of the beta estimates–impact the outcome variable?

- The simplest form of the regression equation with one dependent and one independent variable is defined by the formula `y = c + b*x` where:

 y = estimated dependent variable score.
 c = constant.
 b = regression coefficient.
 x = score on the independent variable.
 
 [More on types of linear regressions](https://www.statisticssolutions.com/free-resources/directory-of-statistical-analyses/what-is-linear-regression/)
 
 
 ## Train/Test Split and Cross Validation in Python
 
 ## Overfitting/Underfitting
 Data is usually split into two subsets:
 1. training data
 2. testing data
 model is fit on the train data, in order to make predictions on the test data. while doing that overfitting/underfitting might happen:
 
- Overfitting means that model we trained has trained “too well” and is now, well, fit too closely to the training dataset. This usually happens when the model is too complex.
- Underfitting means that the model does not fit the training data and therefore misses the trends in the data. It also means the model cannot be generalized to new data.
 
 ![](https://miro.medium.com/max/555/1*tBErXYVvTw2jSUYK7thU2A.png)

 
 [More on test split](https://towardsdatascience.com/train-test-split-and-cross-validation-in-python-80b61beca4b6)
