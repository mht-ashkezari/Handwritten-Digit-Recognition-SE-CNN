# Handwritten Digit Recognition using CNN with Squeeze-and-Excitation Blocks

This project aims to enhance the accuracy and robustness of handwritten digit recognition using a Convolutional Neural Network (CNN) architecture enhanced with Squeeze-and-Excitation (SE) blocks. The model is trained on the EMNIST Digit Dataset, which contains handwritten digits from 0 to 9, and achieves state-of-the-art performance for recognizing these digits.

## Table of Contents
- [Handwritten Digit Recognition using CNN with Squeeze-and-Excitation Blocks](#handwritten-digit-recognition-using-cnn-with-squeeze-and-excitation-blocks)
  - [Table of Contents](#table-of-contents)
  - [Project Overview](#project-overview)
  - [Features](#features)
  - [Dataset](#dataset)
  - [Model Architecture](#model-architecture)
  - [Requirements](#requirements)
  - [Evaluation](#evaluation)
  - [License](#license)

## Project Overview

Handwritten digit recognition is an important task in computer vision and pattern recognition with applications ranging from postal automation to digitizing handwritten notes. This project leverages Convolutional Neural Networks (CNN) and Squeeze-and-Excitation (SE) blocks to create a robust model that accurately identifies handwritten digits, even under challenging variations in style, size, and orientation.

## Features
- Convolutional Neural Network (CNN) with Squeeze-and-Excitation (SE) blocks to prioritize important features and improve recognition accuracy.
- Data Augmentation to improve generalization through transformations like rotation, shifting, and zooming.
- High performance on both validation and test sets, achieving perfect precision, recall, and f1-scores.
- Detailed model evaluation using confusion matrices, ROC-AUC, and Precision-Recall curves.

## Dataset

The project uses the EMNIST Digit Dataset, a subset of the Extended MNIST (EMNIST) dataset. This dataset contains:

- 280,000 training images of digits (0-9)
- 40,000 test images

Each image is a 28x28 pixel grayscale representation.

## Model Architecture

The model incorporates:

- **Input Layer**: 28x28 grayscale images.
- **Convolutional Layers**: Extracts features from images.
- **Squeeze-and-Excitation (SE) Blocks**: Dynamically recalibrates feature maps to enhance the network’s focus on important information.
- **Residual Connections**: Helps train deeper networks by solving vanishing gradient problems.
- **Pooling Layers**: Reduces dimensionality, accelerating training and preventing overfitting.
- **Fully Connected Layers**: Combines extracted features to predict digit class (0-9).
- **Output Layer**: Predicts digit class using softmax activation.

## Requirements

To run this project, you need the following libraries installed:

- Python 3.x
- TensorFlow/Keras
- NumPy
- Matplotlib
- OpenCV (for image processing)
- Google Colab (optional for cloud-based training)


## Evaluation

After training, the model is evaluated using several metrics:

- **Accuracy**: Measures overall correctness of predictions.
- **Precision, Recall, F1-Score**: Provides detailed class-by-class performance.
- **ROC-AUC and Precision-Recall Curves**: Illustrates the model’s performance in distinguishing digit classes.


## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
