# 🧠 Handwritten Digit Classification

This project demonstrates a machine learning pipeline for classifying handwritten digits using the [Scikit-learn Digits Dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_digits.html). Various models were trained and evaluated, with a focus on **Random Forest**, which was fine-tuned and analyzed using a confusion matrix.

---

## 📊 Dataset Overview

- **Samples**: 1,797 grayscale images
- **Image size**: 8x8 pixels
- **Classes**: Digits from 0 to 9

Each image is represented by 64 features (pixel intensity values) and a label indicating the digit.

---

## 🛠 Models Trained

The following classifiers were trained using **10-fold cross-validation**:

| Model                     | Accuracy (%) |
|---------------------------|--------------|
| Logistic Regression       | 92.82        |
| Random Forest (n=40)      | 94.66        |
| Support Vector Classifier | 96.99        |

### ✅ Fine-Tuning Random Forest

We optimized the Random Forest classifier by setting `n_estimators = 40`. This configuration achieved strong accuracy with relatively low computational cost.

---

## 📌 Confusion Matrix (Random Forest)

The following confusion matrix shows the performance of the fine-tuned Random Forest model on the test data:

You can check it out on the code.

### 🔍 Observations

- Most digits are correctly classified (values along the diagonal).
- Minor confusions occur between:
  - **4 vs. 8/9**
  - **5 vs. 9**
  - **8 vs. 1**
- These confusions are expected due to the visual similarity between handwritten digits.

---

## 🚀 How to Run

1. Clone the repository or copy the notebook.
2. Install required packages:
   ```bash
   pip install scikit-learn matplotlib seaborn

