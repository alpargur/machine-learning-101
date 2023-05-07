# 4. Decision Trees

## Lecture Notes
- Benefits: 
	- classification, regression, multiclass predictions, 
	- it gives the probability of the classes in percentages
    - they don't require data preparation (feature scaling or centering)
    - they are often called whitebox models in contrast to neural networks or random forests
- Gini Impurity or Entropy?
	- Gini best split (1/2, 1/2)
	- Entropy best split (1/2, 1)
	- They both return the same decision tree but the differences is in the slope of equations.
- **CART algorithm is important for the exam**
- Minimal cost complexity pruning
- One of the limitations of decision trees is that **they are largely unstable compared to other decision predictors**. A small change in the data can result in a major change in the structure of the decision tree, which can convey a different result from what users will get in a normal event.

## Classification and Regression Tree (CART) Algorithm
- Scikit-Learn uses CART algorithm and it produces only binary trees.
- The node split is made based on a single feature and a threshold value.

## How to choose a pair of (feature, threshold)?
- It looks for the purest subsets weighted by their size and selects the pair with the lowest impurity. <br>
- CART is called a _greedy algorithm_. It opts out for a good solution but not possibly the best one. <br>
- Finding the optimal tree is a NP-Complete problem _O(exp(m))_.

## Gini vs. Entropy
- Gini is slightly faster and often chosen as default.
- Gini impurity tends to isolate the most frequent class in its own branch of the tree, while entropy tends to produce slightly more balanced trees.

## Regularization of Decision Trees
- **Regularization:** Avoiding overfitting of a model.
- **Parametric Model:** Degree of freedeom is limited. This can prevent overfitting, nevertheless increases the chance of underfitting.
- **Hyperparameters in Decision Trees:**
  - **max_depth:** tuning max depth helps to prevent overfitting
  - **min_samples_split:** min number of samples a node must have before it can be split
  - **min_samples_leaf:** min number of samples a leaf node must have
  - **min_weight_fraction_leaf:** fraction of total number of weighted instances
  - **max_leaf_nodes:** max number of leaf nodes
  - **max_features:** max number of features allowed to be evaluated for splitting each node
  - In general increasing the _min*_ parameters and decreasing the _max*_ parameters regularize the model.
- **Pruning:** 
  - Other algorithms first train the model without any restrictions and then remove insignificant nodes, so called pruning. <br> A node whose children are all leaf nodes is considered to be insignificant if the purity improvement is negligible.
  - X^2 test is used to estimate the probability aka _p-value_. If this value is higher than selected threshold then node is said to be insignificant.
  - With `ccp_alpha` parameter you can control the use of pruning. The higher the ccp_alpha value, the more batches will be pruned.