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

## ⚙️ How It Works

1. **Data Preprocessing:**
   - The FER-2013 dataset contains grayscale images (48x48) of human faces, labeled with one of seven emotions.
   - Images are normalized to the range [0,1] and reshaped for input into the CNN.

2. **Data Augmentation:**
   - The training data is augmented with random rotations, shifts, zooms, and flips to improve the model's generalization to new images.

3. **Model Architecture:**
   - **3 Convolutional Blocks** with:
     - Conv2D → BatchNormalization → MaxPooling → Dropout
   - **Fully Connected Dense Layers:**
     - Flatten → Dense → Dropout → Dense (softmax activation)
   - **Regularization:**
     - **Dropout layers** help prevent overfitting.
     - **Batch Normalization** stabilizes learning and improves performance.
   - **Optimizer & Loss:**
     - Optimizer: Adam
     - Loss Function: Categorical Crossentropy (for multi-class classification)

4. **Training:**
   - Model is trained with **early stopping** to halt if validation loss stops improving.
   - **Training time:** ~10-20 minutes on CPU depending on your machine, faster with GPU.

5. **Real-time Detection:**
   - The trained model is loaded.
   - OpenCV detects faces in real-time via webcam.
   - Detected faces are processed and classified into one of 7 emotion categories.
   - The predicted emotion and confidence are overlaid on the video feed.
