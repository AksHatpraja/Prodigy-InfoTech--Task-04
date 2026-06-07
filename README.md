# Prodigy-InfoTech-Task-04
Prodigy InfoTech- Task-04

# 🚀 Project Overview: Hand Gesture Recognition Model

The **Hand Gesture Recognition Model** was developed as part of **Internship Task-04 at ProDigy InfoTech**. The objective of this project was to build a deep learning-based computer vision system capable of recognizing and classifying different hand gestures from image data. Hand gesture recognition is an important application of Artificial Intelligence that enables more natural human-computer interaction and has potential use cases in virtual reality, gaming, sign language interpretation, robotics, and touchless control systems.

## 📌 Project Objective

The primary goal of this project was to create an accurate and efficient image classification model that can automatically identify different hand gestures from input images. By leveraging Convolutional Neural Networks (CNNs), the model learns meaningful visual patterns and features from gesture images and predicts the correct gesture category with high accuracy.

## 📂 Dataset Preparation and Preprocessing

The project utilizes the **LeapGestRecog dataset**, which contains thousands of hand gesture images belonging to multiple gesture classes. Proper preprocessing was performed before training the model to ensure optimal performance.

### Data Preprocessing Steps:

* Loaded images from the LeapGestRecog dataset directory.
* Processed images using OpenCV.
* Resized all images to a uniform size of **64 × 64 pixels**.
* Converted images from BGR format to RGB format.
* Normalized pixel values to a range between 0 and 1.
* Converted image arrays to float32 format for efficient computation.
* Encoded gesture labels using LabelEncoder.
* Applied one-hot encoding to prepare labels for multi-class classification.
* Split the dataset into:

  * **80% Training Data**
  * **20% Testing Data**
* Used a fixed random state to ensure reproducible results.

These preprocessing techniques helped improve training efficiency and ensured consistency across the dataset.

## 🧠 Deep Learning Model Architecture

A **Convolutional Neural Network (CNN)** was designed and implemented using TensorFlow and Keras. CNNs are highly effective for image classification tasks because they automatically learn spatial features and patterns from image data.

### Model Components

### 1. Feature Extraction Layers

The model consists of three convolutional blocks:

#### First Convolution Block

* Conv2D Layer with 32 filters
* ReLU activation function
* MaxPooling2D layer with pool size (2×2)

#### Second Convolution Block

* Conv2D Layer with 64 filters
* ReLU activation function
* MaxPooling2D layer with pool size (2×2)

#### Third Convolution Block

* Conv2D Layer with 128 filters
* ReLU activation function
* MaxPooling2D layer with pool size (2×2)

These layers automatically learn important visual features such as edges, shapes, textures, and gesture patterns.

### 2. Classification Layers

After feature extraction:

* Flatten layer converts feature maps into a one-dimensional vector.
* Dense layer with 128 neurons and ReLU activation learns complex relationships between extracted features.
* Dropout layer with a rate of 0.5 reduces overfitting and improves model generalization.
* Final Dense layer with Softmax activation generates probability scores for each gesture class.

## ⚙️ Training Configuration

The model was compiled and trained using the following configuration:

### Optimizer

* Adam Optimizer
* Learning Rate: 0.001

### Loss Function

* Categorical Crossentropy

### Training Parameters

* Epochs: 10
* Batch Size: 32

The Adam optimizer helped achieve faster convergence while maintaining stable learning throughout the training process.

## 📈 Model Training Process

During training, the CNN gradually learned distinguishing features of different hand gestures. Accuracy improved significantly with each epoch while the loss continuously decreased.

Although some OpenCV warnings appeared due to unreadable image paths within specific dataset folders, the training process continued successfully without affecting overall model performance.

The training and validation curves demonstrated:

* Rapid learning during early epochs.
* Stable convergence across training iterations.
* Consistently high validation accuracy.
* Minimal signs of overfitting.

## 🎯 Model Performance and Results

The final model achieved outstanding classification performance.

### Performance Summary

* Successfully completed all 10 training epochs.
* Achieved near-zero training loss.
* Reached 100% training accuracy.
* Achieved 100% test accuracy on the evaluation dataset.
* Generated highly stable validation accuracy throughout training.

### Accuracy Analysis

The accuracy graph showed that:

* Training accuracy rapidly increased toward 100%.
* Validation accuracy closely followed training accuracy.
* Performance remained stable across all epochs.
* The model effectively learned gesture patterns without significant performance fluctuations.

## 💾 Model Export and Deployment Readiness

After successful training and evaluation, the trained CNN model was saved locally as:

**hand_gesture_model.keras**

Saving the model allows future use for:

* Real-time gesture recognition applications.
* Webcam-based gesture control systems.
* Human-computer interaction projects.
* Sign language recognition systems.
* AI-powered touchless interfaces.

## 🔍 Skills and Technologies Applied

### Programming Language

* Python

### Libraries and Frameworks

* TensorFlow
* Keras
* OpenCV
* NumPy
* Scikit-learn
* Matplotlib

### Machine Learning Concepts

* Deep Learning
* Convolutional Neural Networks (CNN)
* Image Classification
* Feature Extraction
* Data Preprocessing
* Model Evaluation
* Multi-Class Classification

## 🏆 Conclusion

This project successfully demonstrates the power of Deep Learning and Computer Vision in solving real-world image classification problems. By implementing a CNN-based architecture, the model was able to accurately recognize hand gestures and achieve exceptional performance. The project provided valuable hands-on experience in image preprocessing, neural network design, model training, evaluation, and deployment preparation, making it an important step toward building advanced AI-powered vision applications.
