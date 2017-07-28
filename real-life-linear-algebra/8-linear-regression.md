---
layout: default
---
{% include subpage-nav.html %}
{% include mathjax.html %}

### Linear Regression- Least-Squares Method
Find the line $$mx+b$$ where $$m$$ is the slope and $$b$$ is the intercept of the point that best estimates the data points.
### Linear Regression using Linear Algebra
With three data points given as $$(2, 4), (3, 7), (4, 9)$$, we can create a linear system with $$m$$ and $$b$$ as unknowns.   
    
    
$$ \left[ {\begin{array}{cc}
   2 & 1 \\
   3 & 1 \\
   4 & 1 \\
  \end{array} } \right] 
  \left[ {\begin{array}{c}
   m \\
   b \\
  \end{array} } \right] = 
  \left[ {\begin{array}{c}
  4 \\
  7 \\
  9 \\
  \end{array} }\right]$$
  
But, a solution for $$m$$ and $$b$$ might not always exist. Infact it usually does not. That is why we want the best approximation. Interestingly enough,
it turns out that solving the any linear system as follows will always give the best approximation (under least-squares estimations).    
    
    
$$M^{T}Mx = M^{T}b$$    
With this, we can proceed with our previous example.    

$$ \left[ {\begin{array}{ccc}
   2 & 3 & 4 \\
   1 & 1 & 1 \\
  \end{array} } \right]
   \left[ {\begin{array}{cc}
   2 & 1 \\
   3 & 1 \\
   4 & 1 \\
  \end{array} } \right] 
  \left[ {\begin{array}{c}
   m \\
   b \\
  \end{array} } \right] = 
  \left[ {\begin{array}{ccc}
   2 & 3 & 4 \\
   1 & 1 & 1 \\
  \end{array} } \right]
  \left[ {\begin{array}{c}
  4 \\
  7 \\
  9 \\
  \end{array} }\right]$$  
  
 
 $$ \left[ {\begin{array}{ccc}
   29 & 9 \\
   9 & 3 \\
  \end{array} } \right]
  \left[ {\begin{array}{c}
   m \\
   b \\
  \end{array} } \right] = 
  \left[ {\begin{array}{ccc}
   65 \\
   20 \\
  \end{array} } \right]$$       
  
  Solving the system above, we get $$m = 2.5$$ $$b = -0.8333$$.    
  
  The problem of least-square approximation can also be solved with MATLAB or Octave in a single line as
  ````octave
  solution = inverse (M' * M) * (M' * y)
  ````
  
 