# Binarize Images

Various notebooks and attempts to binarize images and remove graph paper while preserving mathematical formulas.

The test_images notebook works best and demonstrates the pipeline. We still have work to do on thresholding certain types of images (more details in that notebook).

Below is the flow of the binarization pipeline. It is not optimized for all images but works well for some. 

### Convert to Grayscale
1. Read in image.
2. Convert to grayscale.

### Remove Noise
3. Apply a bilateral filter which is highly effective in noise removal while keeping edges sharp compared to other filters.

### Remove Any Shadows on Image
4. Dilate image to blur out text
5. Blur image with median blur function
6. Subtract this image from the original image that was a result of 3.

### Binarization
7. Apply Otsu Binarization which searches for a threshold based on the local minima in a bimodal histogram.

The test_images pdfs display the progress.

