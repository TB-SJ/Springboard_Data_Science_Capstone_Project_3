# 🧠 Brain Tumor Detection from MRI Scans

This project leverages deep learning to automate the detection of brain tumors from MRI images. Early and accurate detection plays a critical role in improving treatment outcomes and planning for patients. This model uses convolutional neural networks (CNNs) and transfer learning to classify brain MRI images into tumor and no-tumor categories.

---

## 📌 Table of Contents
- [Project Overview](#project-overview)  
- [Motivation](#motivation)  
- [Data Description](#data-description)  
- [Methodology](#methodology)  
- [Model Performance](#model-performance)  
- [Confusion Matrices](#confusion-matrices)  
- [Business Value](#business-value)  
- [Future Work](#future-work)  
- [Author](#author)

---

## 🔍 Project Overview

The goal of this capstone project is to build a binary image classification model to detect the presence of brain tumors using MRI scans. The project investigates the effectiveness of CNN architectures and transfer learning in medical image analysis.

---

## 💡 Motivation

- Brain tumors are life-threatening conditions requiring early and accurate diagnosis.
- Manual MRI analysis is time-consuming and prone to error.
- A robust, automated classification model can help radiologists flag potential cases faster and more accurately.

---

## 📊 Data Description

- **Input Type:** MRI brain scan images  
- **Labels:** Binary classification — Tumor / No Tumor  
- **Preprocessing:** Resizing, normalization, and data augmentation (e.g. flipping, zooming, rotation)  
- Source: Kaggle- https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset
  
-| Meta Data      | Raw Imaged | Cleaned Images | 
|----------------|----------|-----------|
| Image Size | 368 different image sizes     | (224, 224      | 
| Image Mode      | 4 different image modes     | RGB     | 



---

## 🧠 Methodology

- **Model Architectures Compared:**  
  - MobileNetV2 (Transfer Learning) ✅ *Best Performer*  
  - Custom CNN (Built from scratch)  
  - EfficientNetB0 (Transfer Learning)  
- **Steps:**  
  - Data augmentation and preprocessing  
  - Feature extraction using pre-trained models  
  - Fine-tuning final layers  
  - Model comparison on test set performance  
- **Loss Function:** Binary Crossentropy  
- **Optimizer:** Adam  

---

## 📈 Model Performance

| Model           | Accuracy | Precision | Recall | F1-Score | Test Loss |
|----------------|----------|-----------|--------|----------|-----------|
| **MobileNetV2** | 0.95     | 0.97      | 1.00   | 0.98     | 0.14      |
| Custom CNN      | 0.89     | 0.99      | 0.85   | 0.91     | 0.26      |
| EfficientNetB0  | 0.68     | 1.00      | 0.55   | 0.71     | 0.85      |

> ✅ **MobileNetV2 was the best-performing model** with near-perfect results, especially recall, which is critical in medical diagnoses.

---

## 📊 Confusion Matrices (Test Set)

**MobileNetV2**
```
Predicted →   No Tumor     Tumor
Actual
No Tumor         231         25
Tumor              2        730
```

**Custom CNN**
```
Predicted →   No Tumor     Tumor
Actual
No Tumor         254          2
Tumor            109        625
```

**EfficientNetB0**
```
Predicted →   No Tumor     Tumor
Actual
No Tumor         185         71
Tumor            331        403
```

---

## 💼 Business Value

- **Clinical Decision Support**: High-recall model helps flag potential tumors early in the diagnostic pipeline  
- **Operational Efficiency**: Reduces manual workload on radiologists  
- **Patient Safety**: Minimizes false negatives, ensuring fewer tumors are missed  
- **Scalability**: Can be deployed into diagnostic tools or integrated with telemedicine platforms

---

## 🚀 Future Work

- Add explainability (e.g. Grad-CAM) to visualize what parts of the image influence decisions  
- Improve robustness with external validation datasets  
- Expand dataset to include tumor types and severity levels  
- Deploy model as a web app using Streamlit or Flask  

---

## 👤 Author

**Travis Bates**  
Springboard Data Science Graduate  
[LinkedIn](https://www.linkedin.com/in/travis-bates)  
Email: bates.travis@outlook.com
