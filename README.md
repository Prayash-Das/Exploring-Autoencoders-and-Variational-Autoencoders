# Autoencoder and Variational Autoencoder Experiments

## Introduction

This repository contains experiments with Autoencoders and Variational Autoencoders (VAE) on MNIST image data and a custom dataset (`data1.csv`). The experiments include:

1. **MNIST Autoencoder Error Analysis**
2. **Vanilla and Deep Autoencoders on `data1.csv`**
3. **Variational Autoencoder with modifications**

## Part I: MNIST Autoencoder Error Analysis

### Steps:

1. **Load and Train Autoencoder**:
   - Loaded the MNIST dataset.
   - Trained a basic autoencoder with one hidden layer.

2. **Calculate Reconstruction Errors**:
   - Calculated the reconstruction errors for the test dataset.
   - Sorted and identified the top-10 images with the highest reconstruction errors.

3. **Visualize and Analyze**:
   - Displayed the original and decoded images for these top-10 error cases.

### Results:

- Reconstruction errors varied significantly across the test dataset.
- The top-10 images with the highest errors often had complex or distinct features that the autoencoder struggled to reproduce accurately.

## Part II: Autoencoder on `data1.csv`

### Steps:

1. **Vanilla Autoencoder**:
   - Trained a vanilla autoencoder with one hidden layer (2 nodes) on the first 28 columns of `data1.csv`.
   - Plotted the histogram of reconstruction errors.

2. **Deep Autoencoder**:
   - Trained a deep autoencoder with two hidden layers (final hidden layer with 2 nodes) on the same data.
   - Plotted the histogram of reconstruction errors and compared with the vanilla autoencoder.

3. **Scatter Plots**:
   - Plotted the scatter plots of the hidden layer outputs for both vanilla and deep autoencoders.
   - Colored the scatter plots based on the `class` column from `data1.csv`.

### Results:

- The deep autoencoder showed improved performance in terms of reconstruction errors compared to the vanilla autoencoder.
- Scatter plots indicated clear clustering of different classes in the hidden layer space, with the deep autoencoder providing better separation.

## Part III: Variational Autoencoder (VAE) Testing

### Steps:

1. **Run VAE Example**:
   - Implemented the VAE as per Keras documentation.
   - Trained the model and plotted the generated images.

2. **Modify Network Architecture**:
   - Modified the VAE architecture to add an additional layer with 64 units before the bottleneck layer.
   - Trained the modified VAE and compared the quality of generated images.

### Results:

- The addition of an extra layer improved the quality of generated images, indicating that a more complex encoder can capture the data distribution better.

## Conclusion

This repository demonstrates the effectiveness of different types of autoencoders on image and tabular data. The experiments show how model complexity impacts reconstruction quality and how latent space representations can be visualized and interpreted.

## How to Run

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Prayash-Das/autoencoder-vae-experiments.git
   cd autoencoder-vae-experiments
