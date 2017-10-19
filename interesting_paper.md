# Subspace clustering

## Review


## Conventional method
1. Scalable Sparse Subspace Clustering by Orthogonal Matching Pursuit (Chong You et al.)
Main idea: using orthogonal matching pursuit to find the affinity matrix (much faster)
Prons: beautiful theory, can solver problems with tens of thousands of samples (comparing to several thousand samples in conventional methods)

2. Scalable Sparse Subspace Clustering (Xi Pent et al.)
Not read yet.

## Deep model
1. Deep Sparse Subspace Clustering (Xi Peng et al.)
Main idea: It iteratively updates the weights of the encoder and the affinity matrix C.
Prons: VERY STABLE.
Main drawback: Some features are not updated after pretraining (meaning they are fixed). Still neet to extract feature manually.
(Fast l1-minimization algorithms and an application in robust face recognition: a review (Allen et al.). They use this paper to solve the l1-minimization problem)

# Variational Autoencoder


# Others
Coulomb GANs: Provably Optimal Nash Equilibria via Potential Fields (Thomas et al.)