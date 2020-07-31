# Dimention Reduction
	* Feature subsetting: ANOVA, LASSO
	* Matrix decompostion techniques: PCA, SVD
	* Manifold learning techniques: tSNE, isomap
	* dimention reduction in the context of a pipeline: models mau vary in terms of their sensitivity to the class imbalance

	The mail goal is to compare and tune different alogorithm available for dimension reduction.


# Feature subsetting
	* AIC/BIC in the context of GLM/GLMMs
	* LASSO regression
	* Neural networks
		1. For labeled data:feature extraction via upper-layer outputs
		2. For labeled or ublabeled data: autoencoders

	* Feature selection:
		1. from sklearn.feature selection import VarianceThreshold
		2. from sklearn.feature selection import SelectKBest
	* Recursive feature elimination


# Principle Component Analysis
	* Latex Formula: Cov(X,Y) = \frac {\sum_{i=1} ^{n} (X_i - \bar{X} ) (Y_i - \bar{Y} )} {n-1}
<!-- ![alt text](pca_formula.gif) -->
<div style="text-align:center"><img src="images/pca_formula.gif" /></div>

	Usually we will get a covariance matrix with a lot of large values.Our ideal would be one
	where all the non-diagonal values are 0. This means that there is no relationship between the
	features. PCA is essentially a transformation of the data to help make this happen.

	Principle components are linear combinations of the original variables.
	

# Other matrix decomposition techniques
	* DictonaryLearning - Dictionary learning
	* FactorAnalysis - Fator Analysis (FA)
	* FastICA - FastICA: a fast algotithm for the Independent Component Analysis.
	* IncrementalPCA - Incremental principal component analysis (IPCA)
	* KernalPCA - Kernal principal component analysis (KPCA)
	* LatentDirichletAllocation - Latent Dirichlet Allocation with online variational Bayes 
	  algorithm.
	* NMF - Non-Negative Matrix Factorization (NMF)
	* SparsePCA - Sparse Principal Components Analysis (SparsePCA)
	* SparseCoder - Sparse coding
	* TruncatedSVD - Dimensionality reduction using truncated Singular Value Decomposition (aka LSA).
	
# Manifold learning:
	Manifold learning algorithms are often used in the context of visualization.
	Principal component analysis and independent component analysis are examples of algorithms
	that define ways to obtain a specific linear projection of the data. These methods have the
	caveat that they do not identify nonlinear structure in the data. Manifold learning is used to
	generalize linear techniques such as PCA to be more sensitive to nonlinear structure in your
	data.  
	* Isomap Isomap Embedding
	* LocallyLinearEmbeddin
	* MDS - Multidimensional scaling
	* SpectralEmbedding - Spectral embedding for non-linear dimensionality reduction.
	* TSNE t-distributed Stochastic Neighbor Embedding.

	t-SNE has a cost function that is not convex. This means that we will not always get the same
	result.It's always highly recommended to use another dimensionality reduction method such as
	PCA for dense data, or truncated SVD for sparse data.To reduce the number of dimensions down
	to a reasonable amount such as 50.
