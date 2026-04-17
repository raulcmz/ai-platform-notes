# Confusion Matrix Explained

## The real problem

Accuracy alone is misleading.

A model can be "accurate" while completely failing on the cases that matter.

So we need a better way to understand predictions.

---

## What is a confusion matrix?

A confusion matrix shows how your model predictions compare to the actual values.

It breaks predictions into four categories:

- True Positives (TP)
- True Negatives (TN)
- False Positives (FP)
- False Negatives (FN)

---

## The intuition

Think of a medical test:

- Positive → patient has the disease
- Negative → patient does not

Now the model makes predictions.

The confusion matrix tells you where it gets it right and where it fails.

---

## Visual representation

(we will add a diagram here)

---

## The four components

### True Positive (TP)
Model predicts positive and it's correct

### True Negative (TN)
Model predicts negative and it's correct

### False Positive (FP)
Model predicts positive but it's wrong

### False Negative (FN)
Model predicts negative but it's wrong

---

## Why this matters

Not all errors are equal.

- False positives → annoying
- False negatives → dangerous

---

## From confusion matrix to metrics

From these four numbers, we derive:

- Accuracy
- Precision
- Recall
- F1-score

---

## Example

(we will add numbers + small table)

---

## Code example

```python
from sklearn.metrics import confusion_matrix

y_true = [0, 1, 0, 1, 1, 0]
y_pred = [0, 1, 0, 0, 1, 1]

cm = confusion_matrix(y_true, y_pred)
print(cm)
```

## Visual walkthrough

<video controls width="100%" preload="metadata" style="border-radius: 12px;">
  <source src="../../assets/videos/confusion-matrix.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>


## Key takeaway

A confusion matrix tells you not just how often your model is right,
but how it is wrong.

That is what really matters in ML systems.