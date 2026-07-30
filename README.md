# Image Classification of Cats and Dogs using Convolutional Neural Networks (CNN)

## Student Information

**Name:** Gargee Singh

**Registration Number:** 23BCE11449

**Application Number:** IN26011964

**Email ID:** gargee.23bce1449@vitbhopal.ac.in

---

# Project Objective

The aim of this project is to build a Convolutional Neural Network (CNN) model capable of automatically classifying pet images into two categories: **Cats** and **Dogs**. The model is implemented using TensorFlow/Keras and demonstrates how deep learning can be applied to image classification problems.

---

# Dataset

**Dataset Source:**

https://www.kaggle.com/datasets/bhavikjikadara/dog-and-cat-classification-dataset

The dataset consists of RGB images belonging to two classes:
- Cats
- Dogs

It contains nearly 25,000 images, with an equal number of samples from both categories.

---

# Technologies and Libraries

The following Python libraries were used during implementation:

- Python
- NumPy
- Pandas
- Matplotlib
- TensorFlow
- Keras
- Scikit-learn
- Pillow (PIL)
- Kaggle API

---

# Project Workflow

## 1. Dataset Exploration

- Downloaded the dataset from Kaggle.
- Examined the directory structure.
- Displayed sample images from both categories.
- Verified the class distribution.

## 2. Data Preprocessing

The dataset was prepared before training by performing the following steps:

- Removed unreadable or corrupted image files.
- Resized every image to **128 × 128 pixels**.
- Normalized pixel values between **0 and 1**.
- Split the dataset into:
  - **80% Training Data**
  - **20% Testing Data**
- Loaded images efficiently using **ImageDataGenerator**.

---

# CNN Model Architecture

The CNN model consists of three convolutional blocks followed by fully connected layers.

### Layer 1
- Conv2D
- 32 Filters
- 3×3 Kernel
- ReLU Activation
- MaxPooling (2×2)

### Layer 2
- Conv2D
- 64 Filters
- 3×3 Kernel
- ReLU Activation
- MaxPooling (2×2)

### Layer 3
- Conv2D
- 128 Filters
- 3×3 Kernel
- ReLU Activation
- MaxPooling (2×2)

### Fully Connected Layers

- Flatten Layer
- Dense Layer (128 neurons, ReLU)
- Output Layer (1 neuron, Sigmoid)

---

# Model Configuration

- **Optimizer:** Adam
- **Loss Function:** Binary Crossentropy
- **Evaluation Metrics:** Accuracy
- **Epochs:** 10

---

# Model Summary

| Layer | Output Shape | Parameters |
|--------|--------------|-----------:|
| Conv2D (32 Filters) | (126,126,32) | 896 |
| MaxPooling2D | (63,63,32) | 0 |
| Conv2D (64 Filters) | (61,61,64) | 18,496 |
| MaxPooling2D | (30,30,64) | 0 |
| Conv2D (128 Filters) | (28,28,128) | 73,856 |
| MaxPooling2D | (14,14,128) | 0 |
| Flatten | (25088) | 0 |
| Dense (128) | (128) | 3,211,392 |
| Dense (1) | (1) | 129 |

---

# Performance

The trained CNN achieved the following performance on the test dataset:

| Metric | Value |
|---------|-------|
| Test Accuracy | **85.20%** |
| Test Loss | **0.7194** |
| Precision | **84.43%** |
| Recall | **86.32%** |
| F1-Score | **85.36%** |

---

# Conclusion

This project demonstrates the effectiveness of Convolutional Neural Networks for binary image classification. The model successfully learns visual features from cat and dog images and achieves an accuracy of **85.20%** on unseen test data.

Future improvements may include:

- Applying data augmentation
- Adding Dropout layers
- Using Batch Normalization
- Increasing training epochs
- Performing hyperparameter tuning
- Implementing transfer learning with pretrained CNN models such as VGG16, ResNet, or MobileNet for improved accuracy.

---

# Repository Contents

```
Assignment-8.ipynb
README.md
dataset/
```

---

Thank you.
