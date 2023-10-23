# SVM

The hyperplane in the SVM plays the role of the decision boundary. It is used to separate two groups of example from one
another. As such, it has to be as far from each group as possible

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

### Dealing with Noise

To extend SVM To cases in which the data is not linearly sepearbel, we introduce the hinge loss function:

$$
max(0,1-y_{i}(wx_{i}-b))
$$

Hinge loss function is zero if teh constraints of hyperplane are satisfied, in other words, if $wx_{i}$ lies on te
correct side of the decision boundary.
For data on the wrong side of the decision boundary, teh function's value is proportional to the distance from the
decision boundary.

We then wish to minimize the following cost function:

$$
C||w||^2 + 1/N ∑^N_{i=1}max(0,1-y_i(wx_i-b))
$$

where the hyperparameter *C* determines the tradeoff between increasing the size of the decision boundary and ensuring
that each $x_i$ lies on the correct side of the decision boundary. The value of *C* is usually chosen experimentally,
just like *ID3's* hyperparameters $ϵ$ and *d*.

SVMs that optimize hinge loss are called *soft-margin* SVMs, which the original formulation is referred to as a *hard
margin* SVM

As you can see, for sufficiently high values of C, the second term in the cost function will
become negligible, so the SVM algorithm will try to find the highest margin by completely
ignoring misclassification. As we decrease the value of C, making classification errors is
becoming more costly, so the SVM algorithm will try to make fewer mistakes by sacrificing
the margin size. As we have already discussed, a larger margin is better for generalization.
Therefore, C regulates the tradeoff between classifying the training data well (minimizing
empirical risk) and classifying future examples well (generalization)

