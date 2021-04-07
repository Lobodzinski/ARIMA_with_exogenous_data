***Weird aspects of ARIMA - how to increase the accuracy of predictions by exogenous data***      

ARIMA models with exogeneous data are strongly dependent on the factor by which we multiply the exogeneous data. 
Generalizing, we can say that the larger the factor, the smaller the prediction error of the model.   
Available in the folder script **ARIMA_exogenous_data__scaling_property.ipynb**  
presents a practical confirmation and realization of the hypothesis presented on my blog    
https://dataanalyticsforall.blogspot.com/2021/04/weird-aspects-of-arima-how-to-increase.html   

In brief, the Idea of the hypothesis is as follows:
1. use exogenous variables that are highly correlated (α≈1.) or anti-correlated (α≈−1.) with the target is equivalent to a model without exogenous variables (but with changed model parameters).
2. the use of exog data, scaled by the ratio ( exogenous data/target ) allows for a significant modification of the final prediction error of the model. The error is now scaled by the factor 1/1−α. \
So   
a) we have the error explosions for |α|≈1,   
b) for |α|<1: error with exog data > error without exogenous variable,   
c) for |α|>1: error with exog data < error without exogenous variable.
