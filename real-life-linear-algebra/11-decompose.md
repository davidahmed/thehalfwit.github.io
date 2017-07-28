---
layout: default
---
{% include subpage-nav.html %}
{% include mathjax.html %}

### The Singular Value Decomposition (SVD)
Not very much different from prime factorization of integers, matrices can also be broken up (or decomposed) into a product form. $$LU$$ decomposition is a common decomposition, but here we'll be discussing $$SVD$$. Unlike the former, $$SVD$$ can be found for a matrix of any arbitrary dimension. Performing a $SVD$$ decomposition of any matrix gives us three matrices $$U$$, $$\sigma$$ and $$V$$. $$\sigma$$ and $$V$$ are always square matrices. $$SVD$$ decomposition helps us in getting a good approximation of a matrix.
### Frobenius norm of a matrix
How well a matrix approximation performs can be measured using Frobenius norm. It is simply the square root of sum of all the elements of a matrix.   
$$ D_{F} = \sqrt{\sum_{i=1}^m \sum_{j=1}^1 a_{ij}^2} $$
### Rank-k approximation of a matrix and image compression
Rank of a matrix is the least total number of row vectors that are not linear combinations of each other. To compute a rank-k approximation of a matrix, we calculate $$M_k = U_k \sigma_k V_k$$ where $$\sigma_k$$ is the matrix formed from first $$k$$ rows and columns of matrix $$\sum$$, $$U_k$$ is the first $$k$$ columns of $$U$$, and $$V_k$$ is the first $$k$$ columns of $$V$$.     
We can use the same idea to compress images using an approximation.
### Rank-k approximation to reduce noise
It turns out that we can reduce noise from 'regular' image by applying $$SVD$$ approximation to it.
### Downsampling an image
We can easily downsample images using $$SVD$$. We begin downsampling by clustering the image using $$SVD$$, and applying the colors to the cluster pixels. What's the difference between eigenanalysis clustering and $$SVD$$ clustering? To find the two clusters:
1. Convert the RGB image to a matrix with each row associated with each pixel, and different columns for different color channels.
1.1 Merge the columns based on a metric, say average.
2. Perform $$SVD$$, and cluster the corresponding pixels based on their signs in $$U$$.

How can we achieve multiple clustering?

Instead of using a single column vector, we can use a two column matrix. Perform the decomposition. Cluster the pixels into different groups based on different permutations of the signs of the column.