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

1. Variational Dropout and the Local Reparameterization Trick (Diederik P. Kingma et al.)

Dropout can be viewed as a stochastic variational inference of the weights. In this paper, they use local reparameterization trick to replace the global reparameterization (reparameterize on every variable, which is local to every sample, rather than reparameterize on weights, which is global) to reduce the variance of the gradients. Thus achieves better results.

**Can we also use local-reparameterization trick (later reparameterization) in VAE to improve the performance?**

**What is the relationship between variational weight and variational neuron?**

2. Variational Dropout Sparsifies Deep Neural Networks

They use two strategies to improve the variational dropout: 1) Replace the posterior of $w$ from $\mathcal{N}(\theta,\theta\alpha)$ to $\mathcal{N}(\theta,\sigma^2)$; 2) Use a better KL divergence approximation between $p(w)$ and $q(w)$.

The main drawback of the original paper is that $\alpha$ cannot be larger than $1$, which means the dropout rate could only be no larger than $0.5$. In this paper, the dropout rate can be nearly $1$ thus makes the network weight sparse.

3. Bayesian Compression for Deep Learning

Comparing to the previous paper, they further add a group sparsity term to motivate the group sparsity property. In previous paper, all the weights are independant ($p(w_{ij})\propto\log|w_{ij}|$). They use another parameter $z$ to control the group sparsity, thus $p(w_{ij})\sim\mathcal{N}(w_{ij};0,z_i^2)$ and $p(z)$ follows a half-Cauchy distribution: $\mathcal{C}^+(0,s)=2\left(s\pi\left(1+(z/s)^2\right)\right)^{-1}$, where $s$ is also a tunable parameter.

**Can we also add group sparsity to VAE?** 

4. Adversarial Variational Bayes: Unifying Variational Autoencoders and Generative Adversarial Networks

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

Standford course on theories of deep learning: https://www.researchgate.net/project/Theories-of-Deep-Learning