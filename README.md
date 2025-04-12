# Image Compression using K-Means Clustering

## Overview
An efficient image compression project that reduces the number of colors in an image using **K-Means** and **Mini-Batch K-Means** clustering techniques. This approach compresses images by clustering similar color pixels and replacing them with their centroid values, ultimately reducing file size while retaining visual similarity.

## Features
- **Color Reduction**: Compress images by reducing the color palette to a specified number of dominant colors.
- **K-Means Clustering**: Uses the standard K-Means algorithm for clustering pixel colors.
- **Mini-Batch K-Means**: Leverages a faster, memory-efficient version of K-Means that processes data in mini-batches.
- **Image Resizing Option**: Optionally resize images to accelerate the clustering process.
- **Visualization**: Displays original and compressed images side-by-side for comparison.
- **File Size Analysis**: Provides details on file size reduction after compression.

## Technologies Used
- **Python** – Core language for the image processing and clustering.
- **OpenCV (cv2)** – For image loading, processing, and saving.
- **NumPy** – Handling multi-dimensional image arrays.
- **Matplotlib** – To visualize the images.
- **Scikit-Learn** – Utilizes `MiniBatchKMeans` for faster clustering computations.

## How It Works
1. **Load and Process Image**: The image is loaded, optionally resized, and preprocessed (converted to RGB and reshaped).
2. **Apply Clustering**:
   - **K-Means**: The algorithm clusters pixel colors based on Euclidean distance in RGB space.
   - **Mini-Batch K-Means**: Processes random mini-batches for faster convergence on large images.
3. **Reconstruct Compressed Image**: Each pixel is replaced with its corresponding cluster centroid, resulting in a compressed image with a reduced color palette.
4. **Save and Display**: The compressed image is saved (using reduced JPEG quality if desired) and compared visually against the original.

