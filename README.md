# 🫁 Detection of Lung Cancer Using Histopathological and CT Scan Images

An AI-powered multi-modal lung cancer detection system that classifies lung tissue using **Histopathological Images** and **CT Scan Images**. The project compares a deep learning-based approach with a hybrid feature extraction approach to identify the most effective method for lung cancer classification.

## 📖 Overview

Lung cancer is one of the leading causes of cancer-related deaths worldwide. Early diagnosis plays a crucial role in improving patient survival. This project proposes an intelligent diagnostic framework that leverages both **deep learning** and **machine learning** techniques for accurate lung cancer detection.

Two different approaches were implemented and evaluated:

- **Approach 1:** MobileNetV2 + XGBoost
- **Approach 2:** InceptionV3 + HOG + DAISY + XGBoost

The project demonstrates that deep learning-based feature extraction significantly outperforms handcrafted feature extraction for heterogeneous medical imaging datasets.

---

## 🎯 Objectives

- Develop an AI-based system for lung cancer classification.
- Utilize both Histopathological and CT scan images.
- Compare deep learning and hybrid feature extraction techniques.
- Improve diagnostic accuracy while maintaining computational efficiency.

---

## 🏗️ Project Pipeline

```
Input Images
      │
      ▼
Data Preprocessing
      │
      ▼
Feature Extraction
      │
      ├── Approach 1
      │      MobileNetV2
      │
      └── Approach 2
             InceptionV3
             + HOG
             + DAISY
      │
      ▼
Dimensionality Reduction (PCA)
      │
      ▼
XGBoost Classification
      │
      ▼
Performance Evaluation
```

---

## 📂 Dataset

The project utilizes two types of medical imaging datasets:

- Histopathological Lung Tissue Images
- CT Scan Images

Classes:

- Normal Lung Tissue
- Adenocarcinoma
- Squamous Cell Carcinoma

---

## 🖼️ Image Preprocessing

### Histopathology Images

- Color Noralization
- Stain Normalization
- Noise Reduction
- Resize to **150 × 150**

### CT Scan Images

- Rotation
- Scaling
- Brightness/Contrast Adjustment
- CLAHE
- Resize to **256 × 256**

---

# 🚀 Approach 1 – Deep Learning Based

### Feature Extractor

- MobileNetV2 (Pretrained on ImageNet)

### Classifier

- XGBoost

### Advantages

- Automatic feature learning
- Lightweight architecture
- Better generalization
- Higher accuracy

---

# 🚀 Approach 2 – Hybrid Feature-Based

### Feature Extractors

- InceptionV3
- Histogram of Oriented Gradients (HOG)
- DAISY Descriptor

### Dimensionality Reduction

- Principal Component Analysis (PCA)

### Classifier

- XGBoost

### Purpose

This approach combines deep semantic features with handcrafted texture descriptors to evaluate whether feature fusion improves lung cancer classification.

---

## 📊 Results

| Model | Feature Extractor | Classifier | Accuracy |
|--------|------------------|------------|-----------|
| Proposed Model 1 | MobileNetV2 | XGBoost | **99.03%** |
| Proposed Model 2 | InceptionV3 + HOG + DAISY | XGBoost | **86.56%** |

---

## 📈 Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

---

## 💡 Key Findings

- MobileNetV2 automatically learns robust hierarchical features.
- Handcrafted descriptors (HOG & DAISY) are sensitive to texture and modality variations.
- Deep learning-based feature extraction generalized significantly better across Histopathological and CT images.
- MobileNetV2 + XGBoost achieved the best overall performance.

---

## 🛠️ Technologies Used

- Python
- TensorFlow / Keras
- Scikit-learn
- OpenCV
- XGBoost
- NumPy
- Pandas
- Matplotlib
- Albumentations
- HDF5

---

## 📁 Project Structure

```

---

## 🔮 Future Improvements

- Explainable AI using Grad-CAM
- Integration of patient clinical information
- Federated Learning for privacy-preserving AI
- Real-time deployment for clinical applications
- Mobile and edge-device optimization

---

## 📄 Research Paper

**Detection of Lung Cancer Using Histopathological and CT Scan Images**

This project was developed as part of our research work on AI-assisted lung cancer diagnosis using multi-modal medical imaging.

---
