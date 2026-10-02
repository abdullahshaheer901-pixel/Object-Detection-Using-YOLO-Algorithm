# User Guide

## Windows Project Location

Place the project at:

`C:\Users\ABDULLAH SHAHEER\OneDrive\Desktop\Object Detection Using YOLO Algorithm`

## Installation

Open Command Prompt or PowerShell inside the project folder and run:

```bash
python -m venv .venv
.venv\Scripts\activate
python -m pip install -r requirements.txt
```

## Run

```bash
python object_detection_using_yolo_algorithm.py
```

## What You Will See

The program will:

1. Generate the synthetic dataset.
2. Display one sample image.
3. Build the CNN.
4. Print the model summary.
5. Train for 10 epochs.
6. Evaluate test loss.
7. Predict five test samples.
8. Print true boxes, predicted boxes, and IoU values.

## Troubleshooting

### TensorFlow is not installed

Run:

```bash
python -m pip install tensorflow
```

### OpenCV import error

Run:

```bash
python -m pip install opencv-python
```

### Matplotlib import error

Run:

```bash
python -m pip install matplotlib
```

### NumPy import error

Run:

```bash
python -m pip install numpy
```

## Reproducibility

The current source generates random rectangles and does not set a random seed. Therefore, generated samples and numerical results can differ between runs.

## Important Note

This project should be presented as an educational **YOLO-like CNN object-detection implementation**. It is not the same as training or running an official YOLO release.
