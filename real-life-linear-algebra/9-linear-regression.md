---
layout: default
---
{% include subpage-nav.html %}
{% include mathjax.html %}

## Notes
* How to perform the linear least-squares method on a dataset-done.
* Applying the least-squares method to facial recognition
* Computing correlation between two datasets

### Facial Recognition with Linear Algebra
1. Take an image and turn it to a grayscale image.
2. Convert the matrix to a vector.
3. Turn the data set into a matrix with each column as a person's image.
4. Find the linear combination which is closest to the image we are looking for. We need linear regression!
5. It is just matching the pixels.

### Computing correlation betw3een two datasets
1. Subract mean from every item of each column.
2. $$corr(c, d) = \frac{c.d}{||c||||d||}$$