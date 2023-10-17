# PAC Learning
Probably approximately correct learning

PAC theory helps analyze whether and under what conditions a learner *L* with probably output an approximately correct classifier.

Let's define "approximate"

A hypothesis

$$
h \in H
$$

is approximately correct if its error over the distribution of inputs is bounded by some *E* , 0<= *E* <=1/2. i.e. 
$$
error_D(h) < ϵ
$$
where *D* is the distribution over inputs.


Next, "probably", if *L* will output such a classifier with probability
$$
1 - δ
$$

with

$$
0 <= δ <= 1/2,
$$
we call that classifier probably approximately correct.

Knowing that a target concept is PAC learnable allows you to bound the sample size necessary to probably learn an approximately correct classifier, which is whats shown in teh formula you have reproduced:

$$
m ⋝ 1/ϵ(ln|H| + ln(1/δ))
$$

To gain some intuition about this, note the effects on m when you alter variables in the right hand side.

As allowable error decreases, the necessary sample size grows.

Likewise, it grows with the probability of an approximately correct learner and with the size of the hypothesis space *H*

Loosely, a hypothesis space is the set of classifiers your algorithm considers.

More plainly, as you consider more possible classifiers, or desire a lower error or higher probability or correctness, you need data to distinguish between them.
