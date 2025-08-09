# Snake Gourd Leaf Disease Classification

This project uses a Convolutional Neural Network (CNN) to classify images of snake gourd leaves into three categories: Anthracnose, Healthy, and Yellow. The model is built using TensorFlow and Keras, and it achieves high accuracy in identifying leaf diseases.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Evaluation](#evaluation)

## Project Overview
The goal of this project is to classify snake gourd leaves into three categories based on their health status:
1. **Anthracnose**: A fungal disease causing dark, sunken lesions.
2. **Healthy**: Leaves with no visible disease symptoms.
3. **Yellow**: Leaves showing yellowing, often due to nutrient deficiencies or other stress factors.

The model is trained on a dataset of labeled images and can be used to predict the health status of new leaf images.

## Dataset
The dataset consists of three classes:
- **Train**: 1260 images (420 per class)
- **Validation**: 180 images (60 per class)
- **Test**: 360 images (120 per class)

The images are resized to 224x224 pixels and normalized for training.

## Model Architecture
The CNN model consists of the following layers:
1. **Convolutional Layers**: Three layers with 32, 64, and 128 filters, respectively, using ReLU activation.
2. **MaxPooling Layers**: After each convolutional layer to reduce spatial dimensions.
3. **Flatten Layer**: To convert the 3D output to 1D.
4. **Dense Layers**: One hidden layer with 128 neurons and ReLU activation, followed by a dropout layer (0.5 rate) to prevent overfitting.
5. **Output Layer**: Softmax activation for multi-class classification.

## Training
The model was trained for 10 epochs with the following parameters:
- **Batch Size**: 32
- **Optimizer**: Adam
- **Loss Function**: Categorical Crossentropy
- **Metrics**: Accuracy

### Training Results
- **Training Accuracy**: ~93%
- **Validation Accuracy**: ~89%
- **Test Accuracy**: ~88%

## Evaluation
The model's performance was evaluated using:
- **Classification Report**: Shows precision, recall, and F1-score for each class.
- **Confusion Matrix**: Visualizes the model's predictions vs. actual labels.
![Confusion Matrix of this code.](https://i.postimg.cc/Wbm5mX7g/output.png)
