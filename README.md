# Regularization: Selection, Shrinkage and Valid Intervals

## Objective
I explored how LASSO affects variable selection, coefficient estimates, and confidence intervals.

## Methodology
- I simulated a treatment effect of 1.0 with 100 candidate controls.
- I used LASSO to select controls and then ran OLS.
- I compared this method with double selection.
- I compared LASSO coefficients with their true values and post-LASSO OLS estimates.
- I used five-fold cross-validation to choose lambda, with standardization inside each fold.

## Key Findings
- The original method had a coverage rate of 82.5% across 200 samples.
- Double selection improved coverage to 88.5%, with an average of 26.5 controls.
- LASSO reduced the true coefficients by an average of 4.6%, while post-LASSO OLS brought them closer to their true values.
- My cross-validation results matched GridSearchCV, with a lambda of 0.0501 and a CV MSE of 1.0173.
