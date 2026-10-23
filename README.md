# 🎬 Box Office Success Predictor (Pre-Release Analytics)

An end-to-end Machine Learning pipeline developed to evaluate and forecast the commercial success of motion pictures prior to their theatrical release, leveraging metadata from the TMDB 5000 dataset.

---

## 📌 Project Overview
Predicting financial outcomes in the entertainment industry is critical for minimizing risk. This project constructs a predictive classification framework that analyzes pre-release indicators—such as production budgets, genre combinations, runtime, and cast/crew size—to estimate movie success without relying on post-release data (such as user reviews or post-launch revenue).

---

## 🎯 Target Formulation
A movie is categorized as **Successful (Class 1)** based on a standard industry heuristic:
$$\text{Revenue} \ge 1.5 \times \text{Budget}$$

> **Note:** Financial metrics like revenue are strictly reserved for constructing the target labels during training and are fully excluded from the model feature input set to prevent data leakage.

---

## 🛠️ Data Pipeline & Methodology
1. **Data Acquisition:** Sourced structured movie metadata from the TMDB Kaggle dataset.
2. **Feature Engineering & Cleaning:**
   - Parsing structured JSON/Text columns (genres, keywords, cast, production companies).
   - Handling missing indicators and filtering valid budget entries.
   - Feature normalization and scaling for distance-based estimators.
3. **Model Architecture:** Implemented and benchmarked four distinct supervised classification algorithms:
   - **Logistic Regression**
   - **K-Nearest Neighbors (KNN)**
   - **Decision Tree Classifier**
   - **Gaussian Naive Bayes (GaussianNB)**

---

## 💻 Tech Stack
- **Language:** Python
- **Environment:** Jupyter Notebook
- **Core Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

---

## 🚀 Getting Started

### Prerequisites
Clone the repository and install the required dependencies:
```bash
git clone https://github.com/Bushra-Alhusyani/Pre-Release-Movie-Success-Prediction.git
cd Pre-Release-Movie-Success-Prediction
pip install pandas numpy scikit-learn matplotlib seaborn
