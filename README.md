# Bilateral-Filtering
A bilateral filter is a non-linear, edge-preserving, and noise-reducing smoothing filter for images. It replaces the intensity of each pixel with a weighted average of intensity values from nearby pixels. This weight can be based on a Gaussian distribution. Crucially, the weights depend not only on Euclidean distance of pixels, but also on the radiometric differences (e.g., range differences, such as color intensity, depth distance, etc.). This preserves sharp edges.

Adobe Photoshop implements a bilateral filter in its surface blur tool. GIMP implements a bilateral filter in its Filters-->Blur tools; and it is called Selective Gaussian Blur. The free G'MIC plugin Repair → Smooth [bilateral] for GIMP adds more control. A simple trick to efficiently implement a bilateral filter is to exploit Poisson-disk subsampling.

The bilateral filter in its direct form can introduce several types of image artifacts:

Staircase effect – intensity plateaus that lead to images appearing like cartoons
Gradient reversal – introduction of false edges in the image.
There exist several extensions to the filter that deal with these artifacts, like the scaled bilateral filter that uses downscaled image for computing the weights. Alternative filters, like the guided filter, have also been proposed as an efficient alternative without these limitations.
