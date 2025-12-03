---
layout: post_math
title: Confusion matrix
date: 2025-12-03 9:00:00 +0530
categories: jekyll tutorial

---

While learning Machine Learning, it is common to assume that **accuracy** is the ultimate measure of model performance.  
However, I learned the hard way that **accuracy alone can be misleading**. Looking at accuracy over each training iteration helps determine whether a model is **truly learning** or simply **memorizing / guessing**.

To correctly evaluate a classification model, we need to understand different performance metrics derived from the **confusion matrix**.

---

## Confusion Matrix Overview

|                       | **Predicted Positive** | **Predicted Negative**   |
|-----------------------|-------------------------|-------------------------|
| **Actual Positive**   | True Positive (TP)      | False Negative (FN)     |
| **Actual Negative**   | False Positive (FP)     | True Negative (TN)      |

---

## Key Metrics

### **Accuracy**
> Measures how many predictions are correct overall.

$$
\text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN}
$$

---

### **Precision**
> Out of everything the model predicted as positive, how many were actually positive?

$$
\text{Precision} = \frac{TP}{TP + FP}
$$

---

### **Recall (Sensitivity / True Positive Rate)**
> Out of all actual positive cases, how many did the model correctly identify?

$$
\text{Recall} = \frac{TP}{TP + FN}
$$

---

### **F1-Score**
> The harmonic mean of Precision and Recall — useful when the dataset is imbalanced.

$$
\text{F1} = 2 \times \frac{Precision \times Recall}{Precision + Recall}
$$

---

## Why These Metrics Matter
- **Accuracy can lie** in cases with **imbalanced datasets** (e.g., 95% accuracy but only predicting the majority class).
- **Precision vs Recall trade-off** tells us whether the model is cautious or aggressive.
- **F1-score** balances both, giving a single metric for comparison.

---

### Takeaway
Evaluating an ML model requires more than just accuracy.  
Understanding **precision, recall, and F1-score** helps determine whether a model is **reliable, fair, and actually learning**.

---


