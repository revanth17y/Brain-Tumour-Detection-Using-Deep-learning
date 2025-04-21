# 🧠 Brain Tumor Classification with CNN (MobileNetV2 + Mixed Precision)

This project uses a Convolutional Neural Network built on top of MobileNetV2 for classifying brain tumor images into four categories. It includes real-time predictions, a confusion matrix, and performance metrics. The model is trained using TensorFlow with mixed precision for enhanced performance.

---

## 🚀 Features

- Transfer learning with MobileNetV2
- Mixed precision training
- Custom image prediction
- Evaluation with confusion matrix and classification report
- Automatic training continuation using a saved `.h5` model
- Live testing via user input

---

## 🗂️ Dataset Structure

Place the dataset in the following structure:

```
BrainTumor/
├── dataset/
│   ├── Training/
│   │   ├── Class1/
│   │   ├── Class2/
│   │   ├── ...
│   ├── Testing/
│   │   ├── Class1/
│   │   ├── Class2/
│   │   ├── ...
```

> Replace `Class1`, `Class2`, etc., with your actual category names.

---

## ⚙️ Installation

1. Clone the repo:
```bash
git clone https://github.com/your-username/brain-tumor-classification.git
cd brain-tumor-classification
```

2. Create and activate a virtual environment (recommended).

3. Install dependencies:
```bash
pip install -r requirements.txt
```

---

## 🧪 Running the Model

```bash
python brain_tumor_classifier.py
```

You'll be prompted to enter image paths for predictions. Type `exit` to end the loop.

---

## 🧠 Model Architecture

- **Base:** MobileNetV2 (ImageNet weights, frozen)
- **Added Layers:**
  - GlobalAveragePooling2D
  - Dense(256, ReLU) + Dropout(0.2)
  - Dense(128, ReLU) + Dropout(0.4)
  - Dense(4, Softmax)

---

## 📊 Evaluation Metrics

- **Accuracy**
- **Confusion Matrix**
- **Classification Report**

---

## 📦 Requirements

```
tensorflow>=2.11
numpy
pandas
matplotlib
seaborn
scikit-learn
Pillow
```

---

## 🧾 License

This project is licensed under the MIT License. Feel free to use and adapt it.
