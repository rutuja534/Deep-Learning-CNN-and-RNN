# Deep Learning Projects: CNN & RNN

This repository contains two projects demonstrating the implementation of a Convolutional Neural Network (CNN) for image classification and a Recurrent Neural Network (RNN) for text classification.

## 1. Convolutional Neural Network (CNN)

### Project Goal

The objective of this project was to build and train a Convolutional Neural Network to classify images from the **Street View House Numbers (SVHN)** dataset. The model identifies the correct digit (0-9) from real-world 32x32 color images.

### Dataset

* **Name:** `svhn_cropped`
* **Description:** A dataset of 73,257 training images and 26,032 test images of 10 different digits (0-9).

### Model Architecture

The CNN was built using a Keras Sequential model with the following layers:
* `Input` (shape 32x32x3)
* `Conv2D` (32 filters, 3x3 kernel, ReLU activation)
* `MaxPooling2D` (2x2)
* `Dropout` (0.3)
* `Conv2D` (64 filters, 3x3 kernel, ReLU activation)
* `MaxPooling2D` (2x2)
* `Dropout` (0.3)
* `Conv2D` (128 filters, 3x3 kernel, ReLU activation)
* `MaxPooling2D` (2x2)
* `Dropout` (0.3)
* `Flatten`
* `Dense` (128 units, ReLU activation)
* `Dropout` (0.5)
* `Dense` (10 units, Softmax activation for output)

### Results

The model was trained for **15 epochs** and achieved the following performance on the test set:
* **Final Test Loss:** 0.3267
* **Final Test Accuracy:** 90.58%

### How to Run

The complete code, training process, and results are available in the **`CNN.ipynb`** notebook. It can be opened and run in Google Colab.

---

## 2. Recurrent Neural Network (RNN)

### Project Goal

The objective of this project was to build and train a Recurrent Neural Network using **LSTM (Long Short-Term Memory)** units to perform text classification. This demonstrates a core technique used in NLP for sentiment analysis.

### Dataset

* **Name:** `ag_news_subset`
* **Task:** The model was trained to classify news headlines into one of four categories: 'World', 'Sports', 'Business', and 'Sci/Tech'.
* **Description:** A dataset of 120,000 training samples and 7,600 test samples.

### Model Architecture

The model uses a `TextVectorization` layer for preprocessing and an RNN built with a Keras Sequential model with the following layers:
* `Embedding` (10,000 input vocab size, 64 output dimension)
* `LSTM` (64 units)
* `Dense` (64 units, ReLU activation)
* `Dropout` (0.5)
* `Dense` (4 units, Softmax activation for output)

### Results

The model was trained for **10 epochs** and achieved the following performance on the test set:
* **Final Test Loss:** 0.6165
* **Final Test Accuracy:** 88.36%

### How to Run

The complete code, training process, and results are available in the **`RNN.ipynb`** notebook. It can be opened and run in Google Colab.
