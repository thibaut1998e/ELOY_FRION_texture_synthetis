# Texture Synthesis Using Deep Neural Networks

[link to the final presentation](https://docs.google.com/presentation/d/1oJG4EPsdERz_G8F8QaoSs0dIXxe0jEQO/edit#slide=id.gc96192608f_1_13)

[link to the flipped classroom presentation](https://docs.google.com/presentation/d/1KdXVSjycCC713hYuQSqGgU3k9v8bqbg9YlSAXOjOh_A/edit)

This project implements a texture synthesis algorithm based on the paper:

> **Gatys, Leon A., Alexander S. Ecker, and Matthias Bethge. "Texture synthesis using convolutional neural networks." *Advances in Neural Information Processing Systems* 28 (2015).**  
> [Link to paper](https://papers.nips.cc/paper_files/paper/2015/hash/563f0f6e5f9ecfd8ed63b7f0fdbbd009-Abstract.html)

**What is Texture Synthesis?**
Texture synthesis refers to the process of generating new images that replicate the visual "style" or texture of a reference image. In this implementation, we extend the idea by combining the content of one image with the style (texture) of another image, as popularized in neural style transfer. The resulting image maintains the general structure of the content image, but its texture, colors, and brushstroke-like patterns are derived from the style image.

**Project Description**
This Jupyter Notebook implements the neural style transfer approach based on a pre-trained convolutional neural network (VGG-19). The goal is to optimize a new image that combines:

The high-level content features of a content image.

The style features captured as Gram matrices from a style image.

The optimization minimizes a loss function composed of both content and style losses.



## Requirements

- Python 3.x
- PyTorch
- NumPy
- Matplotlib
- scikit-image
- Pretrained VGG-19 weights:  
  Download the file from: [https://web.eecs.umich.edu/~justincj/models/vgg19-d01eb7cb.pth](https://web.eecs.umich.edu/~justincj/models/vgg19-d01eb7cb.pth)

## Acknowledgments

This work is a re-implementationof the foundational work by Gatys et al., which introduced the concept of using deep CNNs for artistic style transfer and texture generation.
