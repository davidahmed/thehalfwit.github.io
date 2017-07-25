---
layout: default
---
{% include subpage-nav.html %}

# Simple Matrix Operations
In this section we try out basic (i.e. matrix addition and scalar matrix multiplication) operations on images in the form of matrices.
We can actually use these ideas to emulate effects such as ***fading and color-inversion.*** We can also extend the idea of linear combinations 
to create multiple transparent and overlying images.
### Read and display an image
````r
img = imread('./img/mona.jpg')
imshow (img);
````

### Invert a simple image
````r
[img, map, alpha] = imread('./img/mona.jpg');
imgInverted = 255 - img;
imshow (imgInverted);
````
### Adding linear combination of two images.
We could have also played with a linear combination in the inversion of the image above. Or, we can also add linear combination of images.

````r
tigerImage = imread('./img/tiger.jpg');
catImage = imread('./img/cat.jpg');
imshow (alpha * catImage + (1 - alpha) * tigerImage );
````

### Simply grayscale an image

````r
[x, map] = rgb2ind (img);
grayImg = ind2gray (x, map);
imshow (grayImg);
````

### Squaring and image
````r
grayImgSquared = grayImg * grayImg';
grayImgSquared = grayImgSquared * (1/ max(max(grayImgSquared)));
imshow (grayImgSquared);
````

# Notes
Sum Matrices [ Unit 2 Sum of Matrix ]
* To compute matrix addition
* to compute scalar multiplication
* to invert a grayscale image with matrix arithmetic
* manipulate colors of an image with matrix arithmetic.
* - Get inverted -M + 255(1). Playing with R G B
* -combining two images. Linear Combination of two images (why? we dont want them to go beyond 255.) added effects. fade away. Concwz cobnation (insert eh eq)