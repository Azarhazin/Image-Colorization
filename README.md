# Image-Colorization
Input:
  Gray scale images
Output:
  Colored images

A Generative Adversarial Network which include a UNET based Generator and a PATCH Discriminator

#########################
It imports necessary libraries such as os, glob, time, numpy, PIL, pathlib, tqdm, matplotlib, skimage, and torch for various functionalities.
It sets the path to the image dataset, loads the image file names, randomly selects a subset of images for training and validation, and creates lists of training and validation file paths.
It visualizes a grid of images from the training set using matplotlib.
It defines a ColorizationDataset class to preprocess and load the images for training and validation.
It defines a make_dataloaders function to create data loaders for training and validation sets.
It creates data loaders for the training and validation sets.
It defines the U-Net architecture using UnetBlock and Unet classes.
It defines a patch discriminator using the PatchDiscriminator class.
It defines a GAN loss function using the GANLoss class.
It defines a function to initialize the weights of the models.
It defines a function to evaluate the PSNR (Peak Signal-to-Noise Ratio) of the model's output.
It initializes the main model (MainModel) with the U-Net generator, discriminator, optimizers, and loss functions.
It defines functions to set requires_grad for model parameters, forward pass, backward pass for discriminator and generator, and optimization step.
It defines an AverageMeter class to track average values of a metric.
It defines a function to create meters for loss tracking.
It defines a function to update the loss meters with the current loss values.
It defines a function to convert images from Lab color space to RGB color space.
It defines a function to visualize the model's output on a sample batch of data.
It defines a function to log the results of the loss meters.
It defines a function to train the model for a specified number of epochs.
It initializes an instance of the main model (MainModel) and trains it using the provided data loaders.

In summary, the code sets up a colorization model using a U-Net architecture and trains it on a dataset of grayscale images and their corresponding color images. The model learns to generate colorized images given the grayscale input.
