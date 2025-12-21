
Comparison of CNN, CNN+LSTM, ResNet, MobileNet, YOLOv8 and Transformer models on a custom skin disease dataset

# Skin Disease Classification – Model Comparison

This project presents a comprehensive comparison of multiple deep learning models
for **skin disease image classification** using a large custom dataset.
The objective is to identify the most accurate and stable model suitable for
real-world medical image classification.

---

## 📂 Dataset Overview

- **Total Images:** 36,656
- **Number of Classes:** 14 skin disease categories
- **Dataset Split:**
  - Training: 29,322 images (~80%)
  - Validation: 3,660 images (~10%)
  - Test: 3,674 images (~10%)

The dataset follows a proper **train–validation–test split**, ensuring fair
evaluation and preventing data leakage.

---

## 🧠 Models Evaluated

The following models were implemented and compared:

1. **Basic CNN (from scratch)**
2. **CNN + LSTM**
3. **ResNet50 (Transfer Learning)**
4. **MobileNet (Transfer Learning)**
5. **YOLOv8 (Object Detection – reference)**
6. **Vision Transformer (Conceptual comparison)**

---

## ⚙️ Training Strategy

- All CNN-based models were trained using supervised learning.
- Transfer learning models used ImageNet pretrained weights.
- Fine-tuning was applied where applicable using a low learning rate.
- EarlyStopping was used to prevent overfitting.
- Evaluation was done strictly on the **test dataset**.

---

## 📊 Model Performance Summary

| Model | Training Behavior | Validation Accuracy | Test Accuracy | Stability |
|-----|------------------|--------------------|---------------|-----------|
| Basic CNN | Slow convergence | ~65% | ~64–65% | Moderate |
| CNN + LSTM | Unnecessary complexity | ~60–62% | ~60% | Low |
| **ResNet50** | Smooth convergence | **~80%** | **80.05%** | **High** |
| MobileNet | Fast & lightweight | ~70–73% | ~72% | High |
| YOLOv8 | Detection-focused | N/A | N/A | Not comparable |
| Transformer | Very slow, unstable | < ResNet | Not reliable | Low |

---

## 📈 Accuracy & Loss Curves

### 🔹 CNN (From Scratch)
- Gradual learning
- Lower ceiling on accuracy
- No overfitting, but limited representation power

### 🔹 CNN + LSTM
- Increased complexity
- No meaningful accuracy improvement
- LSTM unsuitable for static image data

### 🔹 ResNet50 (Transfer Learning)
- Smooth increase in training & validation accuracy
- Steady loss reduction
- Validation accuracy closely follows training accuracy
- Indicates **excellent generalization**

📌 **ResNet50 Accuracy & Loss**
