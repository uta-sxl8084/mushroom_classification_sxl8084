# Mushroom Classification Project

## One Sentence Summary

This repository applies machine learning models to classify mushrooms as edible or poisonous using the Kaggle Mushroom Classification dataset: https://www.kaggle.com/datasets/uciml/mushroom-classification

---

# Overview

### Task Definition

The task is to classify mushrooms as edible or poisonous based on their physical characteristics. This is a binary classification problem using tabular data with categorical features.

### Approach

The problem is formulated as a supervised classification task. All categorical features were encoded using one-hot encoding, and multiple models were trained, including Logistic Regression, Decision Tree, and Random Forest. Performance was evaluated using accuracy, ROC-AUC, and confusion matrix.

### Performance Summary

All models achieved near-perfect accuracy due to the highly separable nature of the dataset. Random Forest performed best, achieving approximately 100% accuracy on the validation set.

---

# Summary of Work Done

## Data

### Type

* Input: CSV file of categorical features describing mushroom characteristics
* Output: Binary classification label (`class`: edible = 0, poisonous = 1)

### Size

* Total samples: 8124
* Features: 23

### Split

* Training: 80%
* Validation: 20%
* No separate test set provided

---

## Preprocessing / Clean Up

* Replaced missing values (`?`) with NaN
* Removed rows with missing values
* Converted target labels (`e`, `p`) into numerical format (0, 1)
* Applied one-hot encoding to all categorical features

---

## Data Visualization

* Count plots were used instead of histograms since all features are categorical
* Visualizations showed strong separation between classes
* Features such as **odor** clearly distinguish edible vs poisonous mushrooms

---

# Problem Formulation

### Input / Output

* Input: Encoded categorical features
* Output: Binary classification (0 = edible, 1 = poisonous)

### Models Used

* Logistic Regression
* Decision Tree
* Random Forest

Random Forest was selected as the primary model due to its strong performance on categorical data.

---

## Training

### Method

* Models trained using Scikit-learn
* Stratified train-validation split used

### Training Details

* Training was fast due to small dataset size
* No GPU required

### Stopping Criteria

* Models trained until completion (no iterative epochs required for tree models)

---

## Performance Comparison

### Metrics Used

* Accuracy
* ROC-AUC
* Confusion Matrix

### Results

| Model               | Accuracy |
| ------------------- | -------- |
| Logistic Regression | ~1.00    |
| Decision Tree       | ~1.00    |
| Random Forest       | ~1.00    |

### Observations

* Random Forest performed best overall
* Dataset is highly separable
* Very few classification errors

---

## Conclusions

* The dataset is highly predictable due to strong feature separation
* Features such as odor dominate classification
* Ensemble models like Random Forest perform best

---

## Future Work

* Hyperparameter tuning
* Testing on more complex or noisy datasets
* Applying boosting algorithms

---

# How to Reproduce Results

## Setup

Install required packages:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## Data

Download dataset from:
https://www.kaggle.com/datasets/uciml/mushroom-classification

Place `mushrooms.csv` in the project folder.

---

## Run Notebook

Open:

```bash
mushroom_classification.ipynb
```

Run all cells sequentially.

---

# Repository Structure

```
mushroom_classification.ipynb   # Main notebook with full pipeline
README.md                       # Project documentation
.gitignore                      # Excludes dataset
```

---

# Software Setup

* Python 3.x
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

# Performance Evaluation

* Run notebook cells
* View printed accuracy, ROC-AUC
* Review confusion matrix and ROC curve

---

# Citations

* UCI Mushroom Dataset
* Kaggle Dataset: https://www.kaggle.com/datasets/uciml/mushroom-classification
