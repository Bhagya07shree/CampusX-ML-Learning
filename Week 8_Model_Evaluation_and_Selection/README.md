# Model Evaluation & Selection – Learning Summary

This README documents the **core model evaluation, selection, and tuning concepts** I have learned and applied in machine learning projects.

---

## 1. Model Evaluation

**Definition**: Measuring how well a trained model performs using appropriate metrics.

### Topics Covered

* Confusion Matrix
* Accuracy, Precision, Recall, F1-score
* ROC Curve
* TPR (True Positive Rate)
* FPR (False Positive Rate)
* Threshold concept and threshold movement
* ROC Curve interpretation
* AUC–ROC (concept and usage)

**Key Focus**:

* Why metrics matter
* When accuracy fails
* Choosing metrics based on problem type

---

## 2. Threshold Selection

**Goal**: Choosing the best decision threshold instead of default 0.5.

### Methods Studied

* Top-left corner of ROC curve
* Youden’s J statistic (TPR − FPR)
* Business-defined constraints

  * High recall for medical diagnosis
  * Low FPR for fraud detection

**Key Insight**:
Threshold selection depends on **cost of errors**, not just accuracy.

---

## 3. Model Selection

**Definition**: Choosing the best model or configuration after evaluation.

### Covered Concepts

* Difference between model evaluation and model selection
* Comparing multiple algorithms
* Selecting best hyperparameter configuration
* Why test data should not be used for selection

---

## 4. Data Splitting Strategy

### Datasets Used

* Training set
* Validation set
* Test set

**Key Understanding**:

* Training → learns parameters
* Validation → tunes hyperparameters
* Test → final unbiased evaluation

---

## 5. Hold-Out Validation

### What Was Learned

* Simple train–test split
* Problems with hold-out method:

  * High variance
  * Data inefficiency
* Role of `random_state`
* Why randomness affects results

---

## 6. Cross-Validation

**Purpose**: Robust model evaluation.

### Concepts Covered

* Why cross-validation is needed
* k-fold cross-validation workflow
* Averaging performance across folds
* Reuse of data without leakage

### Types Studied

* k-fold cross-validation
* Stratified k-fold cross-validation
* Leave-One-Out Cross-Validation (LOOCV)

**Industry Note**:
Stratified k-fold is preferred for classification problems.

---

## 7. Data Leakage

### Understanding the Problem

* What data leakage is
* Why it is dangerous
* How it gives unrealistic performance

### Common Causes

* Scaling before data splitting
* Feature engineering using future data
* Using test data during training or tuning

### Prevention Techniques

* Proper train/validation/test separation
* Pipeline-based preprocessing
* Cross-validation-safe workflows

---

## 8. Pipelines

**Purpose**: Prevent data leakage and ensure reproducibility.

### What Was Learned

* What pipelines are
* Why pipelines are important
* Combining preprocessing and model
* Pipelines with cross-validation

---

## 9. Hyperparameters

### Concepts Covered

* Difference between parameters and hyperparameters
* Why the term "hyper" is used
* Types of hyperparameters:

  * Model hyperparameters
  * Optimization hyperparameters
  * Regularization hyperparameters

---

## 10. Hyperparameter Tuning

### Techniques Studied

* GridSearchCV
* RandomizedSearchCV

### Key Learnings

* Role of cross-validation in tuning
* Advantages and disadvantages of each method
* Why RandomizedSearchCV is preferred in practice
* Avoiding overfitting during tuning

---

## 11. Nested Cross-Validation (Conceptual)

### Understanding

* Inner loop: hyperparameter tuning
* Outer loop: model evaluation
* Prevents optimistic bias
* Mostly interview-level concept

---


