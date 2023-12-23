# kNN

k-Nearest Neighbors (kNN) is a non-parametric learning algorithm. Contrary to other
learning algorithms that allow discarding the training data after the model is built, kNN
keeps all training examples in memory. Once a new, previously unseen example x comes in,
the kNN algorithm finds k training examples closest to x and returns the majority label (in
case of classification) or the average label (in case of regression).

The closeness of two points is given by a distance function. For example, Euclidean distance
seen above is frequently used in practice. Another popular choice of the distance function is
the negative cosine similarity. Cosine similarity defined as,

$$
s(x_i,x_k) = cos(∠(x_i,x_k)) = (∑^D_{j=1}x^{(j)}_ix^{(j)}_k)/(√{∑^D_{j=1}(x^{(j)}_i)^2}√{∑^D_{j=1}(x^{(j)}_k)^2})
$$

is a measure of similarity of the directions of two vectors. If the angle between two vectors
is 0 degrees, then two vectors point to the same direction, and cosine similarity is equal to 1.
If the vectors are orthogonal, the cosine similarity is 0. For vectors pointing in opposite
directions, the cosine similarity is ≠1. If we want to use cosine similarity as a distance metric,
we need to multiply it by ≠1. Other popular distance metrics include *Chebychev distance,
Mahalanobis distance, and Hamming distance*. The choice of the distance metric, as well as
the value for k, are the choices the analyst makes before running the algorithm which are also known as hyperparameters.
