# Decision Tree
A decision tree is an acrylic graph that can be used to make decisions.

In each branding node of the graph, a specific feature *j* of the feature vector is examined.
If the value of the feature is below a specific threshold, then the left branch is followed.

Otherwise, the right branch is followed.

As the leaf node is reached, the decision is made about the class to which the example belongs.

ID3 ==> Formulation of the decision tree learning algorithms

The optimization criterion, in this case is average log likelihood:

$$
1/N ∑^N_{i=1}f_{i}lnf_{ID3}(x_{i}) + (1-y_i)ln(1-f_{ID3}(x_{i}))
$$

where *f* of *ID3* is decision tree

Logistic regression is a parametric model *f* of *wb* by finding optimal solution to the optimization criterion.

The ID3 algorithm optimizes it approximately by constructing a non-parametric model

$$
f_{ID3}(x) = Pr(y=1/x)
$$

In ID3, the goodness of a split is estimated by using the criterion called entropy.

Entropy is a measure of uncertainty about a random variable. It reaches its maximum when all values of the random values are equiprobable.
Entropy reaches it minimum value when the random variable can have only one value.

The entropy of a set of example *S* is given by:

$$
H(S) = -f^S_{ID3}lnf^S_{ID3} - (1 - f^S_{ID3})ln(1-f^S_{ID3})
$$

The algorithm stops at a leaf node in any of the below situations:
- All examples in the leaf node are classified correctly by one peice model
- We cannot find an attribute to split open
- The split reduces the entropy less than *E*
- The tree reaches its maximum depth *d*

Because in *ID3*, the decision to split the dataset on each iteration is local (doesn't depend on future split) the algorithm does not guarantee an optimal solution.

The model can be improved by using techniques like backtracking during the search for the optimal decision tree at the cost of possibly taking longer to build a model.

The netropy based split criterion intuitively  makes sense: entropy reaches its minimum of *O* when all examples in *S* have the same level; on the other hand, the entropy is
at its maximum of 1 when exactly one half of examples in *S* is labelled with 1, making such a leaf useless for classification.

