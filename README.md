Image Recognition and Classification using Keras in R

Project Objective

The objective of this project is to implement a basic image recognition and classification system in R using Keras and TensorFlow. The model classifies images into two categories: airplanes and cars.

Problem Description

The project demonstrates a fundamental computer-vision machine-learning workflow:

Collect and inspect a small image dataset.

Read the images using the EBImage package.

Preprocess the images into a common format.

Prepare training and testing datasets.

Convert class labels into categorical form.

Build a sequential neural-network model using Keras.

Train the model and validate its performance.

Generate predictions for training and unseen test images.

Evaluate the results using accuracy and confusion matrices.

Dataset

The project uses 12 images:

p1.jpg to p6.jpg — airplane images

c1.jpg to c6.jpg — car images

The labels are:

0 = Airplane

1 = Car

The notebook uses the first five airplane images and first five car images for training, giving 10 training images. The sixth airplane and sixth car images are used as the 2 test images.

The notebook also includes image conversion/preprocessing steps so that the images can be handled consistently.

Technologies and Packages

R Programming

Keras

TensorFlow

EBImage

BiocManager

Main package roles

EBImage — image reading, inspection, display, and image preprocessing.

Keras — construction, compilation, training, prediction, and evaluation of the neural network.

TensorFlow — backend used for the deep-learning workflow.

Image Preprocessing

The images are read using EBImage. Since the original images can have different dimensions, the project preprocesses them into a common representation suitable for the neural network.

The model uses an input size of:

28 × 28 × 3 = 2352 values per image

The image data is reshaped into numerical vectors before being supplied to the dense neural-network layers.

Neural Network Architecture

The project uses a Keras sequential neural network with the following architecture:

Input: 2352
   |
Dense: 256 units
Activation: ReLU
   |
Dense: 128 units
Activation: ReLU
   |
Dense: 2 units
Activation: Softmax

The model is compiled using:

Loss: binary_crossentropy

Optimizer: RMSProp

Metric: Accuracy

Model Training

The model is trained with:

Epochs: 30

Batch size: 32

Validation split: 20%

Results

Training Results

The notebook records:

Accuracy: 90%

Loss: 0.266763

The training confusion matrix is:

         Actual
Predicted 0 1
        0 5 1
        1 0 4

This means 9 out of 10 training images were classified correctly.

Test Results

The model predicts the two unseen test images as:

[1] 0 1

This corresponds to:

Airplane → 0

Car → 1

The testing confusion matrix is:

         Actual
Predicted 0 1
        0 1 0
        1 0 1

Thus, both test images were classified correctly, giving 100% accuracy on the two-image test set.

How to Run

Open the notebook:

23102A0061_R_Image_Recognition_&_Classification_using_keras_in_R.ipynb

Run it using an R environment that supports Keras/TensorFlow and EBImage.

Make sure the required image files are available to the notebook:

p1.jpg to p6.jpg

c1.jpg to c6.jpg

Install/load the required R packages when necessary.

Execute the notebook cells in order.

Verify the model training, predictions, accuracy, and confusion matrices.

Project Files

The main implementation is provided in:

23102A0061_R_Image_Recognition_&_Classification_using_keras_in_R.ipynb

Version Control

This project is maintained using Git and GitHub. The repository contains the R programming work and the image-recognition/classification notebook.

Reference

This implementation follows the prescribed project tutorial specified in the assignment.

Student

Name: Sahil Ghogare
Roll Number: 23102A0061
