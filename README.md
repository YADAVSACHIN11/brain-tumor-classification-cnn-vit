# Brain Tumor Classification using CNN-ViT Hybrid Model with Cross-Attention

## Overview

This project presents a hybrid deep learning framework for automatic brain tumor classification from MRI images. The proposed architecture combines the local feature extraction capability of Convolutional Neural Networks (CNNs) with the global contextual understanding of Vision Transformers (ViTs). A Cross-Attention Fusion Module is employed to effectively integrate features from both branches, resulting in improved classification performance.

The model is designed to assist in early and accurate detection of brain tumors, which can support medical professionals in diagnosis and treatment planning.

---

## Features

- Hybrid CNN + Vision Transformer architecture
- Cross-Attention based feature fusion
- MRI brain tumor image classification
- Data preprocessing and augmentation
- Model training and evaluation pipeline
- Performance comparison with standalone CNN and ViT models
- Visualization of training and validation metrics

---

## Dataset

The model is trained on a publicly available Brain Tumor MRI dataset.

### Classes

- Glioma Tumor
- Meningioma Tumor
- Pituitary Tumor
- No Tumor

### Dataset Structure

```
dataset/
│
├── Training/
│   ├── glioma/
│   ├── meningioma/
│   ├── pituitary/
│   └── notumor/
│
└── Testing/
    ├── glioma/
    ├── meningioma/
    ├── pituitary/
    └── notumor/
```

---

## Methodology

### 1. Data Preprocessing

- Image resizing
- Normalization
- Data augmentation
  - Rotation
  - Horizontal Flip
  - Zoom
  - Brightness Adjustment

### 2. CNN Branch

The CNN branch extracts local spatial features such as:

- Tumor boundaries
- Texture patterns
- Shape information

### 3. Vision Transformer Branch

The ViT branch captures:

- Long-range dependencies
- Global contextual relationships
- Spatial attention information

### 4. Cross-Attention Fusion

A Cross-Attention mechanism is introduced to:

- Exchange information between CNN and ViT features
- Enhance feature representation
- Improve classification performance

### 5. Classification Layer

The fused feature vector is passed through fully connected layers followed by a Softmax classifier to predict tumor categories.

---

## Proposed Architecture

```
MRI Image
    │
    ▼
Preprocessing
    │
 ┌──┴─────────────┐
 │                │
 ▼                ▼
CNN Branch    ViT Branch
 │                │
 └─────┬──────────┘
       ▼
Cross-Attention Fusion
       ▼
Feature Concatenation
       ▼
Dense Layers
       ▼
Softmax Classifier
       ▼
Tumor Prediction
```

---

## Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-Learn
- OpenCV
- Google Colab

---

## Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/brain-tumor-classification-cnn-vit.git
cd brain-tumor-classification-cnn-vit
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Training

Run the training script:

```bash
python train.py
```

or open the notebook:

```bash
Brain_Tumor_CNN_ViT.ipynb
```

---

## Testing

```bash
python test.py
```

---

## Evaluation Metrics

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

---

## Experimental Results

| Model | Accuracy |
|---------|---------|
| CNN | XX.XX% |
| Vision Transformer | XX.XX% |
| CNN + ViT | XX.XX% |
| CNN + ViT + Cross-Attention (Proposed) | XX.XX% |

> Replace the values with your actual experimental results.

---

## Results Visualization

The project provides:

- Training Accuracy Curve
- Validation Accuracy Curve
- Loss Curve
- Confusion Matrix
- Classification Report

---

## Applications

- Computer-Aided Diagnosis (CAD)
- Medical Imaging Analysis
- Clinical Decision Support Systems
- Brain Tumor Screening

---

## Future Improvements

- Multi-modal MRI integration
- Explainable AI using Grad-CAM
- Real-time clinical deployment
- Lightweight model optimization
- Integration with web applications

---

## Project Structure

```
brain-tumor-classification-cnn-vit/
│
├── dataset/
├── models/
├── notebooks/
├── results/
├── images/
├── train.py
├── test.py
├── requirements.txt
├── README.md
└── Brain_Tumor_CNN_ViT.ipynb
```

---
## Dataset

This project uses a brain MRI dataset for tumor classification.

### Source:
Dataset taken from:
https:https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset

---


---

## Authors

Sachin Sahu

B.Tech, Computer Science & Engineering

Rajkiya Engineering College, Kannauj

---

## License

This project is intended for educational and research purposes.
