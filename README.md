# Deep Learning Projects: CNN & RNN

This repository contains two projects demonstrating the implementation of a Convolutional Neural Network (CNN) for image classification and a Recurrent Neural Network (RNN) for text classification.

## 1. Convolutional Neural Network (CNN)

### Project Goal

The objective of this project was to build and train a Convolutional Neural Network to classify images from the **Street View House Numbers (SVHN)** dataset. [cite_start]The model identifies the correct digit (0-9) from real-world 32x32 color images[cite: 189].

### Dataset

* [cite_start]**Name:** `svhn_cropped` [cite: 158]
* [cite_start]**Description:** A dataset of 73,257 training images [cite: 187] [cite_start]and 26,032 test images [cite: 188] [cite_start]of 10 different digits (0-9)[cite: 186].

### Model Architecture

[cite_start]The CNN was built using a Keras Sequential model with the following layers [cite: 254-274]:
* [cite_start]`Input` (shape 32x32x3) [cite: 255]
* [cite_start]`Conv2D` (32 filters, 3x3 kernel, ReLU activation) [cite: 257]
* [cite_start]`MaxPooling2D` (2x2) [cite: 257]
* [cite_start]`Dropout` (0.3) [cite: 258]
* [cite_start]`Conv2D` (64 filters, 3x3 kernel, ReLU activation) [cite: 260]
* [cite_start]`MaxPooling2D` (2x2) [cite: 261]
* [cite_start]`Dropout` (0.3) [cite: 262]
* [cite_start]`Conv2D` (128 filters, 3x3 kernel, ReLU activation) [cite: 264]
* [cite_start]`MaxPooling2D` (2x2) [cite: 265]
* [cite_start]`Dropout` (0.3) [cite: 266]
* [cite_start]`Flatten` [cite: 268]
* [cite_start]`Dense` (128 units, ReLU activation) [cite: 270]
* [cite_start]`Dropout` (0.5) [cite: 270]
* [cite_start]`Dense` (10 units, Softmax activation for output) [cite: 274]

### Results

[cite_start]The model was trained for **15 epochs** [cite: 290] and achieved the following performance on the test set:
* [cite_start]**Final Test Loss:** 0.3267 [cite: 394]
* [cite_start]**Final Test Accuracy:** 90.58% [cite: 395]

### How to Run

The complete code, training process, and results are available in the **`CNN.ipynb`** notebook. It can be opened and run in Google Colab.

---

## 2. Recurrent Neural Network (RNN)

### Project Goal

The objective of this project was to build and train a Recurrent Neural Network (using LSTM units) to perform multiclass text classification on the **AG News** dataset. [cite_start]The model classifies news headlines into one of four categories[cite: 10, 32].

### Dataset

* [cite_start]**Name:** `ag_news_subset` [cite: 10]
* [cite_start]**Description:** A dataset of 120,000 training samples [cite: 54, 76, 77] and 7,600 test samples. [cite_start]Headlines are classified into 4 categories: 'World', 'Sports', 'Business', and 'Sci/Tech'[cite: 32].

### Model Architecture

[cite_start]The model uses a `TextVectorization` layer for preprocessing and an RNN built with a Keras Sequential model with the following layers [cite: 39-43, 82-94]:
* [cite_start]`Embedding` (10,000 input vocab size, 64 output dimension) [cite: 36, 78, 84]
* [cite_start]`LSTM` (64 units) [cite: 79, 86]
* [cite_start]`Dense` (64 units, ReLU activation) [cite: 79, 88]
* [cite_start]`Dropout` (0.5) [cite: 89]
* [cite_start]`Dense` (4 units, Softmax activation for output) [cite: 94]

### Results

[cite_start]The model was trained for **10 epochs** [cite: 126] and achieved the following performance on the test set:
* [cite_start]**Final Test Loss:** 0.6165 [cite: 142]
* [cite_start]**Final Test Accuracy:** 88.36% [cite: 143]

### How to Run

The complete code, training process, and results are available in the **`RNN.ipynb`** notebook. It can be opened and run in Google Colab.
