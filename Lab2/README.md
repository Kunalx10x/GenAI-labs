# GenAI-Lab-2
# Generative Adversarial Network (GAN) for Fashion-MNIST

## Project Overview
This project implements a Deep Convolutional Generative Adversarial Network (DCGAN) to generate synthetic images of clothing items resembling the Fashion-MNIST dataset. The model consists of a Generator that creates images from random noise and a Discriminator that distinguishes between real and fake images.

## Objectives
* Train a GAN to generate realistic 28x28 grayscale images.
* Implement **Label Smoothing** and **Batch Normalization** to stabilize training.
* Overcome common GAN failure modes like **Mode Collapse**.
* Evaluate the quality of generated images using a pre-trained classifier.

## Tech Stack
* **Language:** Python 3.x
* **Framework:** TensorFlow / Keras
* **Libraries:** NumPy, Matplotlib
