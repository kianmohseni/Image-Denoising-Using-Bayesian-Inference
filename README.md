# Image Denoising Using Bayesian Inference
## Project Overview
This project demonstrates a probabilistic approach to image denoising by leveraging Bayesian inference. Using a corrupted binary image of a bear, the goal is to reconstruct the original image by modeling the joint distribution of pixels and applying Gibbs sampling to infer the denoised image.

## Key Features
1. Input Image:

- The noisy image **(noisy_bear.png)** and its ground truth **(original_bear.png)** are loaded and preprocessed.
- Pixel values are binarized to -1 and +1.

2. Probabilistic Modeling:

- A simple prior is defined over the joint distribution of the noisy and clean image.
- Neighboring pixels are modeled with a potential function to capture spatial relationships.

3. Gibbs Sampling:

- Samples from the posterior distribution of pixel values are iteratively updated.
- Iterative snapshots of the reconstruction process are visualized.

4. Final Reconstruction:

- The reconstructed image is displayed after convergence.

## Tools and Libraries
- NumPy: Numerical computations for probabilistic modeling.
- OpenCV: Image loading and preprocessing.
- Matplotlib: Visualization of denoising iterations and results.
- Mathematical Model: Implements Gibbs sampling based on Bayesian principles.

## Workflow
1. Loading and Preprocessing:

- Load the noisy and ground truth images.
- Binarize pixel values and pad the images for computational ease.

2. Probabilistic Model:

- Define the joint distribution P(X,Y) where X is the noisy image and Y is the reconstructed image.

3. Gibbs Sampling:

- Initialize pixel values randomly.
- For each pixel, update its value based on its neighbors and the noisy image.
- Save snapshots at regular intervals to visualize the denoising process.

4. Reconstruction:

- The reconstructed image is obtained after a specified number of iterations.

## Results
- Iterative reconstruction snapshots demonstrate gradual improvement in image quality.
- The final reconstructed image closely resembles the original ground truth image.

## Future Enhancements
- Extend the model to grayscale or color images.
- Experiment with more sophisticated priors and potential functions.
- Optimize Gibbs sampling for faster convergence.
