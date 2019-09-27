## Housing-Price-Prediction-using-ML-algorithms

This Dataset has been taken from kaggle.com The source of the data set is given as follows: https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data

<ul>
<li>
train.csv - the training set
</li>
<li>
test.csv - the test set
</li>
<li>
In this data set, we need to predict which property has the best SalePrice using different models. We are trying to find which models give the best result.
</li>
</ul>

## Model Summary

We see here that:

<ul>
<li>
In Bagging regressor, both Decision tree and Random Forest regressors over fits the data
</li>
<li>
In Pasting regressor, SVR with linear Kernel underfits the data while Decision Tree overfits the data.
</li>
<li>
In AdaBoost regressor, Decision Tree model over fits the data and SVR model underfits the data
</li>
<li>
In Gradient Boosting Regressor, the model overfits the data
</li>
<li>
Deep Learning model here gives us the best result with 90% train score and 86% test score.
</li>
<li>
Hence our best model so far which has properly fit the data has been Perceptron and MLP

<b>Analysis of RMSE:</b>
The RMSE score for the reduced dataset is somewhat similar than the score of the unreduced dataset(exception – Ridge and Lasso where the RMSE for the unreduced data is more than for the unreduced dataset)We have used 5 PC for our different models. There is not much difference in the scores for the reduced and unreduced data, maybe because we have taken fewer number of Principal Components. We see that our model over fits the data even after using PCA) The above results shows that irrespective of performing PCA on the models, almost all models overfits the data. The Ridge regressor model (without PCA) with 78% train score and 68% test score can be considered as the optimum model here as we can say it somewhat fits the data.

<b>Best Model:</b>
The best feature according to our Ridge regressor has been the LotArea followed by LotFrontage.

<b>Deep Learning:</b>
After performing Ensemble learning and Neural Networks, we see that even Ensemble Learning couldn’t remove the overfitting problem. However, we could see that the Deep Learning model gave 86% test score against 90% train score. Hence, this model had perfectly fit the data.
