# 5. Ensemble Learning

## Light Gradient Boosting Machine (GBM)

## Histogram Based Decision Tree
- Uses histogram with a bins to find the best split (this is pretty fast compared to ordinary decision tree).
- Number of bins is always smaller than the number instances.
- The residual error: The gradient stored just for each bin

## Gradient-based One-side Sampling (GOSS)
- Keep instances with large gradients (residual error) and remove the smaller ones in each boosting epoch.

## Exclusive Feature Bundling (EFB)
 