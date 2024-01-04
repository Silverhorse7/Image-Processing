# Lecture 5 

## Region Based Segmentation

### 1. Region Growing

- Region growing is a simple region-based image segmentation method. It is also classified as a pixel-based image segmentation method since it involves the selection of initial seed points. Region growing is typically used for cases where an image has an uneven background illumination or a non-uniform foreground intensity.

- Steps:
    - Select a seed point.
    - Select a threshold.
    - If the pixel intensity value is greater than the threshold, add it to the region.
    - Repeat the previous step until the region stops growing.

- Advantages:
    - Simple.
    - Fast.

- Disadvantages:
    - The threshold is hard to select.
    - The region may not be homogeneous.
    - This method is sensitive to noise.


### 2. Region Splitting and Merging

- Region splitting and merging is a simple region-based image segmentation method. It is also classified as a pixel-based image segmentation method since it involves the selection of initial seed points. Region splitting and merging is typically used for cases where an image has an uneven background illumination or a non-uniform foreground intensity.

- Steps:
    - Split the image into regions.
    - Merge the regions until the region stops growing.

- Advantages:
    - The image could be split progressivly according to our demanded resolution because the number of splitting level is determined by the user.
    - We could split the image using the criteria we decide, such as mean or variance of segment pixel value.

- Disadvantages:
    - It may produce blocky segments.



## Morphological Image Processing

### 1. Morphological Operations

- Morphological operations are image processing operations that process images based on shapes.

- Morphological operations apply a structuring element to an input image and generate an output image.

- The Structuring element Hit or Miss is used to detect the presence of a particular configuration of pixels in an image.

- If it is a hit, the center pixel of the structuring element is set to 1, otherwise it is set to 0.

If it is a hit it's erosion, otherwise it's dilation.




### 2. Erosion

- Erosion is a morphological operation that shrinks the shapes in an image.

- Erosion is used to remove small objects from an image.

- Erosion is also used to detach two connected objects.

- Erosion is also used to eliminate noise.

- We use structuring elements to perform erosion.

### 3. Dilation

- Dilation is a morphological operation that expands the shapes in an image.

- Dilation is used to join broken parts of an image.

- Dilation is also used to smooth the object boundaries.

- We use structuring elements to perform dilation.

### 4. Opening

- Opening is an erosion followed by a dilation.

- Opening is used to remove small objects from an image.

- Opening is also used to eliminate noise.

### 5. Closing

- Closing is a dilation followed by an erosion.

- Closing is used to join broken parts of an image.

- Closing is also used to smooth the object boundaries.


### Top Hat Transform

- The top hat transform is an operation that extracts small elements and details from given images.

- The top hat transform is defined as the difference between the input image and its opening by some structuring element.