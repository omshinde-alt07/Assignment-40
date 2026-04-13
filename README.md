# Assignment-41

# ShopSense Sentiment Analysis

Github link : https://github.com/omshinde-alt07/Assignment-41

## File Name

`main.ipynb`

## Project Overview

This project performs sentiment analysis on the ShopSense customer review dataset. The goal is to classify customer reviews into **Positive**, **Negative**, and **Neutral** sentiments using Natural Language Processing (NLP) and Machine Learning techniques.

The notebook includes data exploration, preprocessing, model training, evaluation, deployment-focused analysis, cost modeling, and production recommendations.

---

## Objectives

* Analyze sentiment label distribution
* Show why accuracy alone can be misleading
* Train and evaluate sentiment classifiers
* Compare multiple approaches under production constraints
* Detect and fix a broken pipeline
* Estimate business cost of model errors
* Recommend a production-ready solution
* Define monitoring and retraining strategy

---

## Dataset Features

The dataset contains review-related fields such as:

* `review_text`
* `sentiment_label`
* `rating`
* `category`
* `language`
* `verified_purchase`
* `helpful_votes`
* `review_date`
* `device_type`
* `return_flag`

Main columns used in this project:

* **Input Text:** `review_text`
* **Target Label:** `sentiment_label`

---

## Techniques Used

### Data Preprocessing

* Null value removal
* Text cleaning
* Train-test split
* Stratified sampling

### Feature Engineering

* TF-IDF Vectorization
* N-grams

### Models

* Logistic Regression
* Comparative evaluation pipelines

### Evaluation Metrics

* Accuracy
* Precision
* Recall
* Weighted F1 Score
* Macro F1 Score
* Confusion Matrix
* Classification Report

---

## Key Insights

### 1. Class Imbalance

The dataset contains more positive reviews than negative or neutral reviews. Because of this, accuracy alone is not a reliable metric.

### 2. Better Evaluation Metrics

Weighted F1 Score was used because it evaluates all sentiment classes fairly.

### 3. Production Constraints Considered

* New categories with no retraining
* Hindi-English mixed reviews
* Inference under 20 ms

### 4. Business Cost Analysis

Different costs were assigned to:

* False Negatives (missed complaints)
* False Positives (unnecessary escalation)

This helped choose the best production model.

### 5. Monitoring Plan

Weekly tracking of:

* Weighted F1
* False Negative Rate
* Data Drift
* Confidence Shift

---

## How to Run

### Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Open Notebook

```bash
jupyter notebook main.ipynb
```

Run all cells in sequence.

---

## Output

The notebook generates:

* Sentiment distribution charts
* Model performance metrics
* Confusion matrices
* Before vs after pipeline comparison
* Cost estimation summary
* Final production recommendation

---

## Recommended Deployment Model

Balanced classifier evaluated using Weighted F1 Score and monitored weekly for drift and complaint recall.

---

## Author

Om Shinde
