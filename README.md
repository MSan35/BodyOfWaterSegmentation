# Body of Water Segmentation Model

This repository contains a U-Net model for detecting and segmenting bodies of water in satellite images. The model uses TensorFlow and Keras for training and inference.

## Table of Contents

1. [Overview](#overview)
2. [Requirements](#requirements)
3. [Dataset](#dataset)
4. [Testing](#testing)
5. [Conclusion](#conclusion)

## Overview

The goal of this project is to create an AI model that can segment bodies of water in satellite images. This model uses the U-Net architecture for semantic segmentation and is trained using images from Sentinel-2.

## Requirements

The following libraries are required to run the project:

- TensorFlow >= 2.0
- numpy
- matplotlib
- pillow
- os

## Dataset

The model is trained using satellite images from Sentinel-2. The dataset includes:
- **Images**: Satellite images of regions containing bodies of water.
- **Masks**: Corresponding binary masks where white represents water and black represents non-water areas.

Dataset link: https://www.kaggle.com/datasets/franciscoescobar/satellite-images-of-water-bodies

Unseen images for testing taken from sattelites.pro

## Testing

The model's accuracy on seen data was 82.57%\
![alt text](https://github.com/MSan35/BodyOfWaterSegmentation/blob/main/train_accuracy.png)

Loss:\
![alt text](https://github.com/MSan35/BodyOfWaterSegmentation/blob/main/train_loss.png)

Here are some tests on unseen data:\
![alt text](https://github.com/MSan35/BodyOfWaterSegmentation/blob/main/test_results/unseen_test_1.png)
![alt text](https://github.com/MSan35/BodyOfWaterSegmentation/blob/main/test_results/unseen_test_2.png)
![alt text](https://github.com/MSan35/BodyOfWaterSegmentation/blob/main/test_results/unseen_test_3.png)
![alt text](https://github.com/MSan35/BodyOfWaterSegmentation/blob/main/test_results/unseen_test_4.png)

## Conclusion

Looking at the tests on unseen data, the model clearly has a hard time when lighter colors are present in the image such as snow or city environments.\
There is room for improvement but for the first iteration, the accuracy on seen data is great and when looking at darker colored land images such as the first and fourth test, we can see the model perform as expected.

