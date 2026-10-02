# Technical Documentation

## 1. System Objective

The system demonstrates the basic pipeline of object detection using a CNN that predicts a normalized bounding box and class value from an input image.

## 2. Input Representation

The generated image has:

`IMAGE_SIZE = 128`

and three color channels:

`(128, 128, 3)`

The image is normalized by dividing pixel values by `255.0`.

## 3. Bounding-Box Representation

Each label follows:

`[x_center, y_center, width, height, class]`

The center coordinates and dimensions are normalized relative to the image size.

This representation is conceptually aligned with common YOLO-style box parameterization.

## 4. Dataset Generation

For every sample, the program creates a black image and draws one filled white rectangle using OpenCV. The rectangle position and dimensions are randomized.

The dataset function returns NumPy arrays containing images and labels.

## 5. Train/Test Split

The script uses an 80/20 split:

- 80% training data
- 20% test data

The training set is further divided internally by Keras using `validation_split=0.2`.

## 6. CNN

The model uses three convolutional blocks with increasing filter counts:

- 16 filters
- 32 filters
- 64 filters

Max pooling reduces spatial dimensions. Flatten converts the feature maps into a vector, followed by a 128-neuron dense layer.

The final dense layer contains five outputs.

## 7. Training

The model is compiled with:

- Optimizer: Adam
- Loss: Mean Squared Error

Training is performed for 10 epochs with a batch size of 32.

## 8. Evaluation

The test loss is obtained using `model.evaluate()`.

For localization quality, IoU is calculated independently.

## 9. IoU

For each box, the center-width-height representation is converted into minimum and maximum x/y coordinates.

Intersection dimensions are calculated using:

- maximum of the left/top boundaries
- minimum of the right/bottom boundaries

Intersection area is divided by union area.

## 10. Prediction

The script predicts five test samples and compares each prediction with the corresponding ground-truth box.

## 11. Technical Scope

This implementation is intentionally simplified for education. It should be described as a **YOLO-like object-detection learning implementation**, rather than an official YOLO architecture.
