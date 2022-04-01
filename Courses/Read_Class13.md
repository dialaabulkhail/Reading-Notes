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
 
