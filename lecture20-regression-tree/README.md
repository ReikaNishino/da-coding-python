# Lecture 20: Prediction with regression trees (CART)

## Motivation

You want to predict the price of used cars as a function of their age and other features. You want to specify a model that includes the most important interactions and nonlinearities of those features, but you don’t know how to start. In particular, you are worried that you can’t start with a very complex regression model and use LASSO or some other method to simplify it because there are way too many potential interactions. Is there an alternative approach to regression that includes the most important interactions without you having to specify them?

To carry out the prediction of used car prices, we show how to use the regression tree, an alternative to linear regressions that are designed to build a model with the most important interactions and nonlinearities for a prediction. However, the regression tree you build appears to overfit your original data. How can you build a regression tree model that is less prone to overfitting the original data and can thus give a better prediction in the live data?


## This lecture

This lecture introduces the regression tree, an alternative to linear regression for prediction purposes that can find the most important predictor variables and their interactions and can approximate any functional form automatically. Regression trees split the data into small bins (subsamples) by the value of the x variables. For a quantitative y, they use the average y value in those small sets to predict y. We introduce the regression tree model and the most widely used algorithm to build a regression tree model. Somewhat confusingly, both the model and the algorithm are called CART (for classification and regression trees), but we reserve this name for the algorithm. We show that a regression tree is an intuitively appealing method to model nonlinearities and interactions among the x variables, but it is rarely used for prediction in itself because it is prone to overfit the original data. Instead, the regression tree forms the basic element of very powerful prediction methods that we’ll cover in the next seminar.

Case study:
  - [Chapter 15, A: Predicting used car value with regression trees](https://gabors-data-analysis.com/casestudies/#ch15a-predicting-used-car-value-with-regression-trees)

## Learning outcomes
After successfully completing [`02_usedcars_cart_prediction.ipynb`](https://github.com/gabors-data-analysis/da-coding-python/blob/main/lecture20-regression-tree/02_usedcars_cart_prediction.ipynb), students should be able:

  - Understand the how regression tree works
  - Estimate a regression tree
  - Visualize regression tree
  - Set stopping criteria for CART
    - Depth or level of the tree
    - Number of leaves
    - minimum fit measure increase by a split
  - Pruning a large tree
    - find optimal complexity parameter (also known as pruning parameter)
  - Variable importance plot
    - Simple
    - Permutation importance
  - Prediction evaluation
    - comparing trees
    - comparing tree vs linear regressions

## Dataset used

  - [used-cars](https://gabors-data-analysis.com/datasets/#used-cars)

## Lecture Time

Ideal overall time: **100 mins**.


## Further material

  - This lecture is a modified version of [`ch15-used-cars-cart.ipynb`](https://github.com/gabors-data-analysis/da_case_studies/blob/master/ch15-used-cars-cart/ch15-used-cars-cart.ipynb) from [Gabor's case study repository](https://github.com/gabors-data-analysis/da_case_studies).

