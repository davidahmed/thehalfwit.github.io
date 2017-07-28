---
layout: default
---
{% include subpage-nav.html %}
{% include mathjax.html %}

## Eigenvectors
Graphical interpretaion of eigenvectors. (sheer)    
$$ Av = \lambda v \\
   Av - \lambda v = 0 \\
   \left(A - \lambda I \right)v=0
$$    
Can we find such a vector $$v$$, other than the zero vector, that meets the requirement? Yes, if the $$det\left(A-\lambda I\right) = 0$$ is true. Show an example with 2x2 matrix. This should highlight the importance of determinant. With the eigenvalues, we can form a linear system and solve to find the eigenvectors.
### Computing determinants
Lewis Carroll's method

### Clustering nodes in an Undirected graph with eigenanalysis (give example)
1. From the adjacency matrix, find the matrix $$ D $$ which has only a diagonal row and the element in the diagonal is the sum of the row.
2. Find $$ L = D-A$$, which is also a Laplacian Matrix.
3. The vector corresponding to the second smallest eigenvalue is the vector which partions the graph into maximally, and minimally connected graphs.