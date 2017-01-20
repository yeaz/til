# Normal Equation

## Definition

A method for minizing the cost function without using an iterative algorithm. It minimizes the cost function by taking the derivaties with respect to \theta j's, and setting them to zero.

## Formula

theta = (X^T X)^(-1) X^T y

## Comparison with Gradient Descent
| **Normal Equation** | **Gradient Descent** |
| ------------------- | -------------------- |
| No need to set learning rate | Need to set learning rate |
| No need for iterations       | Need many iterations      |
| Slow if number of features is very large ( > 10000) | Works well when number of features is large |

* Normal Equation works well for linear regression with a relatively small number of features. Otherwise, gradient descent is generally used in practice.

## Noninvertibility

There are cases when X^T X is not invertible. This rarely happens, but it may be caused by two reasons.

1) **Two or more features are redundant or very closely related.**
   For example, when a feature is linearly dependent on another feature.

2) **There are too many features.**
   Delete features or use regularization.