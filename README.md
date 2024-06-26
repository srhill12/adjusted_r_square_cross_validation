# Adjusted R2 and Cross Validation

## Introduction

Using the encoded car data, I will use r-squared and adjusted r-squared to evaluate two different linear regressions. The first will be trained using 10 features. After removing the "num-of-doors" column, the second model will only be trained on nine features.

After evaluating the models, I will use cross-validation to gain insight into the potential real world performance of the more promising model.

## Steps

1. Create two linear regression models: `lr1` and `lr2`.

2. Fit `lr1` using the `X_one_col_train` and `y_train data`.

3. Fit `lr2` using the `X_multi_col_train` and `y_train data`.

4. Store the predictions made by passing `X_one_col_test` to the predict method of `lr1`.

5. In a separate variable, store the predictions made by passing `X_multi_col_test` to the predict method of `lr2`.

6. Score both models using the Mean Squared Error and r-squared scores. Print all scores with text to provide names and context.

    * Which model performed better according to the r-squared value?

7. Calculate the adjusted r-squared value for `lr1` by passing `X_one_col_test`, `y_test`, and `lr1` to the `r2_adj` function.

8. Calculate the adjusted r-squared value for `lr2` by passing `X_multi_col_test`, `y_test`, and `lr2` to the `r2_adj` function.

    * Which model performed better according to the adjusted r-squared value?

9. Perform cross validation using the `cross_val_score` function along with a new linear regression model, `X_one_col_train`, and `y_train`. Specify "r2" as the scoring metric.


## Reference

Schlimmer, J. 1987. *Automobile* [Dataset]. UCI Machine Learning Repository. Available: https://archive.ics.uci.edu/dataset/10/automobile [2023, August 17]. ([CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/legalcode))
