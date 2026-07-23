# 🚧 Deep Learning Based Road Pothole Detection System

A Convolutional Neural Network (CNN) based deep learning project for **image-based road pothole detection**. The model classifies road images into two categories: **Normal Road** and **Road with Potholes** using TensorFlow/Keras and OpenCV.

> **Note:** This project performs pothole detection through **image classification** and is **not a real-time video detection system**.

---

## 📌 Project Overview

Road potholes are a major cause of road accidents, vehicle damage, and traffic disruptions. Manual inspection of roads is time-consuming and expensive. This project presents a deep learning solution that automatically classifies road images into **Normal** or **Pothole** categories using a Convolutional Neural Network (CNN).

The model is trained on a labeled dataset of road images and achieves reliable performance for binary image classification.

---

## ✨ Features

- Image-based pothole detection
- Binary classification (Normal / Pothole)
- CNN architecture built using TensorFlow/Keras
- Image preprocessing using OpenCV
- Automatic image normalization
- Early Stopping during training
- Accuracy & Loss visualization
- Confusion Matrix
- Classification Report
- Single image prediction
- Trained model saved in `.keras` format

---

## 📂 Dataset

The dataset is hosted on Google Drive because it exceeds GitHub's recommended file size limits.

**Dataset Link**
https://drive.google.com/drive/folders/1Y90KnlPOvthZvcPNPXed7hTJwSTyJvwd?usp=drive_link

### Dataset Structure

```text
DATASET/
│
├── normal/
│     ├── image1.jpg
│     ├── image2.jpg
│     └── ...
│
└── potholes/
      ├── image1.jpg
      ├── image2.jpg
      └── ...
```

Update the dataset path in the notebook if your Google Drive location is different.

---

## 🛠 Technologies Used

- Python
- TensorFlow
- Keras
- OpenCV
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

---

## 🧠 CNN Architecture

```text
Input Image (128 × 128 × 3)
            │
            ▼
Conv2D (32) + ReLU
            │
       MaxPooling
            │
            ▼
Conv2D (64) + ReLU
            │
       MaxPooling
            │
            ▼
Conv2D (128) + ReLU
            │
       MaxPooling
            │
            ▼
Conv2D (128) + ReLU
            │
       MaxPooling
            │
            ▼
Conv2D (128) + ReLU
            │
       MaxPooling
            │
            ▼
Flatten
            │
Dropout (0.4)
            │
Dense (128)
            │
Softmax (2 Classes)
            │
            ▼
Prediction
```

---

## ⚙️ Training Configuration

| Parameter | Value |
|-----------|-------|
| Image Size | 128 × 128 |
| Optimizer | Adam |
| Loss Function | Categorical Crossentropy |
| Batch Size | 12 |
| Epochs | 30 |
| Train/Test Split | 75% / 25% |
| Framework | TensorFlow/Keras |

---

## 📊 Model Performance

### Test Results

| Metric | Value |
|---------|-------|
| Test Accuracy | **90.64%** |
| Test Loss | **0.2541** |

---

### Classification Report

| Class | Precision | Recall | F1-Score |
|------|----------:|-------:|---------:|
| Normal | **0.91** | **0.91** | **0.91** |
| Potholes | **0.90** | **0.90** | **0.90** |

**Overall Accuracy:** **90.64%**

---

### Confusion Matrix

| Actual Class | Predicted Normal | Predicted Potholes |
|--------------|-----------------:|-------------------:|
| **Normal** | **80** | **8** |
| **Potholes** | **8** | **75** |

The model correctly classified **155 out of 171** test images.

---

## 📁 Project Structure

```text
Deep-Learning-Based-Road-Pothole-Detection-System/
│
├── README.md
├── LICENSE
├── requirements.txt
├── .gitignore
├── POTHOLE.ipynb
│
├── outputs/
│   ├── accuracy_loss.png
│   ├── confusion_matrix.png
│   └── sample_predictions.png
│
├── saved_model/
│   └── pothole_cnn.keras
│
└── sample_images/
    ├── normal.jpg
    └── pothole.jpg
```

---

## 🚀 Installation

### Clone the Repository

```bash
git clone https://github.com/<your-github-username>/Deep-Learning-Based-Road-Pothole-Detection-System.git
```

### Navigate to the Project Folder

```bash
cd Deep-Learning-Based-Road-Pothole-Detection-System
```

### Install Required Packages

```bash
pip install -r requirements.txt
```

### Open the Notebook

```bash
jupyter notebook
```

---

## 📷 Example Prediction

```python
predict_image("sample_images/pothole.jpg")
```

Example Output

```text
Prediction : POTHOLES
Confidence : 98.43%
```

---

## 📈 Output Files

After training, the following files are generated:

- `accuracy_loss.png`
- `confusion_matrix.png`
- `sample_predictions.png`
- `pothole_cnn.keras`

---

## 🔮 Future Scope

- Increase dataset size for better generalization
- Apply Transfer Learning (MobileNetV2, EfficientNet)
- Extend to multi-class road surface classification
- Estimate pothole severity
- Develop a web application for image upload and prediction
- Extend the project to real-time detection using object detection models such as YOLO

---
