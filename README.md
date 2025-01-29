# Principal Component Analysis (PCA) on Horse and Bird Shapes

## Overview
This assignment is part of my coursework at FSU, this applies Principal Component Analysis (PCA) using Singular Value Decomposition (SVD) to analyze a dataset of horse silhouettes and compare them to a bird silhouette. The goal is to explore the principal components of the horse images and examine how the bird image projects onto the same space.

## Dataset
- **`bird.png`**: A single image containing a bird silhouette.
- **`horses.zip`**: A collection of 327 horse images, each of size **128 × 128** pixels.
- All images are normalized so that pixel values range between **0 and 1**.

## Steps Implemented

### 1. Principal Component Analysis (PCA) on Horses
- Perform PCA using **Singular Value Decomposition (SVD)** on the horse dataset.
- Discard the **two largest singular values**.
- Plot the graph of the remaining singular values sorted in decreasing order.

### 2. Projection of Horses onto First Two Principal Components
- Compute the **projection of each horse image** onto the first two principal components (PCs).
- Plot a **2D scatter plot** of these projections.

### 3. Projection of Bird Image onto Horse PCA Space
- Project the **bird image** onto the same **two PCs** computed from the horse dataset.
- Display the **horse projections in black** and the **bird projection as a red 'x'**.

### 4. PCA-Based Image Reconstruction
#### a) Reconstruction of a Horse Image (`horse060.png`)
- Reconstruct the **horse060.png** image using **20 principal components**.
- Apply **binary thresholding at 0.5** to obtain a clean silhouette.
- Display both the **original and reconstructed images**.

#### b) Reconstruction of the Bird Image
- Project the **bird image** onto the **top 20 PCs**.
- Reconstruct the **binary version** of the bird image using **thresholding at 0.5**.
- Display both the **original and reconstructed images**.

### 5. Distance to the 32-PC Subspace
- Compute the **distance of each horse image** to the **plane spanned by the 32 largest PCs**.
- Compute the **distance of the bird image** to the same subspace.
- Plot a graph of:
  - **x-axis:** Projection onto the second principal component.
  - **y-axis:** Distance to the 32-PC plane.
  - **Black points** represent horses, **red 'x'** represents the bird.

### 6. Histogram of Horse Distances
- Generate a **histogram of distances** obtained from the previous step for all horse images.

## How to Run
1. **Download and extract** `horses.zip` into the project directory.
2. **Load `bird.png`** and **normalize all images** so that the maximum value is 1.
3. **Run the script** to execute PCA, perform projections, reconstruct images, and generate plots.
4. **Visual outputs include:**
   - Singular value distribution
   - 2D projections of horse images with the bird image
   - Reconstructed images of a horse and the bird
   - Distance vs. second PC plot
   - Histogram of distances for horses

## Dependencies
- Python (>=3.7)
- NumPy
- SciPy (`scipy.linalg.svd` for SVD computations)
- Matplotlib (for visualization)
- OpenCV or PIL (for image loading and processing)

## Applications
PCA is widely used in:
- **Shape analysis** (e.g., identifying patterns in object silhouettes)
- **Dimensionality reduction** for large datasets
- **Image compression** and reconstruction
- **Anomaly detection** (e.g., identifying outliers like the bird in this case)

This assignment demonstrates the effectiveness of PCA in analyzing shapes and detecting variations in object silhouettes.
