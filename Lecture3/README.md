# Lecture 3 


## Spatial Filtering

### 1. Convolution: a3ks w adrb
- Result = $\sum_{i=0}^{n-1} f(i)g(n-i)$
### 2. Cross-Correlation: 5leek zy m enta bs adrb
- Result = $\sum_{i=0}^{n-1} f(i)g(i+n)$
### 3. Autocorrelation : m3 nfsk
- Result = $\sum_{i=0}^{n-1} f(i)g(i-n)$

### 4. Smoothing Filters

#### 4.1. Median Filter
- Excellent for removing salt and pepper noise.


### 5. Sharpening Filters

- First Derivative Filters : $ f(x, y) = f(x + 1, y) - f(x, y) $S
- Second Derivative Filters : $f(x, y) = f(x + 1, y) + f(x - 1, y) + f(x, y + 1) + f(x, y - 1) - 4f(x, y)$


- Laplacian Filter : 

- Important Note: The Laplacian filter is used to detect edges in an image. It is a second derivative filter. It is very sensitive to noise. So, we use smoothing filters before applying the Laplacian filter.
 

 - Gradient Filters : find the difference between pixel(i) and pixel(i+1) and pixel(i) and pixel(i-1) and so on. Then draw.

Types of Gradient Filters:
1. Horizontal Gradient Filter
2. Vertical Gradient Filter

 - Important Note: The Gradient filter is used to detect edges in an image. It is a first derivative filter. It is very sensitive to noise. So, we use smoothing filters before applying the Gradient filter.