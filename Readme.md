# Notes

Note: These are my notes sourced from

- The hundred page machine learning book
- Sklearn python library

Machine Learning is a universally recognised term that usually refers to the science and engineering of building machine
capable of doing various useful things without being explicitly programmed to do so.

- Supervised
- Semi - supervised
- Unsupervised
- Reinforcement

### Supervised Learning

Dataset --> collection of labelled examples

$$
\{ (x_i,y_i) \} ^N_i=1
$$

Each element

$$ x_i $$

among *N* is called a feature vector.

***Feature Vector*** is a vector in which each dimension *j=1,...,D* contains a value that describes the example.
That value is *feature* and denoted as

$$ x^{j} $$

The *goal of the supervised Learning* algorithm is to use the dataset to produce a model that feature vector as input
and outputs information that allows deducing the label for this feature vector.

### Unsupervised Learning

dataset --> collection of unlabelled examples

feature vector

$$
\{x_i\}^N_{i=1}
$$

The *goal of an unsupervised learning* algorithm is to create a model that takes a feature vector as input and either
transforms it into another vector or into a value that can be used to solve a practical problem.

Examples: Clustering, Dimensionality Reduction, Outlier Detection

### Semisupervised Learning

- Build a fine model with labelled data
- Create pseudo labels for unlabelled data
- Build another model that works with both datasets mixed together

### Reinforcement Learning

RL is a subfield of ML where machine lives in an environment capable of perceiving that state of that environment as a
vector of features.
The machine that can execute actions in every state.
Different actions brings different rewards and could also move the machine to another state of environment.
The goal of RL algorithm is to learn a policy.

A policy is a functions that takes the feature vector of a state as an input and outputs an optimal action to execute in
that state.
The action is optimal if it maximizes the expected average reward.

RL solves a particular kind of problem where decision making is sequential and the goal is long term, such as game
playing, robotics & logistics.

### Algorithms

- Linear regression [Click here!](algorithms/Linear%20Regression.md)
- Logistic Regression [Click here!](algorithms/Logistic%20Regression.md)
- Decision tree [Click here!](algorithms/Decision%20Tree.md)
- SVM [Click here!](algorithms/SVM.md)
- kNN [Click Here!](algorithms/kNN.md)

### Building blocks

Each learning algorithm consists of three parts:

- a loss function
- an optimization criterion based on the loss function (cost function)
- an optimization routine that leverages training data to find a solution to the optimization criterion

### Feature Engineering

 - One Hot Encoding: Converting categorical to numerical values
 - Binning: Converting continuous values to bins/ranges as in categorical
 - Normalization: Process if converting an actual range of values which a numerical feature can take, into a standard range of values, typically in the interval [-1,1] or [0,1]
 - Standardization or z-score normalization: Procedure during which the features are rescaled so that they have properties of s standard normal distribution with  mean = 0 and standard deviation = 1

Tips:

- Unsupervised learning algorithms, in practice, more often benefit from standardization than from normalization;
- Standardization is also a feature if the values this feature takes are distributed close to a normal distribution
- Standardization is preferred for a feature if it can sometimes have extremely high or low values(outliers); this is because normalization will squeeze the normal values into a very small range;


#### Confusion Matrix
The confusion matrix is a table hat summarizes how successful the classification model is at predicting examples belonging to various classes. One axis of the confusion matrix is teh label that the model predicted, and the other axis is the actual label.

#### Precision/Recall
Precision is the ratio of correct positive predictions to the overall number of positive predictions. recall is the ratio of correct positive predictions to the overall number of positive examples in the dataset.


## TODOs
- Bias variance trade off
- Model complexity and overfitting
- Regularization
- Cross validation
- Bootstrap and bagging
- Hyperparameter Tuning
- GMM Gaussian Mixture model
- Coding: Space & time complexity, Data Structures, Linked List, Stacks & Queues, Hashmaps, trees, Breadth first & depth first, Algorithms (recursion, greedy, dynamic), sorting (merge & quick)