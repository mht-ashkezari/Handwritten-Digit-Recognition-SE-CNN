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
- [CNN-SE Handwritten Digit Recognition](#cnn-se-handwritten-digit-recognition)
  - [Instructions](#instructions)
  - [Usage](#usage)
  - [Example](#example)
- [Load EMNIST dataset](#load-emnist-dataset)
- [Train the model](#train-the-model)
- [Evaluate the model](#evaluate-the-model)
  - [Evaluation](#evaluation)
  - [Results](#results)
  - [Real-World Applications](#real-world-applications)
  - [Contributing](#contributing)
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

You can install the required Python packages by running:

```bash
pip install -r requirements.txt

# CNN-SE Handwritten Digit Recognition

## Instructions

1. **Clone this repository**:
    ```bash
    git clone https://github.com/yourusername/CNN-SE-Handwritten-Digit-Recognition.git
    cd CNN-SE-Handwritten-Digit-Recognition
    ```

2. **Install the necessary dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

3. **(Optional)** If you are using Google Colab, upload the project files to your Google Drive.

## Usage

1. **Prepare the Dataset**:  
   Download the EMNIST dataset and place it in the appropriate directory (or load it directly in Colab).

2. **Train the Model**:  
   Run the training script to train the CNN with SE blocks:
    ```bash
    python train_model.py
    ```

3. **Evaluate the Model**:  
   After training, evaluate the model using validation and test sets:
    ```bash
    python evaluate_model.py
    ```

## Example

```python
# Load EMNIST dataset
train_images, train_labels = load_emnist_images('path_to_training_images')
test_images, test_labels = load_emnist_labels('path_to_test_images')

# Train the model
model = train_model(train_images, train_labels)

# Evaluate the model
evaluate_model(model, test_images, test_labels)

## Evaluation

After training, the model is evaluated using several metrics:

- **Accuracy**: Measures overall correctness of predictions.
- **Precision, Recall, F1-Score**: Provides detailed class-by-class performance.
- **Confusion Matrix**: Visualizes model performance by comparing predictions to true labels.
- **ROC-AUC and Precision-Recall Curves**: Illustrates the model’s performance in distinguishing digit classes.

## Results

The model achieves perfect scores on both the validation and test sets. Key performance metrics:

- **Precision, Recall, F1-Score**: 1.00 for all classes.
- **ROC-AUC**: 1.00 across all digit classes.

## Real-World Applications

This model can be applied in various real-world scenarios, including:

- **Postal Automation**: Automatically reading handwritten postal codes or addresses.
- **Digit Recognition**: Digitizing handwritten documents or financial records.
- **Educational Tools**: Building applications that recognize student handwriting on exams or assignments.

## Contributing

Contributions are welcome! If you want to contribute to this project, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
