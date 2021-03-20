# XGBoost

XGBoost is an optimized distributed gradient boosting library designed to be highly efficient, flexible and portable.Bagging and Boosting are 2 main types of decision tree ensemble.
# XGBoost properties:
 1. XGBoost is working with numerical vectors, so all object data should be transformed (as option- One-Hot_Encoder:output- new columns with feature name and binary 0/1 value - availabiity of given feature)
 2. XGBoost doesnt suffer from colinear features, however it is a good practice to drop them.

# Boosting and Bagging
Bagging is an acronym for 'Bootstrap Aggregation' and is used to decrease the variance in the prediction model.In Bagging we combine predictors from multiple-decision trees through a majority voting mechanism. Bagging generates additional data for training from the dataset. This is achieved by random sampling with replacement from the original dataset. 

Boosting is a sequential ensemble method that iteratively adjusts the weight of observation as per the last classification. If an observation is incorrectly classified, it increases the weight of that observation Examples of boosting are Ada Boost where the algorithm first trains a base classifier and uses it to make prediction on the training set. 
The algorithm then increases the relative weight of the miscalassified  training instances, then train the second classifier using the updated weights and again make prediction on the training set. It stops after the specified level or no error is seen in the next stage.

# Special case of boosting:
A spesial case of Boosting in which the error is minimized is Gradient Descent Algorithm (GDA-optimization algorithm)-in case of recruitment process- the least qualified candidates are eliminated as early as possible.
Here the initial tree is trained and the error from the inital trees is again modeled using another predictor this way sequential error training is done to get the complete result.

# XGBoost and Gradent Boosting method:
XGBoost stands for Extreme Gradient Boosting; it is a specific implementation of the Gradient Boosting method which uses more accurate approximations to find the best tree model. It employs a number of nifty tricks that make it exceptionally successful, particularly with structured data. The most important are

1.) computing second-order gradients, i.e. second partial derivatives of the loss function (similar to Newton's method), which provides more information about the direction of gradients and how to get to the minimum of our loss function. While regular gradient boosting uses the loss function of our base model (e.g. decision tree) as a proxy for minimizing the error of the overall model, XGBoost uses the 2nd order derivative as an approximation.

2.) And advanced regularization, which improves model generalization.

XGBoost has additional advantages: training is very fast and can be parallelized / distributed across clusters.


