# 🎯 Object Detection Using YOLO Algorithm

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![YOLO](https://img.shields.io/badge/YOLO-v8-red?style=for-the-badge)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green?style=for-the-badge&logo=opencv)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)

A real-time **Object Detection System** built using the **YOLO (You Only Look Once)** algorithm. This project detects and classifies multiple objects in images and video streams with high accuracy and speed.

---

## 📌 Table of Contents

- [About the Project](#-about-the-project)
- [Features](#-features)
- [Demo](#-demo)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Installation](#-installation)
- [Usage](#-usage)
- [How It Works](#-how-it-works)
- [Results](#-results)
- [Documentation](#-documentation)
- [Roadmap](#-roadmap)
- [Contributing](#-contributing)
- [License](#-license)
- [Author](#-author)
- [Connect With Me](#-connect-with-me)
- [Acknowledgements](#-acknowledgements)

---

## 🧠 About the Project

**Object Detection Using YOLO Algorithm** is a computer vision project that leverages the power of the YOLO (You Only Look Once) deep learning model to identify and localize objects in real time. Unlike traditional detection systems, YOLO treats object detection as a single regression problem, making it extremely fast and suitable for real-time applications.

This project demonstrates:
- How to load and use a pre-trained YOLO model
- How to perform detection on images and video streams
- How to draw bounding boxes with class labels and confidence scores
- How to optimize detection for real-time performance

---

## ✨ Features

- ✅ **Real-time object detection** on images, videos, and webcam feed
- ✅ **80+ object classes** supported (COCO dataset)
- ✅ **High-speed inference** using YOLO architecture
- ✅ **Bounding boxes** with class labels and confidence scores
- ✅ **Configurable confidence threshold** and NMS (Non-Maximum Suppression)
- ✅ **Modular Python code** — easy to extend and integrate
- ✅ **Cross-platform** — works on Windows, Linux, and macOS
- ✅ **Well-documented** with detailed project reports and user guides

---

## 🎥 Demo

### Sample Detection Output

> _Add your detection screenshots here_

```bash
# Example
Input:  sample_image.jpg
Output: Detected 5 objects (person, car, dog, bicycle, traffic light)
```

### Video Demo

> _Add a GIF or YouTube link of your project demo here_

---

## 🛠 Tech Stack

| Technology | Purpose |
|------------|---------|
| **Python 3.8+** | Core programming language |
| **YOLO (Ultralytics)** | Object detection model |
| **OpenCV** | Image/video processing |
| **NumPy** | Numerical computations |
| **PyTorch** | Deep learning backend |
| **Matplotlib** | Visualization |

---

## 📁 Project Structure

```
Object-Detection-Using-YOLO-Algorithm/
│
├── object_detection_using_yolo_algorithm.py   # Main detection script
├── requirements.txt                            # Python dependencies
├── README.md                                   # Project documentation
├── .gitignore                                  # Git ignore rules
│
└── docs/                                       # Documentation folder
    ├── Object_Detection_YOLO_Project_Report.docx
    ├── Object_Detection_YOLO_Project_Report.pdf
    ├── PROJECT_REPORT.md
    ├── TECHNICAL_DOCUMENTATION.md
    └── USER_GUIDE.md
```

---

## ⚙️ Installation

### Prerequisites

- Python 3.8 or higher
- pip package manager
- (Optional) CUDA-compatible GPU for faster inference

### Step 1: Clone the Repository

```bash
git clone https://github.com/abdullahshaheer901-pixel/Object-Detection-Using-YOLO-Algorithm.git
cd Object-Detection-Using-YOLO-Algorithm
```

### Step 2: Create Virtual Environment (Recommended)

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux / macOS
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Download YOLO Weights (if not included)

Download the YOLO weights file and place it in the project root directory:
- `yolov8n.pt` (Nano — fastest)
- `yolov8s.pt` (Small — balanced)
- `yolov8m.pt` (Medium — more accurate)

---

## ▶️ Usage

### Run with Webcam

```bash
python object_detection_using_yolo_algorithm.py
```

### Run with an Image

```bash
python object_detection_using_yolo_algorithm.py --source path/to/image.jpg
```

### Run with a Video File

```bash
python object_detection_using_yolo_algorithm.py --source path/to/video.mp4
```

### Adjust Confidence Threshold

```bash
python object_detection_using_yolo_algorithm.py --conf 0.5
```

---

## 🔍 How It Works

1. **Input** — Image, video, or webcam frame is captured.
2. **Preprocessing** — Frame is resized and normalized.
3. **YOLO Inference** — The YOLO model predicts bounding boxes, class probabilities, and confidence scores.
4. **Post-processing** — Non-Maximum Suppression (NMS) removes duplicate detections.
5. **Output** — Detected objects are drawn with bounding boxes, labels, and confidence scores.

### YOLO Algorithm Summary

YOLO divides the input image into an **S × S grid**. Each grid cell predicts:
- **B** bounding boxes
- **Confidence score** for each box
- **C** class probabilities

This single-pass approach makes YOLO extremely fast compared to two-stage detectors like R-CNN.

---

## 📊 Results

| Metric | Value |
|--------|-------|
| Model | YOLOv8 |
| mAP@0.5 | 0.XX |
| Inference Speed | XX FPS (GPU) / XX FPS (CPU) |
| Classes Supported | 80 (COCO) |

> _Update these values with your actual results_

### Sample Outputs

> _Add detection screenshots here_

---

## 📚 Documentation

Detailed documentation is available in the [`docs/`](docs/) folder:

| Document | Description |
|----------|-------------|
| [PROJECT_REPORT.md](docs/PROJECT_REPORT.md) | Complete project report |
| [TECHNICAL_DOCUMENTATION.md](docs/TECHNICAL_DOCUMENTATION.md) | Technical details & architecture |
| [USER_GUIDE.md](docs/USER_GUIDE.md) | Step-by-step user guide |
| [Project Report (PDF)](docs/Object_Detection_YOLO_Project_Report.pdf) | Formatted PDF report |
| [Project Report (DOCX)](docs/Object_Detection_YOLO_Project_Report.docx) | Editable Word document |

---

## 🗺 Roadmap

- [x] Basic YOLO object detection on images
- [x] Real-time detection on webcam feed
- [x] Video file detection support
- [ ] Custom dataset training
- [ ] Web interface (Flask/Streamlit)
- [ ] Mobile deployment (TFLite)
- [ ] Multi-object tracking (DeepSORT integration)

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Abdullah Shaheer**

- 🎓 Data Analytics Student | Computer Vision Enthusiast
- 🐙 GitHub: [@abdullahshaheer901-pixel](https://github.com/abdullahshaheer901-pixel)
- 💼 LinkedIn: [Abdullah Shaheer](https://www.linkedin.com/in/abdullah-shaheer260)
- 📊 Kaggle: [@abdullahshaheer260](https://kaggle.com/abdullahshaheer260)
- 📧 Email: [abdullahshaheer901@gmail.com](mailto:abdullahshaheer901@gmail.com)

---

## 🌐 Connect With Me

<p align="left">
  <a href="https://www.linkedin.com/in/abdullah-shaheer260" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
  <a href="https://kaggle.com/abdullahshaheer260" target="_blank">
    <img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white" alt="Kaggle"/>
  </a>
  <a href="https://github.com/abdullahshaheer901-pixel" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
  </a>
  <a href="mailto:abdullahshaheer901@gmail.com" target="_blank">
    <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail"/>
  </a>
</p>

---

##  Acknowledgements

- [Ultralytics YOLO](https://github.com/ultralytics/ultralytics) — YOLO implementation
- [OpenCV](https://opencv.org/) — Computer vision library
- [COCO Dataset](https://cocodataset.org/) — Pre-trained classes
- [Digi Skills Program](https://digiskills.pk/) — Learning platform

---

## ⭐ Show Your Support

If this project helped you, please give it a **⭐ star** on GitHub!

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/abdullahshaheer901-pixel">Abdullah Shaheer</a>
</p>
