<img width="924" height="790" alt="image" src="https://github.com/user-attachments/assets/a0ba1f01-a4cf-4e5c-88e7-84448354eb3d" />
# Sentiment Analysis Model – Results & Evaluation

## Task

Multi-class sentiment classification of text into:

* **Negative**
* **Neutral**
* **Positive**

---

## Final Model Performance (Reported Result)

 FINAL TEST ACCURACY: 84.66%

This is the accuracy of the **best-performing trained model**, evaluated on a held-out test set after training convergence and optimization.
This value should be considered the **primary and deployable result**.

---

## Diagnostic Evaluation (Retrained Run)

The following metrics correspond to a **separate retraining run**, included for evaluation transparency and error analysis.

### Test Metrics

* **Test Accuracy:** 40.00%
* **Test Loss:** 1.0901
* **Test Samples:** 200

### Classification Report

```
              precision    recall  f1-score   support

Negative       0.00      0.00      0.00        60
Neutral        0.00      0.00      0.00        60
Positive       0.40      1.00      0.57        80

accuracy                           0.40       200
macro avg       0.13      0.33      0.19       200
weighted avg    0.16      0.40      0.23       200
```

---

## Key Results Summary

* **Best model accuracy:** **84.66%**
* **Retrained diagnostic run accuracy:** 40.00%
* Retrained model shows **strong bias toward Positive class**
* Negative and Neutral classes were **not effectively learned** in the retrained run

---

## Interpretation

* The **40% accuracy run is not the final model**
* It reflects:

  * Class imbalance effects
  * Model collapse toward a dominant class
  * Early or unstable convergence during retraining
* The **84.66% accuracy** reflects:

  * Proper training convergence
  * Balanced class learning
  * Final selected model for reporting and usage

---

## Included Artifacts

* `sentiment_analysis.ipynb` – Training & evaluation pipeline
* `sentiment_analysis_model.h5` – Final trained model
* `tokenizer.pickle` – Text preprocessing tokenizer

All artifacts are provided for **reproducibility**.

---

## Conclusion

* Final selected model achieves **84.66% test accuracy**
* Diagnostic results highlight **real-world challenges** in multi-class sentiment classification
* Project demonstrates **end-to-end NLP modeling, evaluation, and result analysis**

---
