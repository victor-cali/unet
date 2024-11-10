# U-Net for Biomedical Image Segmentation (Replication Study)

This repository is a fork of the original U-Net implementation by Olaf Ronneberger, Philipp Fischer, and Thomas Brox, focusing on replicating and evaluating claims from the paper **“U-Net: Convolutional Networks for Biomedical Image Segmentation.”** This study assesses U-Net's performance and computational efficiency in biomedical images segmentation.

## Overview

In their paper, Ronneberger et al. claim that U-Net, when trained with data augmentation, can achieve:
- Competitive Intersection over Union (IoU) accuracy with a limited number of annotated samples.
- Over 77% accuracy with fewer than 40 training images.
- Segmentation of a 512x512 image in under one second on a modern GPU.

This study aims to verify these claims through a replication of their segmentation tasks.

## Methodology

- **Dataset**: ISBI 2015 dataset, preprocessed as per the original repository.
- **Code**: Original authors' code, with minor adjustments to accommodate updated libraries.
- **Environment**: Experiments were conducted on an Asus ROG Zephyrus G14 with 32 GB RAM, AMD Ryzen 9 CPU, and Nvidia GeForce RTX 3070 GPU. Total GPU time was approximately 8 hours.

### Key Adjustments
- Updates for compatibility with newer libraries.
- Additional code for calculating Intersection over Union (IoU).
- Adjustemts to the code to run on the GPU.

## Results

The replication supports the authors' claims:
- **Mean IoU**: Achieved 0.9186, closely matching the reported 0.9203.
- **Segmentation Speed**: Processed 30 images at an average of 1.3 seconds per image.

These findings validate U-Net’s accuracy and speed for biomedical segmentation with limited data.

## Challenges and Limitations

- **Documentation**: Limited documentation and parameter specifications posed challenges in exactly replicating the results.
- **Data Augmentation**: Lack of detailed augmentation instructions led to some variability in the accuracy achieved.
- **Lack of Ground Truth Masks**: Only two masks were available to calculate the IoU

## Acknowledgements

The original code and dataset were sourced from [zhixuhao GitHub repository](https://github.com/zhixuhao/unet). 
