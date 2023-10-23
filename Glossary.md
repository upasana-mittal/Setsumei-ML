# Terms & Definitions

- A **vector** is an ordered list of scalar values called attributes.
- A **set** is an unordered collection of unique elements.

#### Product of elements in a collection

$$
∏
$$

#### Sum of elements in a collection

$$
∑
$$

#### Cardinal of |S| / number of elements in set S

$$
|S|
$$

- sum or difference or product of vector & scalar will be a vector
- dot product of vectors is scalar
- product is done by multiplying row of first matrix * column of second matrix


- *f(x)* has a local minimum if *f(x)* ⋜ *f(c)* for every *x* around an open interval around *c*, *x = c*
- The minimum value among all the local minima is called the global minimum
- A **gradient** of a function is a vector of partial derivatives.
- Partial derivative of a function as the process of finding derivative of focusing on one of the function's inputs and
  by considering all other inputs as constant values.

$$
f(x,y) = ax + by + c
$$

**Gradient** of a function is

$$
⊽f = [𝜕f/𝜕x, 𝜕f/𝜕y]
$$

- The *list of probabilities* is called **probability mass function (pmf)**
- The probability distribution of a continuous random variable (a continuous probability distribution) is described by
  a **probability density function (pdf)**
- The **pdf** is a function whose codomain is non-negative and the area under the curve is equal to 1

## Bayes Rule / Bayes Theorem

$$
Pr(X=x/Y=y) = Pr(Y=y/X=x)Pr(X=x) / Pr(Y=y)
$$

**Principle of maximum likelihood**

##TODO correct this equation

$$
θ^* = arg max_θ ∏^N_(i=1) Pr(θ = θ^^ / X=x_i)
$$

If the set of possible values for theta is not finite, then we need to optimize the above equation directly using a
numerical optimization routine such as gradient descent.

Usually, we optimize the natural logarithm of the right hand side expressions because the logarithm of a product becomes
the sum of logarithms and easier for the machine to work with sum than the product

- All the model based learning algorithms have a loss function and what we do to find the best model is we try to
  minimize the objective known as **cost function**.
- In linear regression, the cost function is given by the average loss also called the **empirical risk**.
