# 03 Classification

1. **Is a performance of 90% always a good result for a classification task ? Explain in which situations it is bad.** <br>
It is not enough to assess the performance of our model. We need more insights. Because if we were to only make one prediction in total and this was to be true, then we have 100% performance.

2. Confusion matrix show four things:
    - Number of instances that were positive and predicted true -> TP
    - Number of instances that were positive and predicted false -> FP
    - Number of instances that were negative and predicted true -> TN
    - Number of instances that were negative and predicted false -> FN

3. Confusion matrix of a perfect classifier would look like:


| Perfect        | Confusion  | Matrix | ---            |
|----------------|------------|--------|----------------|
| True Negative  | n - n_true | 0      | False Positive |
| False Negative | 0          | n_true | True Positive  |


|           |     | Predictions | Predictions |
| ---       | --- | --- | --- |
|           |     | Dog | Cat |
| Actual | Dog | TN | FP |
| Actual | Cat | FN | TP |


4. **Precision:** How many of positive identifications were correct TP / TP + FP


5. **Recall:** Ratio of positive identification to sum of positive and negative identifications TP / TP + FN


6. What does a precision of 0.72 and a recall of 0.75 mean? <br> 0.72 % of predicted values were right and 0.75 % of actual values were predicted.


7. **F1-Score:** <br> The F1 score favors classifiers that have similar precision and recall. This is not always what you want: in some contexts you mostly care about precision, and in other contexts you really care about recall. For example, if you trained a classifier to detect videos that are safe for kids, you would probably prefer a classifier that rejects many good videos (low recall) but keeps only safe ones (high precision), rather than a classifier that has a much higher recall but lets a few really bad videos show up in your product


8. **Precision / Recall trade-off:** <br> Increasing threshold for decision function would increase the precision but decrease the recall rate and vice versa.


9. How to determine a good decision threshold? <br> This mostly depends on what we are aiming for. Since there is an obvious trade-off between precision and recall, it is reasonable to set a threshold which favors what we prioritize. To find a sweet spot we can use `precision_recall_curve` or plot precision vs recall.


10. What does ROC show? <br> Receiver operator characteristics (ROC) is a common tool for binary classifiers. It plots the _true positive rate (recall)_ vs. _false positive rate_ in another words "ratio of negative instances classified as positive". <br> It's equal to $1- TNR$ (ratio of negative instances correctly classified as negative -> **specificty**) <br> So ROC represents -> **_sensitivity (recall) vs. 1 - specificty_**.


11. When to use PR curve or ROC curve? <br> Generally ROC curves should be used when there are roughly equal numbers of observations for each class. Precision-Recall curves should be used when there is a moderate to large class imbalance.


12. Describe the one-versus-the-rest and one-versus-one strategy for multiclass classifiers.
    - **One-vs-Rest:** Train model for each class category against the rest of the set. n models for n classes
    - **One-vs-One:** Train each model against each other using every possible combination. n(n-1) / 2 models for n classes.


13. **Multilabel Classifier:** Systems output multiple binary tags. For example: <br> Face-recognition system identifying many faces in a picture.


14. **Multioutput Classifier:** It is a multilabel classification system where each label can be multiclass. For example: <br> An object classifier which tell the shape and color given a picture. The set of classes may look something like:

```json
{
   "shape": ["cirle", "rectanlge", "triangle", "square"],
   "color": ["red", "green", "blue"]
}
```

---

## Addendum
### - If we revert the labels of 1, 0 (_e.g._ classify negatives instead of positives) than the accuracy stays the same but the precision and recall values change.
### - ROC curve doesn't exist for every estimator.
### - Use confusion matrix for determining the misclassifications of a multiclass classifier model.