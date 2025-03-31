# Lossy Compression by Convolutional Autoencoder

## Project Overview

This project implements lossy image compression using convolutional autoencoders. By leveraging deep learning techniques, we achieve significant compression rates while maintaining visual quality, demonstrating the potential of neural networks for image compression.

## Introduction

Image compression is essential for efficient storage and transmission of visual data. This repository demonstrates how convolutional neural networks can be used to create compact representations of images through an encoder-decoder architecture, providing an alternative to traditional compression algorithms.

## Models

The project implements two convolutional autoencoder architectures:

### Model 1: Baseline Autoencoder

Our baseline model uses a standard convolutional architecture with the following components:

- Convolutional layers with Batch Normalization
- ReLU activation functions
- MaxPooling for downsampling
- A bottleneck layer for compression

![Baseline Architecture](/assests/model1.jpg)

### Model 2: Enhanced Autoencoder

The enhanced model builds upon the baseline with additional improvements:

- Skip connections between encoder and decoder
- Additional convolutional layers
- More sophisticated upsampling techniques
- Better regularization strategies

![Enhanced Architecture](/assests/model2.jpg)

Both models are trained to minimize reconstruction loss while maximizing compression efficiency.

## Results

### Visual Reconstruction Quality

#### Reconstruction Evolution Over Training Epochs

The image below shows how reconstruction quality improves over training epochs for both models:

![Reconstruction Evolution](/assests/recon_over_epochs.png)
_Reconstruction quality improvement over training epochs for both baseline (top) and enhanced (bottom) models_

#### Original vs Reconstructed Comparison

Our experiments show clear visual differences between original images and their reconstructions:

![Original vs Reconstructed Comparison](/assests/orig_recon_diff.png)
_From top to bottom: Original images, Baseline reconstructions, Enhanced reconstructions, Difference maps (Enhanced - Baseline)_

The enhanced model consistently produces reconstructions with better detail preservation, particularly in areas with fine textures and subtle color gradients.

### Training Performance

The training and validation loss curves demonstrate the learning progress of both models:

![Training and Validation Loss](/assests/train_test_loss.png)
_Training and validation loss for both models over 20 epochs_

Key observations:

- Both models converge after approximately 10-15 epochs
- The enhanced model achieves lower initial loss values
- The enhanced model exhibits better generalization with smaller gaps between training and validation loss
- Final MSE loss values are below 0.01 for both models, with the enhanced model achieving slightly better results

## How to Use This Repository

To explore these results yourself:

1. Clone this repository:

```bash
git clone https://github.com/jaydenw712/Lossy-Compression-by-Convolutional-Autoencoder.git
cd Lossy-Compression-by-Convolutional-Autoencoder
```

2. Install the required dependencies:

```bash
pip install -r requirements.txt
```

3. Run the Jupyter Notebook!

## Requirements

- Python 3.7+
- PyTorch
- NumPy
- Matplotlib
- Pillow
- Jupyter

## License

This project is licensed under the MIT License - see the LICENSE file for details.
