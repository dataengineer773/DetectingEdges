We want to find the edges in an image, Use an edge detection technique like the Canny edge detector, Edge detection is a major topic of interest in computer vision. Edges are important because they are
areas of high information. For example, in our image one patch of sky looks very much like another and
is unlikely to contain unique or interesting information. However, patches where the background sky
meets the airplane contain a lot of information (e.g., an object’s shape). Edge detection allows us to
remove low-information areas and isolate the areas of images containing the most information.
There are many edge detection techniques (Sobel filters, Laplacian edge detector, etc.). However, our
solution uses the commonly used Canny edge detector. How the Canny detector works is too detailed
for this book, but there is one point that we need to address. The Canny detector requires two
parameters denoting low and high gradient threshold values. Potential edge pixels between the low and
high thresholds are considered weak edge pixels, while those above the high threshold are considered
strong edge pixels. OpenCV’s Canny method includes the low and high thresholds as required
parameters. In our solution, we set the lower and upper thresholds to be one standard deviation below
and above the image’s median pixel intensity. However, there are often cases when we might get better
results if we used a good pair of low and high threshold values through manual trial and error using a
few images before running Canny on our entire collection of images.
