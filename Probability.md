## Conditional Probability

Probability of an event _A_ given that an event _B_ has occurred.
For example, what is the probability of a patient having a particular disease, given that the patient tested positive
for the disease?
This is known as the _conditional probability of A given B_ known as _**Bayes' rule**_

$$
P(A|B) = (P(B|A)P(A))/P(B)
$$

Under Bayes' rule, _P(A)_ is known as prior, _P(B|A)_ as the likelihood, and _P(A|B)_ as the posterior.
As per this rule, A and B have to be dependent on each other. If they are independent then _P(A|B)_ will be _P(A)_.

Similarly, it is possible for _A_ and _B_ to be conditionally independent given the occurrence of another event _C_.

## Law of Total Probability

TODO

## Counting

The concept of counting typically shows up in form or another in most interviews. Some questions may directly ask about
counting (e.g. "How many ways can five people sit around a lunch table?"),
while others may ask a similar question, but as a probability (e.g., "What is the likelihood that I draw four cards pf
the same suit?").

Two forms of counting elements are generally relevant. If the order of selection of the n items being counted k at a
time matters, then the method for counting possible permutations is employed:

$$
n * (n-1) * ... * (n - k + 1) = (n!)/((n-k)!)
$$

In contrast, if order of selection does not matter, then the technique to count possible number of combinations is
relevant:

$$
C(n k) = (n!)/((k!)((n-k)!))
$$

## Random Variables

A random variable is a quantity with an associated probability distribution. It can be either discrete or continuous.

Discrete: Have a countable range
Continuous: Have a uncountable range

The probability distribution associated with a discrete random variable is a _probability mass function (PMF),_
and that associated with a continuous random variable is a _probability density function (PDF)_.

In discrete case, _X_ can take on particular values with a particular probability
In continuous case, probability of a particular x is not measurable; instead a "probability mass" per unit per length
around _x_ can be measured

## Discrete Probability Distribution

The binomial probability distribution gives the probability of k number of successes in n independent trials, where each
trial has probability p of success. Its PMF is

$$
P(X=k) = ℂ(n,k)P^k((1-p)^(n-k))
$$

The most common applications for a binomial distribution are coin flips (the number of heads in n flips), user signups
and any situation involving counting some number of successful events where outcome of each event is binary.

The Poisson Distribution gives the probability of the number of events occurring within a particular fixed interval
where the known, constant rate of each event's occurrence is lambda.
The most common applications for a possession distribution are in assessing const over a continuous interval, such as
the number of visits to a website in a certain periods of time or the number of defects ina square foot of fabric. Thus,
instead of coin flips with probability p of a head as a use case of the binomial distribution, applications of the
Poisson will involve a process X occurring at a rate lambda.
