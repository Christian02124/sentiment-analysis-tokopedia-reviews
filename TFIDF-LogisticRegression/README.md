# Sentiment Analysis on Indonesian Product Reviews

## 📌 Overview
This project builds a sentiment analysis model to classify Indonesian product reviews into **positive** or **negative** sentiments using traditional NLP and machine learning techniques.

The goal of this project is to demonstrate a complete **machine learning pipeline**, from data preprocessing to model training, evaluation, and inference readiness.

---

## 📊 Dataset
- Source: Indonesian product reviews (Tokopedia)
- Columns used:
  - `review_text`
  - `rating`
- Sentiment labeling:
  - Rating ≥ 4 → Positive
  - Rating ≤ 2 → Negative
  - Rating = 3 removed (neutral)

---

## 🧹 Data Preprocessing
- Removed missing values
- Removed neutral ratings
- Text cleaning:
  - Lowercasing
  - URL & symbol removal
  - Stopword removal (Bahasa Indonesia – Sastrawi)
- Class imbalance handled using **undersampling**

---

## ⚙️ Feature Engineering
- TF-IDF Vectorization
- Unigram & Bigram
- Max features: 5000

---

## 🤖 Model
- Algorithm: Logistic Regression
- Train-test split: 80:20 (stratified)
- Evaluation metrics:
  - Precision
  - Recall
  - F1-score
  - Confusion Matrix

---

## 📈 Results
- Balanced sentiment distribution after preprocessing
- Model performs consistently on both positive and negative classes
- Interpretable features showing top positive and negative keywords

---

## 🚀 Inference Example
```python
predict_sentiment("Barangnya bagus dan pengiriman cepat")
# Output: positive

predict_sentiment("barang jelek dan tidak sesuai")
# Output: negative
