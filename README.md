##### Predict-the-number-of-adults-with-Mental-issues > 14-days-in-an-year

The original purpose of building a model in which we can predic the counts of bad mental health among adults zipcode wise to assist Dynamic Health Inc. with targeting areas of high need for mental health support. In order to produce our final model, we ran three separate types of regression models.

The first model was a simple linear regression model. Although the R squared was relatively close to 1 for both the train and the test, the error metrics were not nearly as strong. Additionally the train results were better than the test results. For these reasons we tried using a model with pipeline and hyperparameter tuning.
In preparation for further modeling, we constructed a pipeline with standard scaler PCA. We then built a Random Forest Regression Model and Gradient Boosting Regressor. From this, we discovered that PCA did not improve our model so we eliminated that moving forward. The best performing model was the Scaled Gradient Boosting. Then we used hyperparameter tuning to improve the Scaled GB.
The hyperparameter (Model 2) tuning improved our Mean Squared Error, R squared, Mean Absolute Error and Bias Error in both the train and test models when comparing to the linear regression results.
The third and final model we built was AutoML. AutoML produced the lowest MSE, the lowest MAE, and lowest Bias error for test. Additionally the AutoML produced the the best R squared for both train and test. Finally, the model had no issues with overfitting. Therefore we chose to move forward with AutoML.
We believe that the AutoML model will provide the best results to identify the zipcodes with the highest future values of mental illnesses.
