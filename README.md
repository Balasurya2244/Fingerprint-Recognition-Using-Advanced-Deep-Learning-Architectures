# Enhanced Fingerprint Recognition using Advanced Deep Learning Architectures

## Introduction
Fingerprint recognition is one of the most widely used biometric technologies for identity verification. However, **partial fingerprint recognition** remains a challenging problem due to limited ridge information, variations in finger orientation, and differences in sensor characteristics.

This project presents an **efficient and scalable partial fingerprint recognition system** using **Siamese deep learning architectures combined with SIFT-based feature matching**, designed to improve generalization across multiple fingerprint sensors while significantly reducing training time.

---

## Base Paper
**A Hybrid Deep Learning and Feature Descriptor Approach for Partial Fingerprint Recognition**

The base paper achieved strong recognition performance using a **Siamese CNN + SIFT** framework but suffered from:
- Very long training time (up to **2500 epochs**)
- Separate training for each fingerprint database
- Limited scalability across different sensors

---

## Proposed Approach
To overcome these limitations, this work introduces a **unified Siamese learning framework** with the following key improvements:

### Siamese Deep Learning Models
The following transfer learning models are implemented within a Siamese architecture:
- ResNet18  
- EfficientNet-B0  
- MobileNetV2  
- ShuffleNetV2  

These lightweight models efficiently learn **discriminative embeddings** from partial fingerprint images.

---

### Cross-Sensor Generalization
All four **FVC2002 databases (DB1–DB4)** are combined into a **single unified dataset**, enabling:
- Learning of cross-sensor fingerprint features  
- Improved generalization  
- Elimination of database-specific model training  

---

### Hybrid Similarity Fusion
For each fingerprint pair:
1. A **deep similarity score** is obtained from the Siamese network  
2. A **SIFT-based similarity score** is computed using keypoint matching  

Both scores are fused using a **weighted fusion strategy** to produce the final verification decision.

---

## Evaluation Metrics
The system is evaluated using standard biometric performance measures:
- **Equal Error Rate (EER)**
- **Area Under the ROC Curve (AUC)**

### Results Summary
- **EER:** 5% – 8%  
- **Training epochs reduced:** 2500 → **50**  
- Comparable accuracy with significantly improved efficiency  

---

## Real-Time Fingerprint Verification
A real-time fingerprint comparison interface is included that allows users to:
- Input two fingerprint images  
- Visualize fingerprint pairs  
- Display **MATCH / NON-MATCH** decision  
- Show similarity score and decision threshold  

---

## Dataset
- **FVC2002 Fingerprint Database**
  - DB1, DB2, DB3, DB4
  - Multiple sensor types
  - Partial fingerprint samples

>  The dataset must be downloaded separately from the official FVC website.

---

## Technologies Used
- Python  
- PyTorch  
- OpenCV  
- scikit-learn  
- timm (PyTorch Image Models)  
- SIFT (OpenCV)

---

## Key Contributions
- Reduced training time with transfer learning  
- Unified cross-sensor fingerprint model  
- Lightweight Siamese architectures  
- Hybrid deep learning + handcrafted feature fusion  
- Real-time verification capability  

---
