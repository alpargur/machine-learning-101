# 07 - Unsupervised Learning
1. Major benefit of unsupervised learning?
2. 2
3. 3
4. 4
5. Hard vs. Soft Clustering
   Hard clustering is method to grouping the data items such that each item is only assigned to one cluster, K-Means is one of them. While Soft clustering is method to grouping the data items such that an item can exist in multiple clusters, Fuzzy C-Means (FCM) is an example. Soft clustering provides predictions about which class an instance might be belong to

6. Describe K-Means Algorithm
   - Select centroids from available instances
   - It ends when the clusters doesn't change or we can also define a max iteration value for the algo.

`inertia` this is the mean squared distance between each instance and its closest centroid


K-means -> Distance-based cluster analysis
	- can't perform well with rounded data tracks
DBSCAN -> Density-based cluster analysis
	- clusters of any shape can be recognized
	- has no centroid
	- computational complexity
	- it can be harder to cluster if density varies significantly across the clusters
	- no specification of cluster centers
	- it gets complicated for high-dimensional problems