## Test
|Name |Description | Code|
|----------|-----|--------|
|UMAP|Uniform Manifold Approximation and Projection is used for dimensionality reduction.<br>Pros: High performance, preserves global structure. <br> Cons: Sensitive to parameters. <br> Applications: Data visualization, feature extraction. <br> Key hyperparameters: <br> n_neighbors: Controls the local neighborhood size default = 15. <br> min_dist: Controls the minimum distance between points in the embedded space default = 0.1. <br> n_components: The dimensionality of the embedding default = 2.|from umap.umap_ import UMAP<br>umap = UMAP(n_neighbors=15, min_dist=0.1, n_components=2) |
