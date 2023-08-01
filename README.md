# Module-12

## Overview of the Analysis

### The purpose of the analysis provided was to build a model that can identify the creditworthiness of borrowers, using imballanced classes since healthy loans easily outnumber risky loans.

### The data provided was historical lending activity from a peer-to-peer lending services company, which was used as the original data.  


### We were trying to predict if the status of the loan is considered low-risk(0) or high-risk(1) this would be done using `value_counts` to make check on the number of low and high risk selections already set in the dataframe.


### First the data was imported  labeled and classified then split into the training sets and test sets using the `train_test_split` from `sklearn`.
### The first test was run using `LogisticRegression` and the second test was run using `RandomOverSampler`


## Results

* Machine Learning Model 1 LogisticRegression:
  ![model1](Resources/mod12.jpg)



* Machine Learning Model 2 RandomOverSampler:
  ![model2](Resources/mod12.1.jpg)

## Summary
## The `RandomOverSampler` preformed the best with a `0.99` balanced accuracy score, with the `LogisticRegression` model having a `0.95` in balanced accuracy score. While the difference doesn't seem like it would be that different, when it comes to knowing a high-risk vs a low-risk client more accuracy is better.
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
## The `LogisticRegression` model is accurate when the data is even, meaning that the `1's` and `0's` are around the same count, with the data that we had, the `1's` or the high-risk clients were at a very minimum which required a `RandomOverSampler` model to make sure that the `1's` were recognized and learned as they are the priority in this exercise.

## With the data that we obtained, and the general instance of a minimal amount of low-risk clients being available for learning I would reccomend using the `RandomOverSampler` model for the credit risk.