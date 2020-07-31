 * Unsupervised learning deals with the discovery of patterns derived from the feature matrix itself. 


 * The domain of unsupervised learning has many families of models. Clustering analysis is one of the main subject areas of unsupervised learning and it is used to partition the observations in a feature matrix into groups in a way that minimizes pairwise dissimilarities.
* Clustering algorithms are generally described as belonging to one of the following categories; combinatorial algorithms, mixture modeling, and mode seeking.

* One issue with many commonly used clustering algorithms is the need to estimate the optimal number of clusters usually represented with the parameter K. There are other modern techniques such as silhouette scores to help.

* Some methods do not suffer from the problems like the Dirichlet Process Mixture Model. These methods have a variety of business applications.



* Unsupervised learning techniques may be useful in all phases of the design thinking process. Since they are essentially designed for summarizing and clustering data sources, they can be helpful in a wide variety of different ways.

During each of the design thinking stages, unsupervised learning techniques may be used to identify patterns in large data sets, which may then be useful in generating new ideas or in making prediction


## An Overview of Unsupervised Learning:

Machine learning algorithms that are built to predict a target or response value (either real-valued or categorical) fall under the heading of supervised learning and include Linear and Logistic Regression, k-Nearest Neighbors, Support Vector Machines, Decision Tree-based models, and Neural Networks. Since all these tools require a well-defined y-value to predict, they can only be used with a relatively small set of data science problems.

With unsupervised learning problems, we begin with a dataset that does not have this target value. In this case, our goals will usually be related to simplifying or summarizing the data. Since we lack a dimension or variable that has the special status of being the target, we can’t really talk about how well our model is doing as clearly as is possible with supervised models. We are not able to do cross-validation, so at some level choosing what’s “good enough” will always be a judgment call in unsupervised learning. That said, it can be very useful to build a “big picture” representation of a dataset using unsupervised learning.


## Clustering:

One of the most prominent domains among unsupervised learning models are those that use clustering techniques. These models attempt to build a simplified picture of a dataset by grouping together similar observations and distinguishing these from observations that fall into other groups. A common use case for this approach is in Market Segmentation, where one uses demographic and/or past purchase data to group consumers together. This process can be helpful for identifying the characteristics of a company’s consumers, for the purpose of designing targeted advertising or promotions likely to appeal to those customers.

There are a large number of clustering algorithms used by data scientists working in various niches. Here we provide brief descriptions of a few of the most broadly applicable ones, starting with two classical combinatorial algorithms: k-Means and Hierarchical clustering. All methods of clustering apply some measure of similarity between observations to group them together, and these two take a geometric perspective by treating observations as points in space and measuring the distances between them. This approach has some drawbacks, which some more contemporary algorithms attempt to address via ranking systems and/or transformations of the data. We introduce two of these: Spectral Clustering and Affinity Propagation. An additional way of grouping data is to do so probabilistically, that is to assume that the data are drawn from a finite number of population distributions and to try to characterize these underlying distributions. Techniques of this form are referred to as Mixture Models, and are our final clustering topic.


## Clustering Evaluation:

There are a large number of clustering performance evaluation tools available. If the labels of the clusters are known then there are metrics like the [adjusted Rand index](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.adjusted_rand_score.html#sklearn.metrics.adjusted_rand_score) and the [Normalized mutual information score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.normalized_mutual_info_score.html#sklearn.metrics.normalized_mutual_info_score). When the labels for the clusters are not known the [silhouette score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.silhouette_score.html#sklearn.metrics.silhouette_score) and [Davis-Bouldin](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.davies_bouldin_score.html#sklearn.metrics.davies_bouldin_score) may be used. To see other methods, look to [scikit-learn’s cluster evaluation page](https://scikit-learn.org/stable/modules/clustering.html#clustering-evaluation). We use silhouette scores in these materials because the numerical range is intuitive.

	-1 - indicates incorrect clustering
    0 - highly overlapping clusters
    1 - dense well-separated clusters

Historically the concept of inertia or the within cluster sum-of-squares has been used for model selection. Generally, it is discussed in the the context of the k-means algorithm, but the metric has a number of drawbacks as far as model selection. Inertia makes the assumption that clusters are convex and isotropic. More importantly though it is not a normalized [metric](https://en.wikipedia.org/wiki/Metric_(mathematics)). We recommend any of the methods provided by [scikit-learn metrics submodule](https://scikit-learn.org/stable/modules/classes.html#module-sklearn.metrics). Another method that is often discussed in the same context as inertia is the [elbow method](https://en.wikipedia.org/wiki/Elbow_method_(clustering)) as a heuristic for determining the number of clusters. These same type of plots can be drawn with other metrics, but they are subjective and can be unreliable.

Important: When thinking about the appropriate number of clusters it is possible that there is more than one answer depending on the perspective. If we clustered visible light on planet earth at night in euclidean space then there would be valid cluster assignments at the continent level, at the country level and at the city level. Keeping this in mind can help ensure you model pipelines are flexible. It can help to think about clusters labels as a probabilistic assignment rather than a hard label.

When comparing across algorithms it is important that the comparisons be between results that contain roughly the same number of clusters. While not definitive, there have been some hints with the running wholesale example that an appropriate number of clusters is around five. For several of the algorithms discussed we can set this value directly. Another alternative is trying to visualize the data using the dimension reduction techniques. The labels designated with colors can provide insight into the cluster assignments. This technique is generally appropriate for the EDA part of the workflow. 