# Texture Synthesis Using Deep Neural Networks

[link to the final presentation](https://docs.google.com/presentation/d/1oJG4EPsdERz_G8F8QaoSs0dIXxe0jEQO/edit#slide=id.gc96192608f_1_13)

[link to the flipped classroom presentation](https://docs.google.com/presentation/d/1KdXVSjycCC713hYuQSqGgU3k9v8bqbg9YlSAXOjOh_A/edit)

This project implements a texture synthesis algorithm based on the paper:

> **Gatys, Leon A., Alexander S. Ecker, and Matthias Bethge. "Texture synthesis using convolutional neural networks." *Advances in Neural Information Processing Systems* 28 (2015).**  
> [Link to paper](https://papers.nips.cc/paper_files/paper/2015/hash/563f0f6e5f9ecfd8ed63b7f0fdbbd009-Abstract.html)

## Overview

This repository demonstrates a method for synthesizing textures using deep convolutional neural networks (CNNs), specifically VGG-19. The technique leverages the feature maps from various layers of the CNN to capture and replicate the statistical characteristics of a texture image.

## Method Summary

The algorithm consists of the following key steps:

1. **Preprocessing**: The input texture image is resized and normalized. It is then reshaped into a format compatible with the VGG-19 network.

2. **Feature Extraction**: A modified version of the pretrained VGG-19 model is used to extract feature maps at multiple convolutional layers. These features capture hierarchical representations of the input texture.

3. **Gram Matrix Computation**: For each selected layer, a Gram matrix is computed from the feature maps. This matrix represents the correlations between different filter responses and captures texture information independent of spatial arrangement.

4. **Optimization**: A noise image is iteratively updated using gradient descent to match the Gram matrices of the original texture image. The loss function is defined as the mean squared error between the Gram matrices of the synthesized and target texture.

5. **Output**: The result is a new image that visually matches the texture characteristics of the original image but is initialized from random noise.

## Requirements

- Python 3.x
- PyTorch
- NumPy
- Matplotlib
- scikit-image
- Pretrained VGG-19 weights:  
  Download the file from: [https://web.eecs.umich.edu/~justincj/models/vgg19-d01eb7cb.pth](https://web.eecs.umich.edu/~justincj/models/vgg19-d01eb7cb.pth)  
  and place it in the `models/` directory.

## Usage

Run the Jupyter notebook `texture_synthesis_gatys.ipynb` step-by-step. Make sure the VGG-19 weights are downloaded beforehand.

## Acknowledgments

This work is a re-implementationof the foundational work by Gatys et al., which introduced the concept of using deep CNNs for artistic style transfer and texture generation.
