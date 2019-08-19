## [Tactics to combat imbalanced training data](https://machinelearningmastery.com/tactics-to-combat-imbalanced-classes-in-your-machine-learning-dataset/)

### 1. Collect more data
### 2. Change the performance metric 
see the [Classification Accuracy Performance Measure](https://machinelearningmastery.com/classification-accuracy-is-not-enough-more-performance-measures-you-can-use/)
#### - Confusion Matrix
A breakdown of predictions into a table showing correct predictions (the diagonal) and the types of incorrect predictions made (what classes incorrect predictions were assigned).
#### - Precision
 A measure of a classifiers exactness.
#### - Recall
A measure of a classifiers completeness
#### - F1 Score
A weighted average of precision and recall.


|                     |    class 1     |    class 2      |
| ------------------- | -------------- | --------------- |
|True label (class 1) | true positive (TP1) | false positive (FP2) |
|True label (class 2) | false positive (FP1) | true positive (TP2) |  

Micro-average of Accuracy = ${(TP1 + TP2) \over TP1+TP2+FP1+FP2}$
Micro-average of Recall ${(TP1 + TP2) \over TP1+TP2+FN1+FN2}$

Macro-average of Accuracy = ${(P1 + P2) \over 2}$
Macro-average of Recall ${(R1 + R2) \over 2}$

Class 1 Precision ${(TP1) \over TP1+FP1}$ Class 2 Precision ${(TP2) \over TP2+FP2}$

Class 1 Recall ${(TP1) \over TP1+FP2}$ Class 2 Recall ${(TP2) \over TP2+FP1}$

- Kappa
- [ROC Curves](https://machinelearningmastery.com/assessing-comparing-classifier-performance-roc-curves-2/)

Like precision and recall, accuracy is divided into sensitivity and specificity and models can be chosen based on the balance thresholds of these values.

### 3. Try Resampling Your Dataset

#### Some Rules of Thumb
- Consider testing under-sampling when you have an a lot data (tens- or hundreds of thousands of instances or more)
- Consider testing over-sampling when you don’t have a lot of data (tens of thousands of records or less)
- Consider testing random and non-random (e.g. stratified) sampling schemes.
- Consider testing different resampled ratios (e.g. you don’t have to target a 1:1 ratio in a binary classification problem, try other ratios)

### 4. Try Generate Synthetic Samples

- SMOTE (Synthetic Minority Over-sampling Technique)

See the paper titled “SMOTE: Synthetic Minority Over-sampling Technique”

### 5. Try Different Algorithms

### 6. Try Penalized Models

- Weka - Cost Sensitive Classifier