# Logistic Regression

Standard Logistic function <===> Sigmoid Function

$$
f(x) = 1/{1+e^{-x}}
$$

*e* is the base of natural logarithm (Euler's number)

Model look like this:

$$
f_{w,b}(x) = 1/{1+e^{-(wx+b)}}
$$

In logistic regression instead of using a squared loss and trying to minimize the empirical risk,
we minimize the likelihood of our training set according to the model.

In statistics, the likelihood function defines how likely the observation is according to our model.

For instance, assume that we have a labelled example

$$
(x_{i}y_{i})
$$

in our training data.

Assume also that we have found some specific values *w* and *b* of our parameters.

If we know apply our model *f* to *x* using the previous equation, we will get some value *0 < p <1* as output.

If y is the positive class then its likelihood of being positive class is given by *p* and for the negative is 1-*p*

The optimization criterion in logistic regression is called maximum likelihood.

Instead of minimizing the average loss in linear regression, we now maximize the likelihood of teh training data
according to our model.

$$
L_{w,b} = ∏_{i=1,..,N}f_{w,b}(x_i)^{y_i}(1-f_{w,b}(x_i))^{(1-y_i)}
$$

because of the exp function used in the model, in practice its more convienient to maximize the log likelihood instead
of likelihood. The log likelihood is defined like follows:

$$
Log L_{w,b} = ln (L_{w,b}(x))
= ∑^N_{i=1}lnf_{w,b}(x) + (i-y_i)ln(1-f_{w,b}(x))
$$

Because *ln* is a strictly increasing function, maximizing this function is same as maximizing its argument, and the
solution to this new optimization problem is the same as the solution to the original problem.


