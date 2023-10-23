# Linear regression

$$
f_{w,b}(x) = wx + b
$$

- *w* is *D* dimensional vector of parameters
- *b* is real number
- The notation *f* means that the model *f* is parametrized by two values: *w* and *b*

The optimization process that we use to find the optimal values for *w* and *b* tries to minimize the following
expression:

$$
1/N∑_{i=1,..,N}(f_{w,b}(x_{i}-y_{i}))^2
$$

The expression we minimize or maximize is called an *objective function*.

The expression

$$
(f(x_i)-y_i)^2
$$

in the above objective is called the *loss function*. It's a measure of penalty for misclassification of example *i*

This particular choice of the loss function is called the *squared error loss*.

#### Note

All the model based learning algorithms have a loss function and what we do to find the best model is we try to minimize
the objective known as **cost function**.

In linear regression, the cost function is given by the average loss also called the **empirical risk**.

The average loss or empirical loss for a model is the average of the penalties obtained by applying the model to the
training data.

Linear models rarely overfit!!


