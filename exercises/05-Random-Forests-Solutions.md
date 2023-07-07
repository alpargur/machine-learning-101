# 05 Random Forest

1. What's the idea behind ensemble learning? Explain it. <br> Using multiple models to get a better result.

2. hard voting vs soft voting classifier? <br>
    - **Hard Voting:** Mode of base classifiers' predictions.
    - **Soft Voting:** Ensembles average predicted probabilities.


3. What can improve ensemble's accuracy? <br> If we **build and combine multiple models**, the overall accuracy could get boosted. <br> The combination can be implemented by aggregating the output from each model with two objectives: reducing the model error and maintaining its generalization.


4. bagging vs pasting <br>
    - **Bagging:** using same training set for every predictor but train them on different random subsets of the training set. Sampling is performed with replacement -> bootstrap aggregation aka bagging.
    - **Pasting:** sampling is performed without replacement.


5. **Out-of-the-bag Evaluation:** OOB evaluation treats the training set as if it were on the test set of a cross-validation.


6. Is it beneficial to have higher randomness in a forest? <br> **Random forest adds additional randomness to the model, while growing the trees**. Instead of searching for the most important feature while splitting a node, **it searches for the best feature among a random subset of features**. This results in a wide diversity that generally results in a better model.


7. What other ways exists to bring randomness into ensemble rather than varying subsets handled for each model? <br> 


8. **Boosting:** <br> gives more weight to the feature with higher error in the next epoch than ones with lower error.


9. **ADABoost:** <br> One way for a new predictor to correct its predecessor is to pay a bit more attention to the training instances that the predecessor underfitted. This results in new predictors focusing more and more on the hard cases. This is the technique used by AdaBoost. <br>
For example, to build an AdaBoost classifier, a first base classifier (such as a Decision Tree) is trained and used to make predictions on the training set. The relative weight of misclassified training instances is then increased. A second classifier is trained using the updated weights and again it makes predictions on the training set, weights are updated, and so on.


10. **Stacking:** <br> Instead of using trivial functions (such as hard voting) to aggregate the predictions of all predictors in an ensemble, why don’t we train a model to perform this aggregation? <br> Final predictor (blender) tales the predictions of ensemble system and makes a final prediction.

## Onsite Questions
- How we build a random forest? -> set of different decision trees
- Why are the trees of a random forest is different from each other? How is the randomness introduced?
- 2 most important hyper params of random forest classifier? -> nr of decision trees and the depth of the tree
- How an extra tree works?
- How is the importance of the features measured with the variable `features_importance_` of the RFC? -> calculated by weighted average
