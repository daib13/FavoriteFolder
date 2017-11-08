# Subspace clustering

## Review

## Conventional method

1. Scalable Sparse Subspace Clustering by Orthogonal Matching Pursuit (Chong You et al.)

Main idea: using orthogonal matching pursuit to find the affinity matrix (much faster)

Prons: beautiful theory, can solver problems with tens of thousands of samples (comparing to several thousand samples in conventional methods)

2. Scalable Sparse Subspace Clustering (Xi Peng et al.)

Not read yet.

## Deep model

1. Deep Sparse Subspace Clustering (Xi Peng et al.)

Main idea: It iteratively updates the weights of the encoder and the affinity matrix C.

Prons: VERY STABLE.

Main drawback: Some features are not updated after pretraining (meaning they are fixed). Still neet to extract feature manually.

(Fast l1-minimization algorithms and an application in robust face recognition: a review (Allen et al.). They use this paper to solve the l1-minimization problem)

2. Deep Subspace Clustering Networks (Pan ji et al.)

Main idea: use a self-express layer to build the affinity map and let the samples to express themselves.

Prons: make use of self-expressiveness in deep neural network.

Main drawback: The energy function is not good. The reconstruction loss can be over-emphasized and it ignores the self-expressive loss part thus makes the performance very poor.

# Variational Autoencoder

1. Variational Dropout and the Local Reparameterization Trick

# Optimization

## Saddle points

1. Gradient Descent Can Take Exponential Time to Escape Saddle Points (Simon S. Du et al.)

2. How to Escape Saddle Points Efficiently (Chi Jin et al.)

3. Gradient Descent Converges to Minimizers (Jason D. Lee et al.)

## L1 minimization

1. Fast L1-Minimization Algorithms and An Application in Robust Face Recognition: A Review

# Measure-Theoretic Probability Theory

A good tutorial: http://www.math.wisc.edu/~roch/grad-prob/index.html

A course:
http://nptel.ac.in/courses/111101005/


# Math Course on Youtube

https://www.youtube.com/channel/UCcAtD_VYwcYwVbTdvArsm7w


# Others

Coulomb GANs: Provably Optimal Nash Equilibria via Potential Fields (Thomas et al.)