# Object Detection Using YOLO Algorithm

A professional educational implementation of an **object-detection pipeline inspired by YOLO**, built with TensorFlow, NumPy, OpenCV, and Matplotlib.

> **Important technical note:** This repository currently implements a **YOLO-like CNN for learning purposes**, not an official YOLOv1/v2/v3/v4/v5/v8/v11 model. It creates a synthetic dataset containing one rectangular object per image, predicts one bounding box plus one class value, and evaluates predictions using Intersection over Union (IoU).

## Project Overview

Object detection combines two tasks:

1. **Localization** — determining where an object is located using a bounding box.
2. **Classification** — identifying the class of the detected object.

This project demonstrates the core learning concepts behind a YOLO-style object detector using a small convolutional neural network.

## Main Features

- Synthetic image and bounding-box dataset generation.
- Normalized YOLO-style bounding-box representation.
- Image visualization with Matplotlib.
- 80/20 train-test split.
- CNN-based bounding-box regression.
- TensorFlow/Keras model training.
- Test-set loss evaluation.
- Intersection over Union (IoU) calculation.
- Prediction comparison between true and predicted boxes.

## Technologies

- Python
- TensorFlow / Keras
- NumPy
- OpenCV
- Matplotlib

## Project Structure

```text
Object-Detection-Using-YOLO-Algorithm/
│
├── object_detection_using_yolo_algorithm.py
├── README.md
├── requirements.txt
├── .gitignore
│
└── docs/
    ├── PROJECT_REPORT.md
    ├── TECHNICAL_DOCUMENTATION.md
    └── USER_GUIDE.md
```

## Dataset

The project generates the dataset programmatically, so an external dataset is not required.

Each generated image:

- Has a size of `128 × 128 × 3`.
- Starts as a black image.
- Contains one randomly positioned white rectangle.
- Stores the bounding box as:

```text
[x_center, y_center, width, height, class]
```

The first four values are normalized by `IMAGE_SIZE`, and the class value is `1`.

## Model Architecture

The CNN contains:

- Conv2D: 16 filters
- MaxPooling2D
- Conv2D: 32 filters
- MaxPooling2D
- Conv2D: 64 filters
- MaxPooling2D
- Flatten
- Dense: 128 neurons
- Dense: 5 output values

The five outputs represent:

```text
x_center, y_center, width, height, class
```

The model uses the Adam optimizer and mean squared error (MSE) loss.

## How to Run

### 1. Open the project folder

On Windows:

```text
C:\Users\ABDULLAH SHAHEER\OneDrive\Desktop\Object Detection Using YOLO Algorithm
```

### 2. Create a virtual environment (recommended)

```bash
python -m venv .venv
```

Activate it:

```bash
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 4. Run the program

```bash
python object_detection_using_yolo_algorithm.py
```

## Expected Workflow

```text
Synthetic Dataset
       ↓
Image + Bounding Box Labels
       ↓
Normalization
       ↓
Train/Test Split
       ↓
CNN Model
       ↓
Training
       ↓
Test Loss
       ↓
Bounding-Box Predictions
       ↓
IoU Evaluation
```

## Evaluation

The project uses **IoU (Intersection over Union)** to compare a predicted bounding box with the true bounding box:

```text
IoU = Intersection Area / Union Area
```

Higher IoU indicates greater overlap between the predicted and ground-truth boxes.

The script also prints:

- True Box
- Predicted Box
- IoU

for five test examples.

## Limitations

This educational implementation intentionally has a simplified scope:

- One object per image.
- One class.
- Synthetic data only.
- Single bounding-box output.
- No grid-cell prediction.
- No anchor boxes.
- No confidence/objectness loss.
- No Non-Maximum Suppression (NMS).
- No multi-scale detection.
- No pretrained YOLO weights.
- No real-world dataset.

Therefore, results should not be interpreted as benchmark performance of an official YOLO model.

## Future Improvements

Possible extensions include:

- Real-world annotated datasets.
- Multiple object instances.
- Multiple object classes.
- Objectness/confidence prediction.
- YOLO grid-based prediction.
- Non-Maximum Suppression.
- Data augmentation.
- Better detection-specific loss functions.
- Precision, recall, mAP, and confusion-matrix analysis.
- Webcam/video inference.
- Integration with an official modern YOLO implementation.

## Academic Purpose

This project is suitable as a learning project for understanding:

- Computer Vision
- CNNs
- Object Detection
- Bounding Boxes
- Regression
- IoU
- TensorFlow/Keras model training

## Author

**Abdullah Shaheer**

GitHub: https://github.com/abdullahshaheer901-pixel

Repository: https://github.com/abdullahshaheer901-pixel/Object-Detection-Using-YOLO-Algorithm
"# Object-Detection-Using-YOLO-Algorithm" 
