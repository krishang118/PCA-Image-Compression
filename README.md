# PCA-based Image Compression on MNIST

This project demonstrates the use of Principal Component Analysis (PCA) for image compression using the MNIST handwritten digits dataset. The workflow includes data preprocessing, applying PCA with various numbers of components, visualizing reconstructions, and analyzing compression performance.

## Overview
- **Dataset:** [MNIST](http://yann.lecun.com/exdb/mnist/) (handwritten digits, 28x28 grayscale images)
- **Goal:** Compress and reconstruct images using PCA, analyze trade-offs between compression ratio, explained variance, and reconstruction error.
- **Tools:** Python, NumPy, Matplotlib, scikit-learn

## Workflow
1. **Data Loading & Preprocessing**
    - Loads the MNIST dataset using `fetch_openml` from scikit-learn.
    - Uses the first 10,000 training samples for analysis.
    - Normalizes pixel values to [0, 1] and reshapes images for PCA.

2. **PCA Compression**
    - Applies PCA with different numbers of components: 10, 50, 100, 200, 400.
    - For each setting, reconstructs the images and calculates explained variance and compression ratio.

3. **Visualization**
    - Plots original and reconstructed images for qualitative comparison.
    - Shows how increasing the number of components improves reconstruction quality.
    - Visualizes the first 16 principal components as images.

4. **Quantitative Analysis**
    - Computes Mean Squared Error (MSE) between original and reconstructed images.
    - Plots:
        - Reconstruction error vs. number of components
        - Explained variance vs. number of components
    - Summarizes compression results for all tested component counts.

## Key Results
- **Compression Ratios & Explained Variance:**
    - 10 components: ~98.7% compression, ~49.4% variance explained
    - 50 components: ~93.6% compression, ~82.8% variance explained
    - 100 components: ~87.2% compression, ~91.7% variance explained
    - 200 components: ~74.5% compression, ~96.8% variance explained
    - 400 components: ~49.0% compression, ~99.6% variance explained
- **Reconstruction Error:**
    - Decreases as the number of components increases
    - Trade-off between compression and image quality

## How to Run
1. **Install dependencies:**
    ```bash
    pip install numpy matplotlib scikit-learn
    ```
2. **Open and run the notebook:**
    - Use Jupyter Notebook or JupyterLab to open `PCA.ipynb`.
    - Execute all cells to reproduce the analysis and visualizations.

## Files
- `PCA.ipynb`: Main notebook with code, analysis, and visualizations
- `LICENSE`: Project license

## References
- [Principal Component Analysis (Wikipedia)](https://en.wikipedia.org/wiki/Principal_component_analysis)
- [scikit-learn PCA documentation](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html)
- [MNIST dataset](http://yann.lecun.com/exdb/mnist/)

## License
See [LICENSE](LICENSE) for details. 