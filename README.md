# 📊 Customer Service Query Classification with Explainable AI (XAI)

This project focuses on classifying customer service queries into multiple topics using NLP techniques and interpretable machine learning models. It explores traditional and modern text vectorization strategies alongside popular classifiers, with a focus on model performance and explainability through SHAP and LIME.

---

## 🧠 Project Overview

Customer service queries are often unstructured and diverse. This project aims to classify such queries into categories (like Shipping, Sales/Promotions, etc.) using:

- Text preprocessing & lemmatization
- Multiple text vectorization techniques
- Three different ML classifiers
- Explainability using SHAP and LIME
- Model evaluation through accuracy & classification reports

The entire pipeline is implemented in a modular, object-oriented format for scalability and reuse.

---

## 🔍 Methodology

1. **Data Preprocessing**:
   - Lowercasing, regex-based tokenization
   - Removal of short words (length ≤ 2)
   - Lemmatization using WordNet
   - Creation of a `clean_questions` column

2. **Text Vectorization Techniques**:
   - **TF-IDF**: Classic frequency-based weighting
   - **Word2Vec**: Average of word embeddings trained on the corpus
   - **Doc2Vec**: Paragraph vector representations
   - **TF-IDF (no stopwords)**: Alternate variant for comparison

3. **Train/Test Splitting**:
   - Stratified 80/20 train-test split
   - Label encoding for multiclass classification

4. **Model Explainability**:
   - **SHAP (SHapley Additive exPlanations)** was used to understand the global and local importance of features.
   - **LIME (Local Interpretable Model-agnostic Explanations)** was applied to analyze the behavior of individual predictions for black-box models like XGBoost and LightGBM.

---

## 🧪 Models Used

- **Decision Tree Classifier**
- **XGBoost Classifier**
- **LightGBM Classifier**

Each classifier was evaluated on all four vectorization techniques.

---

## 🚀 Key Features

- 🧼 Clean, modular code using Python classes (`CustomerQueryClassifier`)
- 📊 Class imbalance visualization
- 🧠 Trains Word2Vec and Doc2Vec embeddings using Gensim
- 📈 Evaluation with:
  - Accuracy Score
  - Classification Report (Precision, Recall, F1-score)
- 🧠 Explainability powered by:
  - **SHAP** for model-wide and instance-level insights
  - **LIME** for local interpretability of individual predictions

---

## 📊 Results Summary

| Vectorizer           | Model         | Accuracy (Approx.) |
|----------------------|---------------|---------------------|
| TF-IDF               | LightGBM      | High                |
| Word2Vec             | XGBoost       | Moderate            |
| Doc2Vec              | Decision Tree | Lower               |
| TF-IDF (no stopwords)| LightGBM      | Highest             |

- **Top Performer**: LightGBM + TF-IDF (with stopword removal)
- **Key Insight**: Simpler models benefit from richer contextual embeddings, but advanced boosting models outperform consistently.

---


