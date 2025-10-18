# Traffic Sign Recognition System

This project focuses on classifying traffic signs from the German Traffic Sign Recognition Benchmark (GTSRB) dataset using deep learning. It demonstrates how computer vision and neural networks can be used to identify and understand real-world road signs - a critical component of intelligent transportation systems and autonomous vehicles.

## Table of Contents
- [Brief Overview](#brief-overview)
- [Dataset](#dataset)
- [How It Works](#how-it-works)
- [Tools & Technologies](#tools--technologies)
- [Model Performance](#model-performance)
- [Remarks](#remarks)

## Brief Overview

The goal of this project is to build and deploy a robust deep learning model capable of recognizing and classifying different types of traffic signs with high accuracy.

Using a Convolutional Neural Network (CNN) and Transfer Learning (MobileNetV2), the model is trained on thousands of labeled traffic sign images. The system includes steps for preprocessing, data augmentation, model optimization, and deployment using Streamlit for interactive testing.

While the model performs well, its accuracy might vary slightly depending on the training setup, but it remains highly reliable and efficient for most real-world scenarios.

## Dataset

The dataset used is the **GTSRB (German Traffic Sign Recognition Benchmark)**, available on Kaggle.

### Dataset Overview
- **Total Images**: Over 50,000 labeled images of German traffic signs
- **Number of Classes**: 43 unique traffic sign categories (e.g., speed limits, stop signs, warnings)
- **Image Type**: Color images (RGB)
- **File Format**: .ppm or .png files depending on the version
- **Variability**: The dataset includes images taken under different lighting conditions, perspectives, and partial occlusions, providing a realistic variety of real-world scenarios

## How It Works

### Data Pipeline
1. **Data Loading**: Reads all images from the dataset folder and extracts corresponding class labels
2. **Preprocessing**:
   - Converts images from BGR to RGB
   - Resizes them to a fixed shape (e.g., 48×48 pixels)
   - Normalizes pixel values between 0 and 1
   - Encodes labels into one-hot vectors
3. **Data Splitting**: Divides the data into training and test sets
4. **Augmentation**: Applies transformations (rotation, zoom, flips) for improved generalization

### Model Training
- Custom CNN and MobileNetV2 architectures are trained using Adam optimizer
- Model checkpoints, early stopping, and learning rate reduction are applied
- **Evaluation**: Measures accuracy, precision, recall, and F1-score
- A confusion matrix helps visualize per-class performance

### Deployment
- The trained model is saved and used in a Streamlit app
- Allows users to upload a traffic sign image for real-time prediction

## Tools & Technologies

- **Programming Language**: Python
- **Deep Learning Frameworks**: TensorFlow / Keras
- **Computer Vision**: OpenCV
- **Data Processing**: NumPy, Pandas
- **Visualization**: Matplotlib, Seaborn
- **Machine Learning Utilities**: scikit-learn
- **Deployment**: Streamlit / pyngrok

## Model Performance

After hyperparameter tuning and data augmentation, the optimized CNN achieved strong results:

| Metric | Score |
|--------|-------|
| **Accuracy** | ~98% |
| **Precision** | ~97% |
| **Recall** | ~96% |
| **F1-Score** | ~96% |

*Performance may vary based on training time and GPU availability, but the results remain consistent and robust across multiple runs.*

## Remarks

This project showcases how deep learning can be effectively applied to real-world image classification tasks. The trained model performs with strong accuracy and stability, making it a reliable starting point for any traffic sign recognition system.

Although performance might slightly vary depending on training time and hardware, it remains a robust and practical solution for most use cases. The modular design allows for easy integration into larger autonomous systems or traffic monitoring applications.
