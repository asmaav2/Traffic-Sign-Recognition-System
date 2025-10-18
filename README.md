# Traffic-Sign-Recognition-System
This project focuses on classifying traffic signs from the German Traffic Sign Recognition Benchmark (GTSRB) dataset using deep learning. It demonstrates how computer vision and neural networks can be used to identify and understand real-world road signs a critical component of intelligent transportation systems and autonomous vehicles.

## Table Of Content
#brief[Brief]
#dataset[Dataset]
#how_it_works[How_It_Works]
#tools[Tools]
#model_performance[Model_Performance]
#remarks[Remarks]

## Brief
The goal of this project is to build and deploy a robust deep learning model capable of recognizing and classifying different types of traffic signs with high accuracy.

Using a Convolutional Neural Network (CNN) and Transfer Learning (MobileNetV2), the model is trained on thousands of labeled traffic sign images. The system includes steps for preprocessing, data augmentation, model optimization, and deployment using Streamlit for interactive testing.

While the model performs well, its accuracy might vary slightly depending on the training setup — but it remains highly reliable and efficient for most real-world scenarios.

## Dataset
The dataset used is the GTSRB (German Traffic Sign Recognition Benchmark), available on Kaggle.

## Overview
Total Images: Over 50,000 labeled images of German traffic signs.
Number of Classes: 43 unique traffic sign categories (e.g., speed limits, stop signs, warnings).
Image Type: Color images (RGB).
File Format: .ppm or .png files depending on the version.
Variability: The dataset includes images taken under different lighting conditions, perspectives, and partial occlusions providing a realistic variety of real-world scenarios.



## How_It_Works
Data Loading: Reads all images from the dataset folder and extracts corresponding class labels.
Preprocessing:
Converts images from BGR to RGB.
Resizes them to a fixed shape (e.g., 48x48).
Normalizes pixel values between 0 and 1.
Encodes labels into one-hot vectors.
Data Splitting: Divides the data into training and test sets.
Augmentation: Applies transformations (rotation, zoom, flips) for improved generalization.
Model Training:
Custom CNN and MobileNetV2 architectures are trained using Adam optimizer.
Model checkpoints, early stopping, and learning rate reduction are applied.
Evaluation: Measures accuracy, precision, recall, and F1-score. A confusion matrix helps visualize per-class performance.
Deployment: The trained model is saved and used in a Streamlit app that allows users to upload a traffic sign image for prediction.


## Tools
Python
TensorFlow / Keras
OpenCV
NumPy, Pandas
Matplotlib, Seaborn
scikit-learn
Streamlit / pyngrok

## Model_Performance
After hyperparameter tuning and data augmentation, the optimized CNN achieved strong results:

Accuracy: ~98%
Precision: ~97%
Recall: ~96%
F1-Score: ~96% Performance may vary based on training time and GPU availability, but the results remain consistent and robust across multiple runs.


## Remarks
This project showcases how deep learning can be effectively applied to real-world image classification tasks. The trained model performs with strong accuracy and stability, making it a reliable starting point for any traffic sign recognition system. Although performance might slightly vary depending on training time and hardware, it remains a robust and practical solution for most use cases.

