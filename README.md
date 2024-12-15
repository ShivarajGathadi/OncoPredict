# OncoPredict: Breast Cancer Detection System

**OncoPredict** is a machine learning-based system designed to classify breast cancer tumors as either malignant (cancerous) or benign (non-cancerous). Using the Wisconsin Breast Cancer dataset, this project aims to provide early detection and support medical professionals in diagnosing breast cancer with high accuracy.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Models Implemented](#models-implemented)
  - [Custom Logistic Regression](#custom-logistic-regression)
  - [Sklearn Logistic Regression](#sklearn-logistic-regression)
  - [Deep Neural Network (Keras)](#deep-neural-network-keras)
- [Key Steps](#key-steps)
  - [Data Preprocessing](#data-preprocessing)
  - [Model Implementation](#model-implementation)
- [Use Case](#use-case)
- [Installation](#installation)
- [Requirements](#requirements)
- [License](#license)

## Overview

OncoPredict aims to assist in the early detection of breast cancer by analyzing various features of breast cell nuclei, obtained from biopsy samples. The project uses machine learning models to classify the tumors into two categories: **malignant** and **benign**. This system helps reduce manual diagnostic errors and provides a quick preliminary screening tool for medical professionals.

## Dataset

The project uses the **Wisconsin Breast Cancer dataset**, which contains 30 features for each sample, including:
- **Cell radius**
- **Texture**
- **Perimeter**
- **Area**
- **Smoothness**
- **Compactness**
- **Concavity**
- **Symmetry**
- **Fractal dimension**

These features are extracted from cell nuclei images and used to predict the nature of the tumor.

## Models Implemented

### Custom Logistic Regression
- Built from scratch without using `sklearn` or any other machine learning library.
- Uses the **sigmoid activation function** for binary classification.
- Implements **gradient descent** to optimize the model and minimize error.
- Achieved **97.36% accuracy** on test data.

### Sklearn Logistic Regression
- Standard logistic regression from the `sklearn` library used for benchmarking purposes.
- Achieved **96.49% accuracy** on test data.

### Deep Neural Network (Keras)
- A neural network architecture with:
  - **Input layer**: 30 neurons (one for each feature, using sigmoid activation).
  - **Hidden layers**:
    - 100 neurons with **tanh activation**.
    - 200 neurons with **ReLU activation**.
    - 100 neurons with **ReLU activation**.
  - **Output layer**: 1 neuron with **sigmoid activation**.
- Achieved **93.86% accuracy** on test data.

## Key Steps

### Data Preprocessing
- **Loading and cleaning** the dataset.
- **Feature scaling** using **MinMaxScaler** to normalize the data and improve model performance.
- **Train-test splitting** to create separate datasets for training and testing the models.

### Model Implementation
- **Custom Logistic Regression**:
  - Forward and backward propagation to compute the output and adjust weights.
  - Gradient descent for optimizing the model.
- **Prediction Function**:
  - After training, the model predicts whether a tumor is malignant or benign based on new data.

## Use Case

OncoPredict is designed to be used as:
- A tool for **early detection** of breast cancer.
- A way to **reduce diagnostic errors** by providing an AI-based second opinion.
- A **quick preliminary screening** tool to assist medical professionals in their diagnosis.

With high accuracy rates (93-97%), this system can be a valuable asset in clinical settings. However, it should be used alongside other diagnostic methods for optimal results.
