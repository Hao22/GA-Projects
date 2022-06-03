# Project 2 - Ames Housing Data and Kaggle Challenge


## Problem Statement

This project aims to provide a reliable estimation of the value of properties located in the city of Ames in Iowa, USA. In this project, we will develop a regression model to predict the prices of properties based on a number of selected features. The accuracy and usefulness of the model will be evaluated by a number of metrics such as root mean squared error (RMSE) and R2 score. We hope that this model will potentially be useful to property investors that are looking to make a profit by flipping properties, or potential homeowners who do not want to pay a premium over the actual home value. 

## Data Sources
train.csv -- 2006-2010 Ames Housing training dataset (split for Kaggle competition)
test.csv -- 2006-2010 Ames Housing test dataset (split for Kaggle competition to predict house prices)

## Modelling Results
From the results of running our models with hyperparameter tuning, we see that the Lasso and Ridge Regression model have slightly worse performance and Elastic Net model having better performance.

It seems we have the flexibility to choose from a number of models according to the models' performance metrics. However, if we were to compare all of our models, pre and post hyperparameter tuning, our initial Linear Regression model, default Ridge Regression and default Lasso Regression model seemed to give us the best RMSE and R2 scores.

We ultimately decide to use the linear regression model as carrying out regularization did not seem to improve our model's performance. In addition, our linear regression model did not have a notable overfitting issue and thus there was no need to regularize our model, and we could also reduce complexity with just using the linear regression model.


## Conclusions and Recommendations
The linear regression model we built was based on selective feature selection and engineering, and the final model to predict the sale prices of the properties achieved an accuracy score of 86.3%, based on the cross-validation score we obtained for the linear regression model. The model also achieved a root mean squared error(RMSE) of 24338 and a R2 score of 0.9, representing a model that has a rather low error rate.

This would give property traders in Ames, the confidence to purchase a property if they deem it sufficiently undervalued, as well as prospective homebuyers to purchase a residential property if the model deems that the property is fairly valued.

However, our model does come with shortcomings, in that the accuracy of the model starts dropping when the sale prices exceed USD350,000. In such scenarioes, users would be advised to utilize the model for comparison's sake instead and not to over-rely on the absolute values churned by the model. To improve on the shortcomings, we could possibly further refine the model upon collecting more data of houses with sale prices above USD 350,000.