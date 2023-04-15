# 03 Classification

1. **Is a performance of 90% always a good result for a classification task ? Explain in which situations it is bad.** <br>
It is not enough to assess the performance of our model. We need more insights. Because if we were to only make one prediction in total and this was to be true, then we have 100% performance.

2. Confusion matrix show four things:
    - Number of instances that were positive and predicted true -> TP
    - Number of instances that were positive and predicted false -> FP
    - Number of instances that were negative and predicted true -> TN
    - Number of instances that were negative and predicted false -> FN

3.
| Perfect        | Confusion  | Matrix | ---            |
|----------------|------------|--------|----------------|
| True Negative  | n - n_true | 0      | False Positive |
| False Negative | 0          | n_true | True Positive  |

4. **Precision:** How many of positive identifications were correct TP / TP + FP

5.  **Recall:** Ratio of positive identification to sum of positive and negative identifications TP / TP + FN

6. What does a precision of0.7 2and a recall of 0.75 mean?

7. F1-Score:

8. Precision / Recall trade-off

9. How to determine a good decision threshold

10. What does ROC show?

11. When to use PR curve or ROC curve?

12. Describe the one-versus-the-rest and one-versus-one strategy for multi class
classifiers.

13. What is called a multilabel classification system?

14. What is a multioutput classification (or multioutput-multiclass classification?
