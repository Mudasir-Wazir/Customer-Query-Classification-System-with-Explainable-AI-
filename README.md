

## 🧠 Explainable AI for Political Bias Classifier

### 🔍 Project Overview
This project extends a political bias detection model with **Explainable AI (XAI)** techniques to improve interpretability and trust. While the core model (BERT + ANN) classifies news articles as Left, Center, or Right, this phase uses SHAP and LIME to explain model decisions, revealing **why** a particular bias label was predicted.

The goal is to make NLP-based media analysis not just accurate, but **transparent and auditable**, especially important for domains involving public trust like journalism, politics, and education.

---

### ⚙️ Key Features

- ✅ **SHAP (SHapley Additive exPlanations)**: 
  - Shows global and local feature impact on the model's predictions.
  - Visualizes how specific words influence a bias label (e.g., “freedom” driving right-leaning classification).

- ✅ **LIME (Local Interpretable Model-agnostic Explanations)**: 
  - Provides human-readable interpretations for individual predictions.
  - Reveals which token groups contribute to specific classification decisions.

- ✅ **Word Importance Heatmaps**: 
  - Interactive visualizations highlight emotionally or politically charged language.
  - Offers direct feedback for media editors and readers.

- ✅ **Comparative Explanation**: 
  - Demonstrates how the same article might be classified differently if a few keywords are altered.
  - Supports style transfer analysis by showing shifting model attention.

---

### 📊 Results Summary

- **Interpretability Insights**:
  - SHAP confirmed that words like *"immigration"*, *"tax cuts"*, and *"gun rights"* strongly influenced Right-leaning predictions.
  - LIME explanations aligned closely with SHAP, confirming robustness of model behavior.

- **Bias Surface Mapping**:
  - Global SHAP summary plots revealed that **Center** class predictions are influenced by neutral terms (e.g., *"report"*, *"update"*) while **Left** predictions skew toward social justice and equality-oriented terms.

- **Trust Calibration**:
  - Providing explanations increased user trust in model outputs by helping them understand *why* a classification was made—key for adoption in journalism and policy.


