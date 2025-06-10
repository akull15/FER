# Facial Emotion Recognition System 🎭

A deep learning-based **real-time facial emotion recognition system** using CNNs trained on the FER-2013 dataset. The system detects human faces from a webcam and classifies their emotions into one of seven categories.

## 📌 Features
- ✅ Trained a **Convolutional Neural Network (CNN)** on the **FER-2013** dataset
- ✅ **Real-time facial expression detection** using **OpenCV** with a webcam
- ✅ Used **data augmentation** to improve model generalization
- ✅ Implemented **EarlyStopping** to prevent overfitting
- ✅ Fully self-contained: **data preprocessing → model training → live detection**

---

## 📁 Dataset
- **Dataset:** [FER-2013 Dataset](https://www.kaggle.com/datasets/msambare/fer2013)
- **Classes (7):** Angry, Disgust, Fear, Happy, Sad, Surprise, Neutral

---

## ⚙️ Requirements
Install the required Python libraries:

```bash
pip install numpy pandas tensorflow opencv-python matplotlib
