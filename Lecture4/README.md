# Lecture 4

# Image Segmentation

## 1. What is Image Segmentation?
- Image segmentation is the process of partitioning a digital image into multiple segments (sets of pixels, also known as image objects).

# 2. Edge-Based Segmentation
- Edge-based segmentation is the process of partitioning a digital image into multiple segments (sets of pixels, also known as image objects) using edge detection.

## 2.1. Edge Detection

- Marr-Hildreth Edge Detection Algorithm
- Canny Edge Detection Algorithm

### 2.1.1. Marr-Hildreth Edge Detection Algorithm

The laplacian of Gaussian (LoG) operator, also known as the Marr-Hildreth operator, is an edge detector which uses the Laplacian of Gaussian to detect edges. It is an approximation to the operator of the second derivative of the image intensity function with respect to space.

![Marr-Hildreth Edge Detection Algorithm](![Marr-Hildreth Edge Detection Algorithm](https://www.researchgate.net/publication/281392911/figure/fig2/AS:614315212173326@1523475568868/Block-diagram-of-the-Marr-Hildreth-algorithm.png))
- Steps:
    - Apply Gaussian Filter to smooth the image.
    - Apply Laplacian Filter to find the edges.
    - Apply Zero Crossing to find the edges.

### 2.1.2. Canny Edge Detection Algorithm

The Canny edge detector is an edge detection operator that uses a multi-stage algorithm to detect a wide range of edges in images. It was developed by John F. Canny in 1986. Canny also produced a computational theory of edge detection explaining why the technique works.

- Steps:
    - Apply Gaussian Filter to smooth the image.
    - Apply Gradient Filter to find the edges.
    - Apply Non-Maximum Suppression to find the edges.
    - Apply Hysteresis Thresholding to find the edges.


## 2.1.3. Hough Transform

The Hough transform is a feature extraction technique used in image analysis, computer vision, and digital image processing. The purpose of the technique is to find imperfect instances of objects within a certain class of shapes by a voting procedure. This voting procedure is carried out in a parameter space, from which object candidates are obtained as local maxima in a so-called accumulator space that is explicitly constructed by the algorithm for computing the Hough transform.


## 2.2. Region-Based Segmentation

- Region-based segmentation is the process of partitioning a digital image into multiple segments (sets of pixels, also known as image objects) using region growing.

### 2.2.1. Region Growing

- Region growing is a simple region-based image segmentation method. It is also classified as a pixel-based image segmentation method since it involves the selection of initial seed points. Region growing is typically used for cases where an image has an uneven background illumination or a non-uniform foreground intensity.

- Steps:
    - Select a seed point.
    - Select a threshold.
    - If the pixel intensity value is greater than the threshold, add it to the region.
    - Repeat the previous step until the region stops growing.

### 2.2.2. Region Splitting and Merging

- Region splitting and merging is a simple region-based image segmentation method. It is also classified as a pixel-based image segmentation method since it involves the selection of initial seed points. Region splitting and merging is typically used for cases where an image has an uneven background illumination or a non-uniform foreground intensity.

- Steps:
    - Split the image into regions.
    - Merge the regions until the region stops growing.

### Exercise

1. Given a picture of a player in a football match, segment the player from the background.

 - Solution:

    - Apply Canny Edge Detection Algorithm to find the edges.
    - Apply Region Growing to find the player.

2. Given a picture of a multiple coins, segment the coins from the background.

 - Solution:

    - Apply Canny Edge Detection Algorithm to find the edges.
    - Apply Region Splitting and Merging to find the coins.

3. Given a picture that has salt and pepper noise, remove the noise.

 - Solution:

    - Apply Median Filter to remove the noise.

4. Given a picture that has motion blur, remove the blur.

 - Solution:

    - Apply Inverse Filter to remove the blur.

5. Given a picture that has motion blur and noise, remove the blur and the noise.

    - Solution:
    
        - Apply Wiener Filter to remove the blur and the noise.


## 3. Thresholding

- Thresholding is the simplest method of image segmentation. From a grayscale image, thresholding can be used to create binary images.

- Steps:
    - Select a threshold.
    - If the pixel intensity value is greater than the threshold, set it to 1.
    - If the pixel intensity value is less than the threshold, set it to 0.

It is mostly used for cases where the image has a uniform background illumination or a uniform foreground intensity.

As an example, consider a photo 


