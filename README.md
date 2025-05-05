# 🗑️ Garbage Classification (OpenCV + scikit-learn)

A complete computer vision project that classifies garbage images according to their material type using traditional image processing and machine learning.

---

### 📸 Overview

This project uses classical computer vision techniques and deep learning to:

* Extract relevant features from each garbage item.
* Classify the type of material using different machine learning models.

The goal is to automatically sort garbage into one of six material categories: **Glass, Metal, Paper, Plastic, Board, Other** — and to compare different classification approaches. The project uses a pretrained **Convolutional Neural Network (CNN) as a feature extractor**, followed by one of three types of classifiers:

- **CNN + Dense Layer **
- **CNN + K-Nearest Neighbors (KNN)**
- **CNN + Support Vector Machine (SVM)**

---

### ✨ Features

* ✅ Feature extraction for classification
* ✅ Trained classifier using `scikit-learn`
* 🧩 Easily extendable for deep learning models (e.g., CNNs)

---

### 🗂 Project Structure

```
📁 GarbageClassification/
│
├── GarbageClassification.ipynb         # Main notebook
├── garbage_dataset/                    # Folder with labeled training images
│   ├── glass/
│   ├── metal/
│   ├── paper/
│   ├── plastic/
│   ├── board/
│   └── other/
├── images/
│   ├── original.png                    # Example input image
│   ├── mask.png                        # Example mask after preprocessing
│   └── prediction_example.png          # Example of classification result
└── README.md
```

---

### 📦 Requirements

Install dependencies using pip:

```bash
pip install opencv-python scikit-learn numpy
```

### 🔍 Pipeline Summary

1. **Read Image:** Load the input image.
2. **Grayscale & Blur:** Reduce noise and prepare for segmentation.
3. **Thresholding & Morphology:** Create binary masks to isolate objects.
4. **Contour Detection:** Find and crop individual garbage items.
5. **Feature Extraction:** Extract shape, texture, and/or color features.
6. **Classification:** Predict material type using a trained ML classifier.

---

### 🧪 Sample Results

| Input Image                   | Classification Result              |
| ----------------------------- | ---------------------------------- |
| ![frame](images/original.png) | ![material](images/prediction_example.png) |
