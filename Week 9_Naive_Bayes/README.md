#  Naive Bayes – Probability Foundations & Interview Preparation

##  Overview

This repository documents my structured learning of **Probability Theory and the Naive Bayes Algorithm**, building a strong mathematical foundation for Machine Learning.

The goal of this study was to:

- Understand probability concepts from first principles
- Learn the intuition and mathematics behind Naive Bayes
- Build strong interview-ready explanations
- Connect theory with practical ML implementation

---

# 1️⃣ Probability Foundations

## 🔹 Random Experiment
An experiment whose outcome cannot be predicted with certainty.

## 🔹 Trial
A single execution of a random experiment.

## 🔹 Outcome
A possible result of an experiment.

## 🔹 Sample Space
The set of all possible outcomes.

Example (Coin Toss):

S = {H, T}

## 🔹 Event
A subset of the sample space.

---

# 2️⃣ Types of Probability

##  Empirical Probability
Based on observed data.

P(E) = (Number of times event occurs) / (Total number of trials)

##  Theoretical Probability
Based on mathematical reasoning.

P(E) = (Favorable outcomes) / (Total possible outcomes)

---

# 3️⃣ Random Variables

A **Random Variable** is a function that maps outcomes of a sample space to real numbers.

Example:

| Outcome | X |
|----------|---|
| Head     | 1 |
| Tail     | 0 |

---

# 4️⃣ Probability Distribution

A probability distribution assigns probabilities to values of a random variable.

Example:

| X | P(X) |
|---|------|
| 0 | 0.5  |
| 1 | 0.5  |

---

# 5️⃣ Expected Value (Mean)

E(X) = Σ xᵢ P(xᵢ)

It represents the long-run average value.

---

# 6️⃣ Variance

Var(X) = E[(X − μ)²]

Variance measures how spread out the distribution is.

---

# 7️⃣ Joint, Marginal & Conditional Probability

## Joint Probability
P(A ∩ B)

Probability of A and B occurring together.

##  Marginal Probability
P(A)

Probability of a single event.

##  Conditional Probability

P(A|B) = P(A ∩ B) / P(B)

Probability of A given B has occurred.

---

# 8️⃣ Bayes Theorem

Bayes theorem updates prior belief after observing evidence.

P(A|B) = [P(B|A) P(A)] / P(B)

Where:

- P(A) → Prior
- P(B|A) → Likelihood
- P(A|B) → Posterior

---

# 9️⃣ Naive Bayes Algorithm

Naive Bayes is a **probabilistic classification algorithm** based on Bayes theorem.

It assumes:

> Features are conditionally independent given the class.

##  Formula

P(Y|X) ∝ P(Y) × Π P(Xᵢ | Y)

Where:

- P(Y) → Class prior
- P(Xᵢ | Y) → Likelihood of feature given class

---

# 🔟 Training vs Testing

## Training Phase

The model computes:

- Class priors: P(Y)
- Conditional probabilities: P(Xᵢ | Y)

##  Testing Phase

For a new input:

1. Compute posterior probability for each class
2. Compare probabilities
3. Choose class with highest value

---

# 1️⃣1️⃣ Numerical Underflow & Log Trick

Multiplying many small probabilities can cause **numerical underflow**.

Solution:

log P(Y|X) = log P(Y) + Σ log P(Xᵢ | Y)

Multiplication becomes addition → numerically stable.

---

# 1️⃣2️⃣ Laplace (Additive) Smoothing

Used to prevent **zero probability problem**.

Without smoothing:
If a word never appears in a class → probability becomes 0 → entire posterior becomes 0.

With smoothing:

For Multinomial NB:

P(word|class) = (count + α) / (total_words + αV)

Where:
- α → smoothing parameter
- V → vocabulary size

---

# 1️⃣3️⃣ Bias–Variance Effect of α

| α Value | Effect |
|----------|--------|
| α = 0 | High variance, overfitting |
| Small α | Balanced generalization |
| Very large α | High bias, probabilities become uniform |

---

# 1️⃣4️⃣ Types of Naive Bayes

## Gaussian Naive Bayes
Used when features are continuous and assumed to follow a normal distribution.

##  Bernoulli Naive Bayes
Used for binary features (0 or 1).

- Models both presence and absence
- Suitable for short text

## Multinomial Naive Bayes
Used for text classification.

- Uses word frequency counts
- Suitable for longer documents

---

# 1️⃣5️⃣ Bernoulli vs Multinomial

| Bernoulli NB | Multinomial NB |
|--------------|----------------|
| Binary features | Count features |
| Models absence | Ignores absence |
| Frequency ignored | Frequency matters |
| Good for short text | Good for long text |

---

# 1️⃣6️⃣ Sparse Data

Text data is usually **high-dimensional and sparse**.

- Large vocabulary
- Most feature values are zero

Naive Bayes performs efficiently in sparse environments.

---

# 1️⃣7️⃣ Important Interview Question

###  Why does Naive Bayes work even though the independence assumption is false?

Even when features are dependent, Naive Bayes often performs well because:

- It focuses on estimating decision boundaries.
- Classification depends on comparing class probabilities.
- Independence assumption reduces variance.
- Works extremely well in high-dimensional text data.

---

# 1️⃣8️⃣ Key Learnings

Through this study, I strengthened my understanding of:

- Probability theory for ML
- Bayes theorem intuition
- Naive Bayes derivation
- Training vs testing workflow
- Log transformation for stability
- Laplace smoothing & bias-variance tradeoff
- Gaussian vs Bernoulli vs Multinomial NB
- Sparse text classification

---

##  Conclusion

Naive Bayes provides a strong mathematical foundation for probabilistic machine learning models and performs exceptionally well in text classification tasks.
