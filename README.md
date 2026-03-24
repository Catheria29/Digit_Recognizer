# Digit_Recognizer
 ** MNIST MLP Classification **

This project implements a Multi-Layer Perceptron (MLP) using TensorFlow/Keras to classify handwritten digits from the MNIST dataset.

 Overview

The goal of this project is to build a simple neural network that can recognize digits (0–9) from grayscale images (28×28 pixels). The model is trained and evaluated using the well-known MNIST dataset.

 Features
Loads and preprocesses MNIST dataset
Normalizes pixel values for better training
Flattens images into vectors (784 features)
Builds a fully connected neural network (MLP)
Uses Dropout for regularization
Trains and evaluates the model
Reports accuracy on test data
 Technologies Used
Python
NumPy
Matplotlib
TensorFlow / Keras
 Project Structure
MNIST_MLP_Classification.ipynb
README.md
 Model Architecture

The neural network consists of:

Input Layer: 784 neurons (28×28 flattened image)
Hidden Layer 1: 256 neurons (ReLU activation)
Dropout Layer: 20%
Hidden Layer 2: 128 neurons (ReLU activation)
Dropout Layer: 20%
Output Layer: 10 neurons (Softmax activation)
Data Preprocessing
Convert data type to float32
Normalize pixel values to range [0, 1]
Reshape images from (28, 28) → (784,)
Training
Optimizer: Adam
Loss Function: Sparse Categorical Crossentropy
Metrics: Accuracy
Epochs: 5
Batch Size: 128
Validation Split: 10%
Evaluation

After training, the model is evaluated on the test dataset:

test_loss, test_acc = model.evaluate(x_test, y_test)
print(test_loss, test_acc)
How to Run

Open the notebook in Google Colab or Jupyter:

jupyter notebook MNIST_MLP_Classification.ipynb
Run all cells:
Load dataset
Preprocess data
Build model
Train model
Evaluate performance
 Expected Results
Test accuracy typically reaches ~97–98% with this architecture.
 Future Improvements
Add Convolutional Neural Networks (CNNs)
Hyperparameter tuning
Data augmentation
Early stopping
Learning rate scheduling
📚 References
MNIST Dataset
TensorFlow Documentation
