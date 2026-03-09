# Convolutional Encoder-Decoder for Image Reconstruction

This project implements a **Convolutional Encoder-Decoder
(Autoencoder)** using **PyTorch**.\
The model compresses images from the **CIFAR-10 dataset** into a latent
representation and then reconstructs them with minimal information loss.

------------------------------------------------------------------------

## Table of Contents

-   Model Architecture
-   Dataset and Preprocessing
-   Training Details
-   Results
-   How to Run

------------------------------------------------------------------------

## Model Architecture

The network consists of two main components:

1.  **Encoder** -- Compresses the image by reducing spatial dimensions
    while increasing feature depth.
2.  **Decoder** -- Reconstructs the original image from the compressed
    latent representation.

### Encoder

  -----------------------------------------------------------------------
  Layer                  Description
  ---------------------- ------------------------------------------------
  Layer 1                Conv2d (3 → 64 channels, kernel=3×3, stride=2,
                         padding=1) + ReLU

  Layer 2                Conv2d (64 → 128 channels, kernel=3×3, stride=2,
                         padding=1) + ReLU

  Layer 3                Conv2d (128 → 256 channels, kernel=3×3,
                         stride=2, padding=1) + ReLU
  -----------------------------------------------------------------------

### Decoder

  -----------------------------------------------------------------------
  Layer                  Description
  ---------------------- ------------------------------------------------
  Layer 1                ConvTranspose2d (256 → 128 channels, kernel=4×4,
                         stride=2, padding=1) + ReLU

  Layer 2                ConvTranspose2d (128 → 64 channels, kernel=4×4,
                         stride=2, padding=1) + ReLU

  Layer 3                ConvTranspose2d (64 → 3 channels, kernel=4×4,
                         stride=2, padding=1) + Tanh
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Dataset and Preprocessing

The model is trained on the **CIFAR-10 dataset**.

**Dataset Details**

-   Image Size: **32 × 32 pixels**
-   Channels: **RGB (3 channels)**
-   Dataset Classes: **10 categories**

**Preprocessing Steps**

Images are normalized with:

mean = (0.5, 0.5, 0.5)\
std = (0.5, 0.5, 0.5)

This maps pixel values from **\[0,1\] → \[-1,1\]**.

**Training Batch Size**

64

------------------------------------------------------------------------

## Training Details

  Parameter       Value
  --------------- ----------------------------------------
  Loss Function   Mean Squared Error (MSE)
  Optimizer       Adam
  Learning Rate   0.001
  Epochs          10
  Device          CUDA (GPU) if available, otherwise CPU

------------------------------------------------------------------------

## Results

The model showed consistent convergence over **10 epochs**.

  Epoch   Average Loss
  ------- --------------
  1       0.0252
  5       0.0037
  10      0.0019

The **low final loss (0.0019)** indicates that the autoencoder
successfully learned to reconstruct the important features of CIFAR-10
images.

------------------------------------------------------------------------

## How to Run

### 1. Install Dependencies

pip install torch torchvision matplotlib numpy

### 2. Run the Notebook

1.  Open **GAI_5.ipynb** in **Jupyter Notebook** or **Google Colab**.
2.  Run all cells.

The notebook will: - Download the CIFAR-10 dataset - Train the
convolutional autoencoder - Display reconstructed images.

------------------------------------------------------------------------

## Project Structure

GenAI_Lab/ │ ├── GAI_5.ipynb ├── README.md └── outputs/ └──
reconstructed_images.png

------------------------------------------------------------------------

## Key Concepts Demonstrated

-   Convolutional Autoencoders
-   Image Compression using Deep Learning
-   Image Reconstruction
-   PyTorch CNN Implementation
-   Latent Feature Representation
