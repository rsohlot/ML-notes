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
![alt text](pca_formula.gifjpg?raw=true)
	Usually we will get a covariance matrix with a lot of large values.Our ideal would be one
	where all the non-diagonal values are 0. This means that there is no relationship between the
	features. PCA is essentially a transformation of the data to help make this happen.

	Principle components are linear combinations of the original variables.
	