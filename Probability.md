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

The _binomial probability distribution_ gives the probability of k number of successes in n independent trials, where
each
trial has probability p of success. Its PMF is

$$
P(X=k) = ℂ(n,k)P^k((1-p)^(n-k))
$$

The most common applications for a binomial distribution are coin flips (the number of heads in n flips), user signups
and any situation involving counting some number of successful events where outcome of each event is binary.

The _Poisson Distribution_ gives the probability of the number of events occurring within a particular fixed interval
where the known, constant rate of each event's occurrence is lambda.
The most common applications for a Poisson distribution are in assessing const over a continuous interval, such as
the number of visits to a website in a certain periods of time or the number of defects ina square foot of fabric. Thus,
instead of coin flips with probability p of a head as a use case of the binomial distribution, applications of the
Poisson will involve a process X occurring at a rate lambda.

## Continuous Probability Distributions

The _uniform distribution_ assumes a constant probability of an _X_ falling between values on the interval a to b.
Its PDF is

$$
f(x)=1/(b-a)
$$

The most applications for a uniform distribution are in sampling random number generation for example and hypothesis
testing cases.

The _exponential distribution_ gives the probability of teh interval length between events of a Poisson process having a
set rate parameter of lambda.
The most common applications for an exponential distribution are in wait times, such as the time until a customer makes
a purchase or the time until a default in credit occurs. One of the distribution's most useful properties, and one that
makes for natural questions, is the property of memory less ness the distribution.

The _normal distribution_ distributes probability according to eh well known bell curve over a range of X's. Many
applications involve the normal distribution, largely due to its natural fit to many real life occurrences, and the
central limit theorem.

## Markov Chains

A _Markov chain_ is a process in which there is a finite set of states, and the probability of being in a particular state
is only dependent on the previous state.
Stated another way, a Markov property is such that, given the current state, the past and future states it will occupy
are conditionally independent.

A _recurrent state_ is one whereby, if entering that state, one will always transition back into that state eventually.
In contrast, a _transient state_ is one in which, if entered, there is a positive probability that upon leaving, one will
never enter that state again.

A _stationary distribution for a Markov chain_ satisfies the following characteristics: _pie = pie*P_,
where _P_ is a transition matrix,a nd remains fixed following any transitions using _P_. Thus _P_ contains the long run
proportions of teh time that a process will spend in any particular state over time.


