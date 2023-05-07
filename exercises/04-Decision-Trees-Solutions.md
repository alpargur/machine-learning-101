# 04 Decision Trees

1. What are the benefits of decision trees?
    - They are east to interpret (whitebox).
    - Requires no data preparation.


2. How does decision trees predict a class? <br> We start with a pair of (feature, threshold). Then the goal is the find the pair with the lowest impurity. <br> This is done via by comparing each pair and the node is splitted based on the pair with lowest impurity. <br> This process continues until we reach to a 100% pure node or a node which doesn't improve if it gets splitted. <br> This node is a leaf node.


3. What does Gini score measure? <br> Gini score measures the impurty.


4. Why are decision trees are called white box? <br> Unlike neural networks, we can observe each step and see the split details of a tree at every step. <br> Whereas a blackbox model gives us a final output and it isn't really intuitive to understand the process in between.


5. How does CART work? <br> It's a greedy algorithm. It is designed to find the lowest impurity among all features at the current point regardless of next split step possibilities and it makes a binary split of data based on that selected feature.


6. What is the overall prediction complexity? <br> _**O(log2(m))**_ <br> This is independent of number of features.


7. What is the overall training complexity? <br> _**O(n × m log(m))**_ <br> Training compares all features on all samples at each node.


8. What is entropy? <br> Entropy is concept of thermodynamics. In its original context it's a measure of molecular disorder. <br> In decision trees it is used as a measure of impurity.


9. Why do we use the _max_depth_ parameter? <br> max_depth restricts the potential reach of a decision tree and it is used for regularization of model.


10. What limitations do decision trees have? <br> They are unstable compared to other predictors. <br> One small change in the data can have a substantial impact on the structure of a decision tree.