## Properties of random variable

For any random variable X, teh following properties hold true

The expectation of a random variable is given by the integral pf teh value of X with its probability density function.
The variance is always non-negative and its square root is called teh standard deviation

## Law of large numbers

The Law of large numbers (LLN) states that if you sample a random variable independently a large number of times, the
measured average value should converge to the random variable's true expectation.
This is important in studying the longer term behaviour of random variables over time. As an example, a coin might land
on heads 5 times in a row, but over a much larger n we would expect teh proportion of heads to be approximately half of
the total flips.
Similarly, a casino might experience a loss on any individual game, but over the long run should see a predictable
profit over time.

## Central Limit theorem

The central limit theorem states that if you repeatedly sample a random variable a large number of times, the
distribution of teh sample mean will approach a normal distribution regardless of the initial distribution of the random
variable.

The CLT provides the basis for much of hypothesis testing, which is discussed shortly. At a very basic level, you can
consider the implications of this theorem on coin flipping. The probability of getting some number of heads flipped over
a large n should be approximately that of a normal distribution. whenever yu are asked to reason about any particular
distribution over a large sample size, you should remember to think of teh CLT, regardless of whether it is Binomial,
Poisson or any other distribution.

### Z- test

Z-test is used when the sample size is large (to invoke the CLT) or when the population variance is known and a t-test
is used when the sample size is small and when the population variance is unknown.

### t- test

The t-test is structured similarly to Z - test but uses the sample variance s square in place of population variance.
The t-test is parametrised by teh degrees of freedom, which refers to teh number of independent observations in a
dataset denoted below by n-1.

### Chi-squared test

This test statistic is used to assess goodness of fit. It takes on a particular number of degrees of freedom, which is
based on the number of categories in teh distribution.

To use the squared test to check whether tw categorical variables are independent, create a table of counts (called a
contingency table), with the values of one variable forming the rows of the table and the values of the other variable
forming its columns, and checks for intersections. 

## p-value
A p-value is the probability of observing the value of the calculated test statistic under the null hypothesis assumptions.