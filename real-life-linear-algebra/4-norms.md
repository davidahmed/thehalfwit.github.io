---
layout: default
---
{% include mathjax.html %}
{% include subpage-nav.html %}
# Norm and Distances
### Euclidean Norm
Euclidean norm of a vector 
$$\vec{v}=\mathopen{\scriptstyle(}\begin{smallmatrix}a & b & c\end{smallmatrix}\mathclose{\scriptstyle)}$$
is 
$$\sqrt[]{a^2 + b^2 + c^2}$$
### Taxicab Norm
Euclidean norm of a vector 
$$\vec{v}=\mathopen{\scriptstyle(}\begin{smallmatrix}a & b & c\end{smallmatrix}\mathclose{\scriptstyle)}$$
is 
$$|a| + |b| + |c|$$.
### Movie recommendation with vector norms
Imagine a scenario where you want to pair yourself with someone who has a similar movie preferences as you do. How do you solve the problem? Well, norm.    
Now, we can extend the same idea, given a movie, find a similar movie. All we do is to form a vector with each component as rating from a particular user. Now, we
find the closest movie to the given movie. Try playing with different distance norms and see how results are affected.

### Vector norms for reading handwritten numbers
1. Divide the images into training and test set.
2. From the training set, find the average of all the matrices representing different digit images.
3. For every test digit, compare it to all the average digits. The digit with lowest distance is the best predictions. 