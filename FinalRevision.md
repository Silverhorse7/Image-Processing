# Final Revision

- Circular Hough TRansform to identify circles

- To remove Gaussian noise, we use Gaussian filter/ Geometric mean filter
- To remove salt and pepper noise, we use median filter
- To remove Salt noise, we use minimum filter
- To remove pepper noise, we use maximum filter/Contraharmonic mean filter
- To remove Periodic noise, we use notch filter 



- Count objects with holes : 
    - 1. Apply erosion
    - 2. Apply dilation
    - 3. Connected component analysis and take each one in separte image and invert it
    - 4. if the objects contain white pixels, then it has holes


- Spot the difference:
    - 1. check that the two image have the same size.
    - 2. subtract the two images
    - 3. Threshold the result   
    - 4. Connected component analysis to highlight the difference

- Solve a puzzle:
    - 1. Smoothing using ccanny edge detection
    - 2. Edge base segmentation to split the puzzles from background
    - 3. Hough line transform to detect border and corners
    - 4. Alignment and matching 


