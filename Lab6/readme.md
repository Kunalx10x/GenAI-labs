# Pix2Pix: Image-to-Image Translation on Edges2Shoes

This project implements a **Conditional Generative Adversarial Network
(cGAN)** based on the **Pix2Pix architecture**.\
The model learns to generate **realistic shoe images from edge-map
sketches** using paired image-to-image translation.

------------------------------------------------------------------------

## Table of Contents

-   Architecture
-   Dataset
-   Training Setup
-   Performance
-   How to Run

------------------------------------------------------------------------

## Architecture

The system consists of two neural networks trained in an adversarial
setting.

### Generator --- U-Net

The **Generator** uses a **U-Net encoder--decoder architecture**.

Key characteristics:

-   Convolutional encoder that compresses the input edge-map
-   Decoder that reconstructs the output image
-   **Skip connections** between encoder and decoder layers
-   Helps preserve spatial information from the input sketch

The generator learns a mapping:

Edge Sketch → Realistic Shoe Image

------------------------------------------------------------------------

### Discriminator --- PatchGAN

The **Discriminator** uses a **PatchGAN classifier**.

Instead of classifying the entire image as real or fake, PatchGAN:

-   Evaluates **local image patches**
-   Penalizes unrealistic textures and structures
-   Encourages sharper and more realistic outputs

The discriminator receives:

(Input Sketch + Generated Image)

and determines whether the pair is **real or fake**.

------------------------------------------------------------------------

## Dataset

**Dataset Name:** edges2shoes

The dataset contains **paired images**: - Edge-drawn sketch of a shoe -
Corresponding real shoe photograph

------------------------------------------------------------------------

### Preprocessing

-   Images resized to **256 × 256 pixels**
-   Pixel values normalized to **\[-1, 1\]**
-   Paired sketch-image alignment maintained

------------------------------------------------------------------------

## Training Setup

### Loss Function

Training uses a combination of:

**Adversarial Loss (Binary Cross Entropy)**\
Encourages the generator to fool the discriminator.

**L1 Loss**\
Ensures generated images are close to the ground truth.

Generator Loss = Adversarial Loss + L1 Loss

------------------------------------------------------------------------

### Optimizers

Two **Adam optimizers** are used:

-   Generator optimizer
-   Discriminator optimizer

Typical parameters:

Learning Rate = 0.0002\
Beta1 = 0.5

------------------------------------------------------------------------

### Hardware

Training executed using:

GPU: **NVIDIA T4**\
Framework: **PyTorch**

------------------------------------------------------------------------

## Performance

The model was trained for **25 epochs**.

Example snapshot:

  Epoch   Generator Loss   Discriminator Loss
  ------- ---------------- --------------------
  8       11.4671          0.1717

This indicates a **stable adversarial training process** where the
generator improves while the discriminator remains balanced.

------------------------------------------------------------------------

## How to Run

### Install Dependencies

pip install torch torchvision matplotlib numpy

### Run the Notebook

1.  Open the notebook in **Jupyter** or **Google Colab**
2.  Run all cells

The notebook will: - Load the edges2shoes dataset - Train the Pix2Pix
model - Generate shoe images from sketches

------------------------------------------------------------------------

## Key Concepts Demonstrated

-   Conditional GANs (cGAN)
-   Pix2Pix architecture
-   U-Net generator
-   PatchGAN discriminator
-   Image-to-image translation
-   Adversarial training
