# 🧠 CIFAR-10 Image Classifier with CNN

![Python](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-Deep%20Learning-D00000?style=for-the-badge&logo=keras&logoColor=white)
![Accuracy](https://img.shields.io/badge/Test%20Accuracy-68.68%25-brightgreen?style=for-the-badge)

> A **Convolutional Neural Network (CNN)** trained on the CIFAR-10 dataset to classify images into 10 categories — built with TensorFlow/Keras and data augmentation for improved generalization.

---

## 📸 What Does It Classify?

The model recognizes **10 object categories** from 32×32 color images:

| Label | Class      | Label | Class       |
|-------|------------|-------|-------------|
| 0     | ✈️ Airplane  | 5     | 🐶 Dog       |
| 1     | 🚗 Automobile | 6     | 🐸 Frog      |
| 2     | 🐦 Bird      | 7     | 🐴 Horse     |
| 3     | 🐱 Cat       | 8     | 🚢 Ship      |
| 4     | 🦌 Deer      | 9     | 🚛 Truck     |

---

## 🏗️ Model Architecture

```
Input (32×32×3)
     │
     ▼
Conv2D(32 filters, 3×3) → ReLU
     │
MaxPooling2D(2×2)
     │
Conv2D(64 filters, 3×3) → ReLU
     │
MaxPooling2D(2×2)
     │
Flatten → Dense(64) → ReLU
     │
Dense(10) → Softmax
```

- **Optimizer:** Adam  
- **Loss:** Sparse Categorical Crossentropy  
- **Metrics:** Accuracy

---

## 📊 Training Results

| Epoch | Train Accuracy | Val Accuracy | Val Loss |
|-------|---------------|--------------|----------|
| 1     | 42.52%        | 50.48%       | 1.3841   |
| 3     | 57.88%        | 62.27%       | 1.0897   |
| 5     | 61.86%        | 66.88%       | 0.9572   |
| 8     | 65.46%        | 67.05%       | 0.9484   |
| **10**| **66.57%**    | **68.68%**   | **0.9162** |

> 📈 Steady improvement across all 10 epochs — val accuracy climbed from ~50% → ~69%

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install tensorflow numpy matplotlib
```

### Run the Notebook

```bash
jupyter notebook cifar10_cnn.ipynb
```

Or run as a Python script:

```bash
python cifar10_cnn.py
```

> The CIFAR-10 dataset (~170MB) is automatically downloaded on first run via `keras.datasets`.

---

## 🔧 Key Features

- ✅ **Built-in dataset** — no manual download needed
- ✅ **Data Augmentation** — rotation, horizontal flip, zoom to reduce overfitting
- ✅ **Pixel Normalization** — scales values from [0–255] → [0–1]
- ✅ **Validation tracking** — monitors val accuracy every epoch

---

## 💡 Ideas to Improve Further

- [ ] Add **Dropout layers** to reduce overfitting
- [ ] Use **Batch Normalization** between conv blocks
- [ ] Try a deeper architecture or **transfer learning** (e.g., MobileNetV2)
- [ ] Increase epochs with a **learning rate scheduler**
- [ ] Visualize misclassified images for error analysis

---

## 📁 Project Structure

```
📦 cifar10-cnn/
 ┣ 📓 cifar10_cnn.ipynb      # Main Jupyter notebook
 ┣ 📜 cifar10_cnn.py         # Python script version
 ┗ 📄 README.md              # You're here!
```

---

## 🙋 Author

**Bavesh** — AI/ML enthusiast building real-world deep learning projects.  
Feel free to ⭐ the repo if you found it useful!

---
