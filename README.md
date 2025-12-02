# Brain-Tumor-Detection-Using-Deep-Learning-MRI-Images-Detection-Using-Computer-Vision
# Brain Tumor Identification Using Deep Learning 🧠

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.0%2B-orange)
![Flask](https://img.shields.io/badge/Framework-Flask-green)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

## 📌 Project Overview
[cite_start]This project is an **Artificial Intelligence-based Computer-Aided Diagnosis (CAD) system** designed to automate the detection and classification of brain tumors using Magnetic Resonance Imaging (MRI) scans[cite: 351, 357].

[cite_start]Utilizing **Deep Learning** and **Computer Vision** techniques, specifically **Transfer Learning with the VGG16 architecture**, the model classifies MRI images into four distinct clinical categories with high precision[cite: 352, 353]. [cite_start]The system is deployed via a user-friendly web interface built with **Flask**, allowing medical professionals to upload scans and receive instant diagnostic results[cite: 355].

## 🎯 Objectives
* [cite_start]**Automated Analysis:** Extract features from raw MRI scans without manual intervention[cite: 377].
* [cite_start]**Multi-Class Classification:** Classify tumors into **Glioma**, **Meningioma**, **Pituitary**, or **No Tumor**[cite: 353].
* [cite_start]**High Accuracy:** Achieve diagnostic accuracy comparable to human experts (~99%)[cite: 357].
* [cite_start]**Accessibility:** Provide a web-based interface for easy usage in clinical settings[cite: 355].

## 🛠️ Tech Stack
* [cite_start]**Deep Learning Framework:** TensorFlow, Keras[cite: 560].
* [cite_start]**Model Architecture:** VGG16 (Pre-trained on ImageNet)[cite: 352, 530].
* [cite_start]**Backend:** Python, Flask[cite: 355].
* [cite_start]**Frontend:** HTML5, CSS3, Bootstrap[cite: 562].
* [cite_start]**Image Processing:** OpenCV, NumPy, Pillow[cite: 567].
* [cite_start]**Visualization:** Matplotlib, Seaborn[cite: 610, 681].

## 📂 Dataset
[cite_start]The model was trained on a balanced, publicly available Brain MRI dataset consisting of four classes[cite: 490]:
1.  **Glioma Tumor**
2.  **Meningioma Tumor**
3.  **Pituitary Tumor**
4.  **No Tumor** (Healthy Control)

## 🧠 Model Architecture (VGG16)
[cite_start]We employed **Transfer Learning** to leverage the feature extraction capabilities of VGG16[cite: 522].
* [cite_start]**Base:** VGG16 with the first 13 convolutional layers **frozen** to preserve pre-learned features[cite: 533].
* **Custom Classification Head:**
    * [cite_start]`Flatten` Layer: Converts 3D tensor to 1D vector[cite: 540].
    * [cite_start]`Dense` Layer: 128 neurons with ReLU activation[cite: 542].
    * [cite_start]`Dropout` Layer: 0.5 rate to prevent overfitting[cite: 544].
    * [cite_start]`Softmax` Output Layer: 4 classes for probability distribution[cite: 546].
* [cite_start]**Optimization:** Trained using the **Adam optimizer** and **Categorical Cross-Entropy** loss function[cite: 550, 552].

## 📊 Results & Performance
* [cite_start]**Testing Accuracy:** ~99%[cite: 357].
* [cite_start]**AUC Score:** 1.00 for Pituitary, Meningioma, and No Tumor classes[cite: 634].
* [cite_start]**False Positives:** **Zero** false positives for healthy (No Tumor) patients[cite: 684].
* [cite_start]**Inference Time:** < 2 seconds per image[cite: 582].

## 🚀 Installation & Setup

### Prerequisites
* Python 3.8+
* pip

### Step 1: Clone the Repository
```bash
git clone [https://github.com/your-username/brain-tumor-detection.git](https://github.com/your-username/brain-tumor-detection.git)
cd brain-tumor-detection
