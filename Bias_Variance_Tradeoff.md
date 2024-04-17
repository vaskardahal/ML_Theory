# Bias-Variance Tradeoff
## Bias
Bias is the measure of the consistent difference between a ML Model's predicted values and the true values.\
We have to be clear that bias is not a measure of the predictive ability of the model or its performance.\
It is more about the systematic errors introduced by the model due to its simplicity or its inability to capture the true relationship between the predictor and predicted variables, such that the model predictions are either constantly underestimated or overestimated.\
How can systematic errors be introduced by a model? Let's consider some examples to take a look at that: 
1. Our objective is to predict real estate property prices (per square unit) using two predictors - size (in area) and location relative to the city. If we build a simple linear model with these two predictors, then our linear model will always be under-predicting the price of the properties closer to the city center. Why is it so? Its logical that an additional square unit area of the property will cost more in the center of the city than outside of it. So, there is clearly an interaction between the location & area that will have a joint effect on the unit price of the property. Since our simple linear regression model failed to take this interaction into account, it will constantly end up under-predicting the price of real estate in the city. 
2. Sales of an item in a store is needed to be predicted. But the training data is collected during a month when the item was on discount. Discounted price potentially means the item's sale will soar up during that period. So, if the model is trained with only the data collected during this discounted period, the model will consistently over-estimate the sales of the item. This consistent over-perdiction leads to bias in the model. 

## Variance
