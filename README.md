# English Character Recognition using Convolutional Neural Networks

![Python](https://img.shields.io/badge/Python-3.12-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Keras](https://img.shields.io/badge/Keras-CNN-red)
![License](https://img.shields.io/badge/License-MIT-green)

A deep learning project that classifies **62 English characters** (digits, uppercase letters, and lowercase letters) using a custom Convolutional Neural Network built with TensorFlow/Keras.

---

# Project Overview

This project trains a CNN capable of recognizing:

- Numbers (0-9)
- Uppercase letters (A-Z)
- Lowercase letters (a-z)

Total Classes:

**62**

The network is trained using grayscale 28×28 character images and predicts the corresponding class with a Softmax classifier.

---

# Example Predictions

> Replace these images with screenshots from your own project.

| Prediction Examples |
|--------------------|
| ![](images/prediction_examples.png) |

---

# Demo

> Replace this GIF with a recording of the model making predictions.

![](images/demo.gif)

---

# Model Architecture

![](images/architecture.png)

The model consists of:

Input (28×28×1)

↓

Conv2D

↓

Batch Normalization

↓

Max Pooling

↓

Conv2D

↓

Batch Normalization

↓

Max Pooling

↓

Flatten

↓

Dense (80)

↓

Dropout

↓

Dense (60)

↓

Dropout

↓

Dense (62 Softmax)

---

# Dataset

The model was trained using the **English Typed Font Dataset** available on Kaggle.

Dataset:

https://www.kaggle.com/datasets/munemshahriar642/english-typed-font-in-csv

The original CSV contains over **62,000** character images.

Each sample contains

- Label
- 784 grayscale pixels (28×28)

The dataset is split into

- Training set
- Testing set

and saved as

```
train.npy
test.npy
train_labels.npy
test_labels.npy
```

for faster loading.

---

# Installation

```bash
git clone https://github.com/USERNAME/English-Character-Recognition.git

cd English-Character-Recognition

pip install -r requirements.txt
```

---

# Training

Run

```bash
python src/train.py
```

---

# Predicting

Run

```bash
python src/predict.py
```

---

# Results

| Metric | Value |
|---------|-------|
| Classes | 62 |
| Image Size | 28×28 |
| Optimizer | Adam |
| Loss | Sparse Categorical Crossentropy |
| Activation | ReLU |
| Output | Softmax |

Replace this table with your final metrics after training.

---

# Training Curves

## Accuracy

![](images/training_accuracy.png)

## Loss

![](images/training_loss.png)

---

# Confusion Matrix

![](images/confusion_matrix.png)

---

# Sample Dataset

![](images/sample_dataset.png)

---

# Project Pipeline

![](images/pipeline.png)

```
CSV Dataset

↓

NumPy Conversion

↓

Train/Test Split

↓

CNN Training

↓

Saved Model (.keras)

↓

Prediction

↓

Visualization
```

---

# Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-Learn

---

# Future Improvements

- Improve CNN architecture
- Hyperparameter tuning
- Data augmentation
- Support handwritten characters
- Export to TensorFlow Lite
- Real-time webcam recognition
- Object detection for full-page OCR
- Deploy as a web application
