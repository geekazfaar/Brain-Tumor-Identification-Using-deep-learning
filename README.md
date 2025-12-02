# Brain Tumor Identification Using Deep Learning 🧠

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.0%2B-orange)
![Flask](https://img.shields.io/badge/Framework-Flask-green)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

## 📌 Project Overview
This project is an **Artificial Intelligence-based Computer-Aided Diagnosis (CAD) system** designed to automate the detection and classification of brain tumors using Magnetic Resonance Imaging (MRI) scans.

Utilizing **Deep Learning** and **Computer Vision** techniques, specifically **Transfer Learning with the VGG16 architecture**, the model classifies MRI images into four distinct clinical categories with high precision. The system is deployed via a user-friendly web interface built with **Flask**, allowing medical professionals to upload scans and receive instant diagnostic results.

## 🎯 Objectives
* **Automated Analysis:** Extract features from raw MRI scans without manual intervention.
* **Multi-Class Classification:** Classify tumors into **Glioma**, **Meningioma**, **Pituitary**, or **No Tumor**.
* **High Accuracy:** Achieve diagnostic accuracy comparable to human experts (~99%).
* **Accessibility:** Provide a web-based interface for easy usage in clinical settings.

## 🛠️ Tech Stack
* **Deep Learning Framework:** TensorFlow, Keras.
* **Model Architecture:** VGG16 (Pre-trained on ImageNet).
* **Backend:** Python, Flask.
* **Frontend:** HTML5, CSS3, Bootstrap.
* **Image Processing:** OpenCV, NumPy, Pillow.
* **Visualization:** Matplotlib, Seaborn.

## 📂 Dataset
The model was trained on a balanced, publicly available Brain MRI dataset consisting of four classes:
1.  **Glioma Tumor**
2.  **Meningioma Tumor**
3.  **Pituitary Tumor**
4.  **No Tumor** (Healthy Control)

## 🧠 Model Architecture (VGG16)
We employed **Transfer Learning** to leverage the feature extraction capabilities of VGG16.
* **Base:** VGG16 with the first 13 convolutional layers **frozen** to preserve pre-learned features.
* **Custom Classification Head:**
    * `Flatten` Layer: Converts 3D tensor to 1D vector.
    * `Dense` Layer: 128 neurons with ReLU activation.
    * `Dropout` Layer: 0.5 rate to prevent overfitting.
    * `Softmax` Output Layer: 4 classes for probability distribution.
* **Optimization:** Trained using the **Adam optimizer** and **Categorical Cross-Entropy** loss function.

## 📊 Results & Performance
* **Testing Accuracy:** ~99%.
* **AUC Score:** 1.00 for Pituitary, Meningioma, and No Tumor classes.
* **False Positives:** **Zero** false positives for healthy (No Tumor) patients.
* **Inference Time:** < 2 seconds per image.

## 🚀 Installation & Setup

### Prerequisites
* Python 3.8+
* pip

### Step 1: Clone the Repository
```bash
git clone [https://github.com/your-username/brain-tumor-detection.git](https://github.com/your-username/brain-tumor-detection.git)
cd brain-tumor-detection
````

### Step 2: Install Dependencies

```bash
pip install -r requirements.txt
```

*Note: Ensure `tensorflow`, `flask`, `numpy`, `pillow`, and `matplotlib` are in your requirements file.*

### Step 3: Project Structure

Ensure your directories are organized as follows:

```
├── app.py                  # Main Flask application
├── models/
│   └── model.h5            # The saved VGG16 model file
├── static/
│   ├── css/
│   └── uploads/            # Folder for temporary image uploads
├── templates/
│   └── index.html          # Web Interface
└── README.md
```

### Step 4: Run the Application

```bash
python app.py
```

### Step 5: Access the Interface

Open your browser and navigate to:
`http://127.0.0.1:5000/`


## 🔮 Future Scope

  * **Segmentation:** Implementing U-Net for precise tumor localization (pixel-perfect boundaries).
  * **Cloud Deployment:** Hosting the app for remote telemedicine access.
  * **Explainable AI (XAI):** Integrating Grad-CAM to visualize heatmap overlays for better trust.

