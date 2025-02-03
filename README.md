# CIFAR-10 Image Generation with GANs

## Overview

This project implements a Generative Adversarial Network (GAN) designed to generate high-quality images from the CIFAR-10 dataset. The CIFAR-10 dataset consists of 60,000 32x32 color images across 10 different classes, making it a popular benchmark for machine learning algorithms.

The GAN architecture comprises two neural networks: the **Generator** and the **Discriminator**. The Generator creates fake images from random noise, while the Discriminator evaluates the authenticity of these images against real images from the dataset. The two networks are trained simultaneously in a competitive setting, where the Generator aims to produce images that are indistinguishable from real images, and the Discriminator strives to correctly classify real and fake images.

## Project Structure

- **Generator**: A neural network that transforms a latent vector (random noise) into a synthetic image. It utilizes transposed convolutional layers to upsample the input and generate images with spatial hierarchies.
  
- **Discriminator**: A neural network that classifies images as real or fake. It uses convolutional layers to downsample input images, extracting features that help in distinguishing between real and generated images.
  
- **Training Procedure**: The GAN is trained using the Binary Cross-Entropy loss function, with Adam optimizers for both networks. The training process involves alternating updates to the Generator and Discriminator, allowing both to improve over time.

## Key Features

- **Convolutional Architecture**: Both the Generator and Discriminator utilize convolutional layers, which are more effective for processing image data compared to traditional fully connected layers.
  
- **Batch Normalization**: Incorporated in both networks to stabilize training and improve convergence rates.
  
- **Activation Functions**: The Generator uses Tanh activation for the output layer to ensure pixel values are in the range [-1, 1], while the Discriminator employs Leaky ReLU activations to allow for better gradient flow.

## Installation

To run this project, ensure you have Python installed along with the necessary libraries. You can install the required packages using:

```bash
pip install torch torchvision numpy





![Generated Image at epoch 99](https://github.com/alirzx/Cifar10-Image-Generation-Using-GANs/blob/main/generated_images/epoch_99.png?raw=true)
