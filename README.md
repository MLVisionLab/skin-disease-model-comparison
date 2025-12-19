
Comparison of CNN, CNN+LSTM, ResNet, MobileNet, YOLOv8 and Transformer models on a custom skin disease dataset

# Skin Disease Classification – Model Comparison

This repository presents a comparative study of multiple deep learning models
for classifying skin disease images using a custom dataset.

---

## 📂 Dataset Information

- Total images: **36,656**
- Number of classes: **14 skin disease categories**
- Dataset split:
  - Training: **29,322 (~80%)**
  - Validation: **3,660 (~10%)**
  - Test: **3,674 (~10%)**

The dataset follows a standard **80:10:10 split** to ensure fair evaluation.

---

## 🧠 Models Considered

- Basic CNN (from scratch)
- CNN + LSTM
- ResNet50 (Transfer Learning)
- MobileNet (Transfer Learning)
- YOLOv8 (Object Detection – reference)
- Vision Transformer (Conceptual comparison)

---

## ⭐ Best Model: ResNet50

- Pretrained on ImageNet
- Custom classification head added
- Fine-tuned top layers with a small learning rate

---

## 📊 Results

- **Final Validation Accuracy:** ~80%
- **Final Test Accuracy:** **80.05%**
- Stable training with no overfitting

---

## 📈 Accuracy & Loss Curves

<img width="1322" height="519" alt="Screenshot 2025-12-19 211314" src="https://github.com/user-attachments/assets/7999182b-0fc7-4e7b-964c-790e18b2071d" />


---

## 🏆 Conclusion

Among all evaluated approaches, **ResNet50 with transfer learning and fine-tuning**
performed the best on the custom dataset in terms of accuracy and stability.

---

## 👥 Team Members

- Member 1 – ResNet50 implementation & analysis
- Member 2 – CNN / CNN+LSTM
- Member 3 – MobileNet / YOLO research
- Member 4 – Documentation

---

## 🛠 Tools & Technologies

- Python
- TensorFlow / Keras
- Google Colab (Tesla T4 GPU)
- Matplotlib

---

## 📌 Note

Dataset images are not included due to Kaggle license restrictions.
