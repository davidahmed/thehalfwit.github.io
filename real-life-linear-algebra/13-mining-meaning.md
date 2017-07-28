---
layout: default
---
{% include subpage-nav.html %}
{% include mathjax.html %}

## Principal Component Analysis (PCA)
1. Subtract the mean of each row from each element in that row.
2. Rather than using a 900-dimensional vector, we'll use a 50-dimensional approximation of the ratings matrix. It actually turns out that we don't lose much information; even better, we do reduce noise from the dataset.
## Creating 'mathematical genres'
## Connection between PCA and SVD
[StackOverflow link](https://math.stackexchange.com/questions/3869/what-is-the-intuitive-relationship-between-svd-and-pca)
## Applying PCA to facial recognition
Images can be stored as vectors (or matrices). With PCA we may need only 50 or 100 images for a good approximation of 10000 images.
1. The matrix containing the image is first converted into a vector.
2. Calculate the average of the images.
3. Subtract the mean from each image and form a matrix with all the pictures. These images are good only as 'mathematical images'. Call the matrix $$P$$.
4. We are looking for eigenvectors of $$C=P P^T$$. Calculating eigenvectors of $$P$$ and $$C$$ is a very labor intensive task as the number of rows equalled no. of total pixels. But calculating it for $$P^T P$$ is quite simple and the eigenvectors of both the systems are same.
5. We take the vectors corresponding to the highest eigenvalues of C.
6. To test an image- 
* subtract the mean from the test image. 
* Calculate the dot product of the image with each eigenface.
* Take a linear combination of eigenfaces using the dot product result.
* Add the average again to recover the closest looking image.

The magic of all this is that we can reduce a library of 50000 images to 50 images and still perform 'optimally'.
## Using SVD for recommendation systems
Use just few rows of of V from SVD decomposition. What about a new user. Let's call $$U_n$$ the rating of the new user. We can find a similar rating as $$U_n^T U_{sub} \sigma_{sub}^{-1}$$.