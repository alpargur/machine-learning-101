# 06 Regression
1. How to train a linear regression model? Which method provides the best outcome?
   - Closed form
   - Iterative approach (gradient descent)
   - They both work fine

2. How to measure model's performance?
    - RMSE, MSE

3. What is computationally more expensive when using closed form calculation? Doubling number of features or instances?
   - Doubling number of features: Quadratic
   - Doubling number of instances: Linear

4. How does polynomial regression works?
   - It calculates the power of each feature and extends the dataset by addition the new calculated features.
   - It has a degree parameter, which sort of determines the number of combinations of features' powers.

5. Describe the difference between a decision tree classifier and regressor.
   - Classifier: Using prediction value it makes a discrete prediction
   - Regressor: It predicts a value

6. What kind of functions can a decision tree regressor approximate well?
   - ALL KINDS OF FUNCTIONS

7. What is the plot of the function of a decision tree regressor for one input variable?
   - It's a step function with different steps and size.

8. Is there a random forest regressor or can you just use the gradient tree boosting regressor for the regression?
   - There exists a general random forest regressor, thought it is not mentioned in the book.

9. How does the gradient tree boosting regressor work? 
   - It fits a new predictor to the residuals of the first tree and so on.

10. Summarize steps of gradient descent:
    - For each instance:
      - initialize a random set of parameters
      - calculate gradient of error function (compute the direction of the steepest slope)
      - move towards the point (the steepest slope direction) minimizing the error function
      - stop cycle if gradient converges | no more minimizes

11. What can be a problem when setting the learning rate too high or low?
    - Too high: we may end up at a bigger error function value by jumping over the optimal point
    - Too low: gradient calculation takes too longs or stuck at a local minima

12. What is a problem with _batch gradient descent_?
    - It goes every single instance in the training dataset.

13. What is a problem with _stochastic gradient descent_?
   - It doesn't reach to the global minimum. Result is good but not optimal.

14. What is the intuition behind the _learning schedule_?
    - Slowing down the step size response / learning rate

15. What is the intuition behind the _mini-batch gradient descent_?
   - It's a mesh of BGD & SGD. It neither iterates over all instances or only one random instance. So by iterating over a subset of random instances. it still has the potential to reach to the global minimum. 

16. How can you tell from the learning curves if a model underfits or overfits?
   - Overfit: Training Loss < Validation Loss
   - Underfit: Plateau, not getting better

17. How does early stopping work?
   - We start with a large number of iterations for gradient operation.
   - If the gradient doesn't improve in respect to the tolerance value, searching for gradient stops.
   - Continue with the next instance.
