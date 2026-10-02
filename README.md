#  Development of AI Algorithms for Lung Disease Diagnosis

University of Thessaly | Department of Computer Science & Telecommunications **Thesis Grade:** 10/10 (Honors) 


##  Project Overview

This thesis presents a multi-model Artificial Intelligence (AI) system designed for the automated detection of pulmonary pathologies through **Chest X-ray** analysis. Utilizing a dataset of over **112,000 images** (NIH Chest X-ray Dataset), the system identifies seven distinct conditions with high accuracy.

###  Targeted Pathologies

The system consists of seven independent machine learning models, each trained to recognize a specific condition:

**Pneumonia** (96% Accuracy)

**Cardiomegaly** (86% Accuracy)

**Emphysema** (84% Accuracy)

**Pneumothorax** (82% Accuracy)

**Mass** (76% Accuracy)

**Atelectasis** (72% Accuracy)

**Nodule** (68% Accuracy) 


##  Technical Architecture

### **The Fusion Model Strategy**

Instead of a single architecture, each disease model utilizes a **fusion of two pre-trained CNNs** to maximize feature extraction:

**MobileNetV2:** For efficient, lightweight feature processing.

**ResNet50:** For deep residual learning and complex pattern recognition.



### **Training Pipeline**

**Binary Classification:** Each model is trained independently (Normal vs. Disease).

**Two-Phase Training:** 
1.  **Head Training:** Pre-trained layers are frozen while the new classification head is trained.
2.  **Fine-Tuning:** All layers are unfrozen for detailed optimization at a lower learning rate ().

**Optimizations:** 

**Mixed Precision Training** for  speed

**Class Weighting** to handle dataset imbalance

**Early Stopping** to prevent overfitting.



##  Software Stack


**Deep Learning:** TensorFlow 2.12, Keras API 

**Inference & GUI:** Python 3, PyQt5 

**Image Processing:** OpenCV, PIL, and **Grad-CAM** for visual explainability 

**Environment:** Ubuntu Linux VM with **CUDA 11.8/cuDNN 8.6** for GPU acceleration 


##  Interpretability (XAI)

To ensure clinical utility, the system integrates **Grad-CAM (Gradient-weighted Class Activation Mapping)**. 
This provides heatmap visualizations that highlight the specific areas of the X-ray that influenced the model's diagnostic prediction, bridging the gap between "black box" AI and medical transparency.

##  Confidentiality & Access

The source code and specific training scripts are **restricted** for academic and intellectual property reasons.

**Contact for Technical Walkthrough:**

**Author:** Yiorgos Papadopoulos 


 
**LinkedIn:** https://www.linkedin.com/in/yiorgospapadopoulos/
  
**Email:** giorgospapadopoulos002@yahoo.com 
