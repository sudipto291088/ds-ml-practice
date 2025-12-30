# Project 1 — Metric Stability & Statistical Intuition in ML

## Overview
This project explores **why machine learning performance metrics (Accuracy, RMSE) can be unstable with small datasets and become more reliable as data size increases**.

Instead of focusing on model optimization, my goal was to **build intuition** around:
- Metric variability
- Sampling effects
- Why cross-validation exists
- How statistics quietly underpins machine learning

The project uses the Titanic dataset to demonstrate these ideas through controlled experiments.

---

## Key Questions Addressed
- Why does the same model give different results on different runs?
- Why is a single train/test split unreliable?
- How does dataset size affect metric stability?
- How does this relate to statistical ideas like averaging and the Central Limit Theorem (intuition-level)?

---

## Dataset
- **Source:** Seaborn built-in Titanic dataset  
- **Why:** Simple, interpretable, and ideal for learning experimentation  
- **Targets:**
  - `survived` → Classification
  - `fare` → Regression

No external data files are required.

---

## Models & Metrics
Two separate problems were intentionally framed using the same dataset:

### Classification
- **Model:** Logistic Regression  
- **Target:** `survived` (0/1)  
- **Metric:** Accuracy  

### Regression
- **Model:** Linear Regression  
- **Target:** `fare`  
- **Metric:** RMSE  

The focus is **not** on maximizing these metrics, but on understanding how **stable** they are.

---

## Experimental Design
To isolate statistical effects:

- Same dataset
- Same features
- Same preprocessing
- Same models
- **Only sample size and random splitting change**

Experiments were run multiple times using:
- **10% of data** (small sample)
- **100% of data** (full dataset)

---

## Key Observations
- With **small samples**, metrics fluctuate wildly across runs.
- With **larger samples**, metrics cluster into a narrower range.
- High

