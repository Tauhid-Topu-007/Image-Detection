# 🐠 Aquarium Object Detection with Faster R-CNN

An end-to-end deep learning project for detecting and classifying aquatic animals in aquarium images using **Faster R-CNN** with a **MobileNetV3-Large + FPN** backbone and transfer learning from COCO-pretrained weights.

## 🚀 Project Overview

This repository contains Jupyter notebooks covering object detection with R-CNN-based architectures. The main project focuses on **Faster R-CNN**, trained to locate multiple marine-life objects in a single image using bounding-box detection.

The model is designed for the **Aquarium Combined Dataset** and supports detection of seven aquatic categories:

- 🐟 Fish
- 🪼 Jellyfish
- 🐧 Penguin
- 🐦 Puffin
- 🦈 Shark
- ⭐ Starfish
- 🐟 Stingray

## ✨ Key Features

- Faster R-CNN object detection
- MobileNetV3-Large backbone with Feature Pyramid Network (FPN)
- COCO-pretrained transfer learning
- Custom PyTorch dataset pipeline
- COCO-format annotation support
- Albumentations-based image augmentation
- GPU/CUDA support
- Training and loss monitoring
- Bounding-box prediction visualization
- Separate notebooks for R-CNN and Faster R-CNN experiments

## 🧠 Model Architecture

```text
Input Image
     │
     ▼
MobileNetV3-Large Backbone
     │
     ▼
Feature Pyramid Network (FPN)
     │
     ▼
Region Proposal Network (RPN)
     │
     ▼
RoI Features
     │
     ▼
Classification + Bounding Box Regression
     │
     ▼
Detected Aquatic Objects
```

The Faster R-CNN implementation uses `fasterrcnn_mobilenet_v3_large_fpn` from TorchVision and replaces the default prediction head to support the target dataset classes.

## 📊 Dataset

The project uses the **Aquarium Combined Dataset**, containing images and object-detection annotations in COCO JSON format.

**Dataset characteristics:**

| Property | Details |
|---|---|
| Domain | Aquarium / Marine Life |
| Annotation | Bounding Boxes |
| Format | COCO JSON |
| Classes | 7 |
| Splits | Train / Validation / Test |
| Task | Multi-class Object Detection |

## 📁 Repository Structure

```text
RCNN/
├── RCNN.ipynb          # R-CNN experiments
├── Faster_RCNN.ipynb   # Faster R-CNN implementation
└── README.md           # Project documentation
```

## 🛠️ Tech Stack

- **Python**
- **PyTorch**
- **TorchVision**
- **Albumentations**
- **NumPy**
- **Pandas**
- **Matplotlib**
- **Jupyter Notebook**
- **CUDA** (recommended for training)

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/Tauhid-Topu-007/RCNN.git
cd RCNN
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Activate it on Linux/macOS:

```bash
source venv/bin/activate
```

### 3. Install dependencies

Install the required packages used by the notebooks, including PyTorch, TorchVision, Albumentations, NumPy, Pandas, Matplotlib, and Jupyter.

For GPU training, install the PyTorch build compatible with your CUDA version from the official PyTorch installation instructions.

## ▶️ Running the Project

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
Faster_RCNN.ipynb
```

For the R-CNN experiments, open:

```text
RCNN.ipynb
```

Make sure the dataset path and annotation locations are correctly configured before running the training cells.

## 🔬 Training Workflow

The typical workflow is:

1. Load the Aquarium dataset.
2. Parse COCO-format annotations.
3. Apply image transformations and augmentation.
4. Build the Faster R-CNN model.
5. Load COCO-pretrained weights.
6. Replace the detection head for the target classes.
7. Train using GPU when available.
8. Track training losses.
9. Run inference on validation/test images.
10. Visualize predicted bounding boxes and class labels.

## 💻 Hardware Recommendation

Training object-detection models is computationally expensive. A CUDA-enabled NVIDIA GPU is recommended for practical training times. CPU execution is possible for experimentation and inference but will generally be much slower.

## 📌 Learning Objectives

This project demonstrates practical concepts including:

- Object detection
- Region Proposal Networks
- Faster R-CNN
- Transfer learning
- Backbone networks
- Feature Pyramid Networks
- Bounding-box regression
- Multi-class detection
- COCO annotation handling
- Computer vision data augmentation
- PyTorch/TorchVision model customization

## 🔮 Future Improvements

Potential extensions include:

- Add quantitative evaluation with mAP, IoU, precision, and recall
- Compare Faster R-CNN with YOLO and SSD
- Fine-tune different backbone architectures
- Add inference on custom images or video
- Build a Streamlit/Gradio demo
- Export the trained model for production inference
- Add experiment tracking with TensorBoard or Weights & Biases

## 👨‍💻 Author

**Tauhidul Islam Topu**

Computer Science & Engineering | Machine Learning & Deep Learning Enthusiast

GitHub: [@Tauhid-Topu-007](https://github.com/Tauhid-Topu-007)

## ⭐ Support

If you find this project useful for learning computer vision or object detection, consider giving the repository a ⭐ on GitHub.

## 📄 License

This project is intended for educational and research purposes. Please review the dataset's original license and terms before using the dataset or trained models for commercial purposes.
