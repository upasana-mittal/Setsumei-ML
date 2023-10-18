# SVM

The hyperplane in the SVM plays the role of the decision boundary. It is used to separate two groups of example from one another. As such, it has to be as far from each group as possible

On the other hand, the hyperplane in linear regression is chosen to be as close to all training examples as possible.

Hyperplane satisfy the following constraints:
- $wx_i - b ⋝ 1$ if $y_i = + 1$ and
- $wx_i - b ⋜ 1$ if $y_i = - 1$ 

We also want to minimize $||w||$ so that the hyperplane was equally distant from the closest examples of each class.

The optimization problem for SVM:

$$
min(1/2)||w||^2
$$

where

$$
y_i(x_iw-b) - 1 ⋝ 0 , i=1,...,N
$$
