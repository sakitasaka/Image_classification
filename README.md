# Rock Paper Scissors Image Classification

## Overview

This project focuses on building a neural network to classify images of hands in rock, paper, or scissors forms. The dataset used for this project includes diverse images of hands created using CGI techniques, with a resolution of 300x300 pixels.

## Dataset

The dataset can be found on Kaggle: [Rock Paper Scissors Dataset](https://www.kaggle.com/datasets/sanikamal/rock-paper-scissors-dataset). It comprises hands in "rock," "paper," or "scissors" forms, with individuals of various races, ages, and genders.

### Data Processing

- The dataset has been split into training, development (dev), and test sets.
- Images have been normalized to values between 0 and 1.

## Model Architecture

The initial model is built using Keras and TensorFlow, with the following architecture:

```plaintext
Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d (Conv2D)              (None, 298, 298, 32)      896       
_________________________________________________________________
max_pooling2d (MaxPooling2D) (None, 149, 149, 32)      0         
_________________________________________________________________
conv2d_1 (Conv2D)            (None, 147, 147, 64)      18496     
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 73, 73, 64)        0         
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 71, 71, 128)       73856     
_________________________________________________________________
max_pooling2d_2 (MaxPooling2 (None, 35, 35, 128)       0         
_________________________________________________________________
flatten (Flatten)            (None, 156800)            0         
_________________________________________________________________
dense (Dense)                (None, 128)               20070528  
_________________________________________________________________
dropout (Dropout)            (None, 128)               0         
_________________________________________________________________
dense_1 (Dense)              (None, 3)                 387       
=================================================================
Total params: 20,166,163
Trainable params: 20,166,163
Non-trainable params: 0
Training

The model is trained using the Adam optimizer and categorical crossentropy loss. You can find the training code in train_model.ipynb.

Model Improvements

The following improvements can be considered:

Weight Initialization Methods
Regularization: L2, Dropout
Mini-Batch Gradient Descent
Gradient Descent Optimization Algorithm: Momentum, RMSProp, Adam
Batch Normalization
Feel free to experiment and contribute to enhancing the model's performance.

Usage

To use the model for inference, you can load the trained model weights and make predictions. Example code can be found in predict_example.ipynb.

License

This project is licensed under the MIT License.

Acknowledgments

Kaggle for providing the Rock Paper Scissors Dataset.
TensorFlow and Keras for making deep learning accessible.
Feel free to reach out if you have any questions or suggestions!
