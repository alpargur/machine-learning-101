# 2. End to end Machine Learning
E2E pipeline is a set of automated steps in order to solve a specific problem. <br>
It handles all steps from retrival of input data, cleaning data, splitting the data, training the model, fine-tuning the model,
evaluating the model, deploying the best one and persisting the output. Rather it be a dataset or something else.

## Before starting an ML project
- Find out the motives behind the task
- Explore existing solutions (they are useful to assess the performance of the model to be developed)
- Frame your problem. Is it (un)supervised learning, classification problem etc.
- Select a performance measuring method (RMSE, MAE)
  - They both measure distance between two vectors.
  - RMSE is more sensitive to outliers than MAE

## Machine Learning Glossary
| Notation          | Meaning                          |
|-------------------|----------------------------------|
| m                 | nr of instances in a dataset     |
| x^i               | vector of i*th* datapoint        |
| y^i               | desired output of i*th* instance |
| X                 | matrix of all instances          |
| h                 | system's prediction function     |
| y_hat^i = h(x_^i) | prediction of a model            |

## Feature Scaling
ML algorithms performs poorly when input numerical values have very different scales. <br> 
In such cases scaling is very useful.
- Normalization $ \frac{n - min}{max -min} $
- Standardization (much less affected by outliers) $ \frac{n - mean}{standard deviation} $
- It is important to fit scaler separate by training and test data set.

## Evaluation with Cross Validation
Cross validation is splitting of training data into smaller chunks to be used as training and validation data before testing the model. <br>
`cross_val_score` splits training data into k-folds and trains it _k_-times using _k-1_ of them for training and 1 set for validation in each round.

## Model Fine-tuning
After getting promising model, we fine tune the selected ones.
- Grid search (unreasonably high computational cost)
- Randomized Search (better)
- Ensemble Approach (combine models performing the best)

## Evaluation on Test Set
**Model must not be fitted during validation!! Do only transformation.**
```shell
$ drop labels from test set (X_test)
$ get labels for validation (y_test)
$ transform(X_test)
$ predict(X_test_transformed)
$ measure_performance(y_test, X_test_predictions)
```

---

### Fitting
Adjusting the parameters to improve the model's accuracy.

### Regression
Is a good choice for prediction problems.
  - **Multiple Regression** uses multiple features to make a prediction.
  - **Univariate Regression** predicts a single value for a single feature.

### SciKit API
  - Estimators
  - Transformers
  - Predictors