# Project Report
## Object Detection Using YOLO Algorithm

### Abstract

This project presents an educational implementation of an object-detection pipeline inspired by the YOLO approach. The system uses TensorFlow/Keras to build a convolutional neural network that learns to predict a normalized bounding box and a class value from synthetic images. OpenCV is used to generate the rectangular objects, NumPy handles numerical data, and Matplotlib is used for visualization.

The project demonstrates the fundamental relationship between image processing, convolutional neural networks, bounding-box regression, and Intersection over Union (IoU). Because the implementation uses synthetic single-object images and a simplified CNN output, it is intended for educational understanding rather than comparison with production YOLO models.

### 1. Introduction

Object detection is a computer-vision task that identifies objects and determines their locations in an image. Unlike image classification, which produces a class for an entire image, object detection also predicts spatial information.

YOLO (You Only Look Once) is a family of object-detection methods designed around direct prediction from an image. This project uses a simplified YOLO-like learning setup to demonstrate the central idea of predicting bounding-box coordinates together with a class value.

### 2. Problem Statement

The objective is to build a small neural-network pipeline that can:

1. Generate synthetic object-detection data.
2. Represent each object using a normalized bounding box.
3. Train a CNN to predict bounding-box values.
4. Evaluate the trained model.
5. Measure bounding-box overlap using IoU.

### 3. Objectives

- Understand object-detection data representation.
- Practice bounding-box coordinate normalization.
- Build a CNN using TensorFlow/Keras.
- Train a regression-style object-detection model.
- Implement IoU manually.
- Compare predicted and ground-truth boxes.

### 4. Tools and Technologies

| Technology | Purpose |
|---|---|
| Python | Programming language |
| TensorFlow/Keras | CNN and model training |
| NumPy | Numerical arrays and dataset handling |
| OpenCV | Synthetic rectangle generation |
| Matplotlib | Image visualization |

### 5. Methodology

The complete workflow is:

**Dataset Generation → Label Creation → Normalization → Train/Test Split → CNN Construction → Training → Evaluation → Prediction → IoU Calculation**

### 6. Dataset Generation

The program creates 200 samples by default. Each sample is a 128×128 RGB image containing one randomly positioned filled white rectangle on a black background.

The corresponding label is:

`[x_center, y_center, width, height, class]`

The coordinates and dimensions are normalized relative to the image size.

### 7. Model Architecture

The model consists of:

| Layer | Configuration |
|---|---|
| Conv2D | 16 filters, 3×3 kernel, ReLU |
| MaxPooling2D | Default pooling |
| Conv2D | 32 filters, 3×3 kernel, ReLU |
| MaxPooling2D | Default pooling |
| Conv2D | 64 filters, 3×3 kernel, ReLU |
| MaxPooling2D | Default pooling |
| Flatten | Feature-vector conversion |
| Dense | 128 neurons, ReLU |
| Dense | 5 outputs, sigmoid |

The five output values correspond to the bounding-box parameters and class value.

### 8. Training Configuration

The model uses:

- Adam optimizer
- MSE loss
- 10 epochs
- Batch size of 32
- 20% validation split from the training data

### 9. Evaluation

The script evaluates the model on the held-out test set and prints the test loss. It then predicts five test examples and calculates IoU for each prediction.

No fixed numerical performance value is reported here because the actual value depends on executing the program.

### 10. IoU

Intersection over Union measures overlap between two bounding boxes:

`IoU = Intersection Area / Union Area`

An IoU of 0 means no overlap, while a value approaching 1 indicates very high overlap.

### 11. Results

The source code is designed to print the true bounding box, predicted bounding box, and IoU for five test examples.

The project documentation intentionally does not invent accuracy, IoU, loss, or training-time values. These should be recorded from an actual run.

### 12. Limitations

- Synthetic dataset.
- One object per image.
- One class.
- Simplified CNN.
- No confidence/objectness score.
- No grid-based multi-object prediction.
- No Non-Maximum Suppression.
- No official YOLO pretrained model.
- No real-world benchmark dataset.
- No mAP/precision/recall evaluation.

### 13. Future Work

The system can be extended with real annotated datasets, multiple classes, multiple objects, confidence prediction, NMS, data augmentation, detection-specific losses, mAP evaluation, and webcam/video inference.

### 14. Conclusion

This project provides a compact educational demonstration of the major components involved in object detection: image preparation, bounding-box labels, CNN feature extraction, regression-style prediction, model evaluation, and IoU measurement.

Its simplified design makes it useful for understanding the concepts before moving to complete production-grade YOLO implementations.

### 15. Repository

GitHub:
https://github.com/abdullahshaheer901-pixel/Object-Detection-Using-YOLO-Algorithm

Author:
Abdullah Shaheer
