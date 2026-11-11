# 🍏 AI-Based Freshness and Shelf-Life Prediction

An AI-powered web application that accurately classifies produce, predicts freshness scores, estimates shelf life, and supports dynamic pricing — enabling better inventory management and reducing food waste across the supply chain.

---

## 📌 Project Overview

This project utilizes Convolutional Neural Networks (CNN) and transfer learning techniques to predict the **freshness** and **remaining shelf life** of fruits and vegetables from images. It aims to assist both consumers and vendors by providing real-time visual analysis and actionable insights.

---

## 🚀 Features

- 🔍 **Freshness Classification** (e.g., Fresh Apple: 80.05%)
- 🕒 **Shelf-Life Prediction** (e.g., 10.46 days remaining)
- 🧠 **Deep Learning Models** trained on augmented datasets
- 📈 **Visualization of Predictions** using Matplotlib
- 💻 **Web-based Interface** for uploading and analyzing images
- 🧪 **Model Evaluation** using MAE, RMSE, and accuracy metrics

---

## 🧠 Models and Methodology

### 🔹 A. Freshness and Rottenness Score Prediction

- **Data Augmentation** using `ImageDataGenerator`:
  - Rescaling, shifting, rotating, zooming, flipping, and shearing
- **CNN Architecture**:
  - 3 Conv2D + MaxPooling2D layers
  - Dense(512) + Flatten + Softmax output (6 classes)
- **Transfer Learning**:
  - InceptionV3 with custom top layers
- **Training**:
  - Optimizer: `Adam`, Loss: `categorical_crossentropy`, Metric: `accuracy`
- **Evaluation**:
  - Test accuracy: **96.33%**

### 🔹 B. Shelf-Life Estimation

- **Advanced Augmentation** using `Albumentations`:
  - Noise, blur, brightness, flips, hue adjustments, etc.
- **CNN Regression Model**:
  - Output: Predicted shelf life (in days)
  - Loss: `Mean Absolute Error`, Optimizer: `Adam`
- **Training Strategies**:
  - Early stopping and learning rate reduction
- **Evaluation Metrics**:
  - MAE: **1.54 days**
  - RMSE: **2.19 days**

---

## 📊 Results

| Task                      | Performance                          |
|--------------------------|--------------------------------------|
| Freshness Score Accuracy | 96.33%                               |
| Shelf-Life Estimation    | ±2 days (MAE: 1.54, RMSE: 2.19)      |
| Classification Accuracy  | 88–91% across 20 produce types       |

---

## 🧪 Visual Examples

- Example:  
  - 🟢 Fresh Apple: 80.05%  
  - 🔴 Rotten Orange: 62.8%  
- Predictions are visualized using **Matplotlib** with class names and confidence levels.

---

## 📂 Dataset & Preprocessing

- Images normalized and augmented
- Categorical labels encoded
- Image size: **150x150**
- Train/Validation/Test split: **80/20**

---

## 🛠️ Tech Stack

- **Python**, **TensorFlow/Keras**, **Albumentations**, **Matplotlib**
- **Pre-trained Model**: InceptionV3
- **Web App Interface** (optional): Flask / Streamlit / Django

---

## 📦 Installation

```bash
git clone https://github.com/omshirode/Freshness-Detection-and-Shelf-Life-Prediction-for-Fruits-and-Vegetables.git
cd freshness-shelf-life-predictor
pip install -r requirements.txt
