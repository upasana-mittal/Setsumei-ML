# Gradient Descent

_Gradient descent or stochastic gradient descent_ are two most frequently used optimization
algorithms used in cases where the optimization criterion is differentiable.
Gradient descent is an iterative optimization algorithm for finding the minimum of a function.
To find a local minimum of a function using gradient descent, one starts at some random
point and takes steps proportional to the negative of the gradient (or approximate gradient)
of the function at the current point.
Gradient descent can be used to find optimal parameters for linear and logistic regression,
SVM and also neural networks which we consider later. For many models, such as logistic
regression or SVM, the optimization criterion is convex. Convex functions have only one
minimum, which is global. Optimization criteria for neural networks are not convex, but in
practice even finding a local minimum suffices.

- Learning rate controls the size of an update
- One pass through all the training examples is called an epoch

Remember that the Linear Regression model looks like this

$$
f(x) = wx+b
$$

We dont know what the optimal values for *w* and *b* are and we want to learn from them from data. To do that, we looks
for such values for *w* and *b* that minimize the mean squared error:

$$
l = 1/N (∑_(i=1)^N(y_i-(wx_i+b))²)
$$

Gradient descent starts with calculating the partial derivative for every parameter:

$$
𝜕l/𝜕w = 1/N (∑_(i=1)^N(-2x_i(y_i-(wx_i+b))))
$$

$$
𝜕l/𝜕b = 1/N (∑_(i=1)^N(-2(y_i-(wx_i+b))))
$$

```python
def update_w_and_b(spendings, sales, w, b, alpha):
    dl_dw = 0
    dl_db = 0
    N = len(spendings)
    for i in range(N):
        """ Below functions are patial functions which we use to update the partial values"""
        dl_dw += -2 * spendings[i] * (sales[i] - (w * spendings[i] + b))
        dl_db += -2 * (sales[i] - (w * spendings[i] + b))

    # update w and b
    w = w - (1 / float(N)) * dl_dw * alpha
    b = b - (1 / float(N)) * dl_db * alpha
    return w, b
```

The function that loops over multiple epochs is shown below:

```python
def train(spendings, sales, w, b, alpha, epochs):
    for e in range(epochs):
        w, b = update_w_and_b(spendings, sales, w, b, alpha)

        # log the progress
        if e % 400 == 0:
            print("epoch: ", e, "loss: ", avg_loss(spendings, sales, w, b))
    return w, b


def avg_loss(spendings, sales, w, b):
    N = len(spendings)
    total_error = 0.0
    for i in range(N):
        total_error += (sales[i] - (w*spendings[i]+b))**2
    return total_error/float(N)
```
