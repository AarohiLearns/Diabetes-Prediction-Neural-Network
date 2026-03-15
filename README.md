# 🏥 Diabetes Prediction Using Neural Networks

A binary classification model to predict diabetes in patients using clinical features, built using TensorFlow and Keras.

---

## 📌 Problem Statement

Diabetes affects millions of people worldwide. Early detection can help prevent serious complications. This model predicts whether a patient is diabetic or not based on clinical measurements.

---

## 🎯 What This Model Predicts

| Output | Meaning |
|--------|---------|
| 1 | Diabetic |
| 0 | Not Diabetic |

> ⚠️ This is a prediction tool for early screening only — not a medical diagnosis. Always consult a doctor.

---

## 📊 Dataset

- **Name:** Pima Indians Diabetes Dataset
- **Source:** Kaggle
- **Rows:** 768
- **Features:** 8 clinical features

| Feature | Description |
|---------|-------------|
| Glucose | Blood glucose level |
| BloodPressure | Diastolic blood pressure |
| BMI | Body mass index |
| Age | Age of patient |
| Insulin | Insulin level |
| SkinThickness | Skin fold thickness |
| DiabetesPedigreeFunction | Family history score |
| Pregnancies | Number of pregnancies |

---

## ⚙️ Tech Stack

```
Language:   Python
Libraries:  NumPy, Pandas, Matplotlib
            Scikit-learn, TensorFlow
Platform:   Google Colab
```

---

## 🧠 Model Architecture

```
Input Layer    → 8 features
Dense Layer 1  → 64 neurons, ReLU, L2
BatchNorm 1    → Normalize outputs
Dropout 1      → 30% dropout
Dense Layer 2  → 32 neurons, ReLU, L2
BatchNorm 2    → Normalize outputs
Dropout 2      → 30% dropout
Dense Layer 3  → 16 neurons, ReLU, L2
BatchNorm 3    → Normalize outputs
Dropout 3      → 20% dropout
Dense Layer 4  → 8 neurons, ReLU
Dropout 4      → 20% dropout
Output Layer   → 1 neuron, Sigmoid
```

---

## 🔧 Training Details

```
Optimizer:        Adam (lr=0.001)
Loss:             Binary Crossentropy
Epochs:           100
Batch Size:       32
Validation Split: 15%
EarlyStopping:    patience=15
ReduceLROnPlateau: factor=0.5
```

---

## 📈 Results

| Metric | Value |
|--------|-------|
| **Accuracy** | **77%** |
| Precision (Non-Diabetic) | 0.82 |
| Precision (Diabetic) | 0.69 |
| F1 Score (weighted) | 0.77 |

### Confusion Matrix

```
              Predicted
              0    1
Actual  0  [ 82   17 ]
        1  [ 18   37 ]
```

---

## 🔬 ML Pipeline

```
Raw Dataset
    ↓
EDA + Data Info
    ↓
Train / Test Split (80/20)
    ↓
StandardScaler
    ↓
Build Neural Network
    ↓
Train with EarlyStopping
    ↓
Evaluate on Test Data
    ↓
Accuracy + Confusion Matrix
```

---

## 📁 Project Structure

```
Diabetes-Prediction/
│
├── DNNLCA1PROJECT.ipynb   ← Main Colab notebook
├── diabetes.csv           ← Dataset
└── README.md
```

---

## 📚 References

1. Pima Indians Diabetes Dataset — Kaggle
2. TensorFlow Documentation
3. Scikit-learn Documentation

---

## 👨‍💻 Author

Made for early diabetes screening research
