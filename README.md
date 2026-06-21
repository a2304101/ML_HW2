# ML_HW2 - Bayesian Learning and Logistic Regression

## Overview

This project was completed for a Machine Learning course in 2017.

The homework focuses on probabilistic machine learning and statistical inference, including:

1. Bayesian Inference for Gaussian Distributions
2. Bayesian Linear Regression
3. Multiclass Logistic Regression using Newton-Raphson Optimization

The project emphasizes Bayesian learning, parameter estimation, predictive uncertainty, and classification.

---

# Part 1 — Bayesian Inference for Gaussian Distribution

## Objective

Estimate the covariance structure of a multivariate Gaussian distribution using Bayesian learning.

Instead of estimating parameters using traditional maximum likelihood estimation, a prior distribution is introduced and updated as new observations arrive.

---

## Topics

### Precision Matrix

The precision matrix is defined as:

```text
Λ = Σ⁻¹
```

where:

```text
Σ = covariance matrix
```

---

### Bayesian Sequential Learning

Posterior distribution is updated incrementally:

```text
p(Λ|X)
```

using newly observed samples.

This demonstrates online Bayesian learning instead of batch estimation.

---

### Prior Distribution

Wishart Distribution:

```text
p(Λ) = W(Λ|W0, ν0)
```

was used as the conjugate prior.

---

### MAP Estimation

MAP estimates were computed under different sample sizes:

```text
N = 10
N = 100
N = 500
```

to observe the effect of data quantity on posterior estimation.

---

# Part 2 — Bayesian Linear Regression

## Objective

Apply Bayesian inference to linear regression and investigate parameter uncertainty and predictive uncertainty.

---

## Dataset

Input:

```text
x ∈ [0, 2]
```

Target:

```text
t
```

100 samples.

---

## Basis Functions

Sigmoidal basis functions:

```text
φj(x) = σ((x-μj)/s)
```

Parameters:

```text
M = 7
s = 0.1
```

---

## Bayesian Formulation

Posterior distribution:

```text
p(w|t) = N(mN, SN)
```

Prior:

```text
p(w)=N(0, 10⁶I)
```

Likelihood precision:

```text
β = 1
```

---

## Experiments

The regression model was evaluated under:

```text
N = 10
N = 15
N = 30
N = 80
```

training samples.

---

## Posterior Sampling

Random parameter vectors were sampled from:

```text
N(mN, SN)
```

to visualize uncertainty in model parameters.

---

## Predictive Distribution

The predictive mean and predictive variance were computed.

Visualization included:

- Mean prediction curve
- One standard deviation confidence region

This illustrates how uncertainty decreases as more training data become available.

---

# Part 3 — Multiclass Logistic Regression

## Objective

Implement multiclass logistic regression from scratch using Newton-Raphson optimization.

---

## Dataset

Wine Dataset

Classification problem with:

```text
3 classes
```

using:

```text
1-of-K encoding
```

for target labels.

---

## Softmax Function

Class probabilities are modeled by:

```text
P(Ck|x)
=
exp(ak)
/
Σ exp(aj)
```

---

## Loss Function

Cross Entropy:

```text
E(w)
=
− Σ Σ tnk log(ynk)
```

---

## Optimization

Newton-Raphson algorithm was implemented to iteratively update model parameters until convergence.

Stopping criterion:

```text
E(w) < ε
```

---

## Experiments

### Learning Curve

Monitor:

- Cross Entropy Loss
- Classification Accuracy

over training epochs.

---

### Test Classification

Evaluate classification performance on unseen test samples.

---

### Feature Distribution Analysis

Histogram analysis was performed for each feature.

Different colors were used to distinguish class distributions.

---

### Global Minimum Discussion

Analyze convergence behavior and verify whether optimization is approaching the global minimum.

---

# Bonus

## Feature Importance Analysis

Identify the most discriminative feature pair.

---

## Reduced Feature Training

Retrain logistic regression using only the selected feature pair and compare performance.

---

# Skills Demonstrated

## Machine Learning

- Bayesian Inference
- Bayesian Learning
- Maximum A Posteriori Estimation
- Bayesian Linear Regression
- Logistic Regression
- Softmax Classification
- Newton-Raphson Optimization

## Statistics

- Gaussian Distribution
- Wishart Distribution
- Posterior Distribution
- Predictive Distribution
- Uncertainty Quantification

## Data Analysis

- Classification Evaluation
- Feature Distribution Analysis
- Feature Selection
- Learning Curve Analysis

---

# What I Learned

Through this project, I gained practical experience with Bayesian machine learning and probabilistic modeling.

The homework strengthened my understanding of:

- Bayesian parameter estimation
- Posterior and predictive distributions
- Uncertainty-aware regression
- Multiclass classification using Softmax regression
- Newton-Raphson optimization
- Statistical interpretation of machine learning models

These concepts provide the mathematical foundation for modern machine learning, probabilistic models, and Bayesian deep learning methods.
