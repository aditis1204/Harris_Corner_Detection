# Harris Corner Detection
Corner detection is a method used in computer vision systems to extract certain features of an image. Corner detection is used frequently in video tracking, stitching motion detection and object recognition. Corner detection overlaps with the topic of interest point detection. Harris corner detection to stitch two different images together. It picks corners because, since it is the intersection of two edges, it represents a point in which the directions of these two edges change. The gradient of the image (in both directions) have a high variation, which can be used to detect it.

### The Harris Corner Detector algorithm in simple words is as follows :
Step 1. It determines which windows (small image patches) produce very large variations in intensity when moved in both X and Y directions (i.e. gradients).

Step 2. With each such window found, a score R is computed.

Step 3. After applying a threshold to this score, important corners are selected and marked.

Take the gray-scale of the original image. Apply a Gaussian filter to smooth out any noise. Apply Sobel operator to find the x and y gradient values for every pixel in the grayscale image. For each pixel p in the grayscale image, consider a m*m window around it and compute the corner strength function. Call this its Harris value. Find all pixels that exceed a certain threshold and are the local maxima within a certain window (to prevent redundant dupes of features). Compute a feature descriptor of all such points.
