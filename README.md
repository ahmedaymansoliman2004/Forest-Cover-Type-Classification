<img width="759" height="245" alt="Elevvo Logo" src="https://github.com/user-attachments/assets/ac3c53a8-9a6c-4db6-b7eb-34b1518d273f" />  # 🌲 Forest Cover Type Classification  <img width="1150" height="488" alt="logo" src="https://github.com/user-attachments/assets/bcea206f-2ac1-4e01-b492-7957e061596a" />

A machine learning project for multi-class classification using the UCI Covertype dataset.

---

## 📌 Project Overview

This project aims to predict the dominant forest cover type of a specific geographical area using cartographic and environmental features.

The dataset contains **581,012 observations** and **54 predictive features**, including:

- Elevation
- Terrain slope and aspect
- Horizontal & vertical distances to hydrology
- Distances to roads and fire points
- Hillshade measurements
- Wilderness areas (one-hot encoded)
- Soil types (one-hot encoded)

The target variable consists of **7 forest cover types**.

---

## 🎯 Objectives

- Perform Exploratory Data Analysis (EDA)
- Handle class imbalance properly
- Train and compare tree-based models
- Evaluate performance using robust multi-class metrics
- Analyze feature importance

---

## 📊 Dataset

Source: UCI Machine Learning Repository  
Dataset: Covertype

Due to GitHub file size limitations, the dataset may not be included directly in this repository.

To run this project:

1. Download `covtype.csv`
2. Place it inside:


---

## ⚙️ Methodology

### 1️⃣ Data Exploration
- Verified dataset integrity (no missing values)
- Analyzed class distribution
- Explored numerical feature distributions
- Evaluated correlations

### 2️⃣ Handling Class Imbalance
Instead of oversampling or SMOTE (which may distort one-hot encoded features), class weighting was applied to ensure fair influence of minority classes.

### 3️⃣ Models Trained

- ✅ Random Forest (with class weighting)
- ✅ XGBoost (with sample weighting)

### 4️⃣ Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-score (Macro & Weighted)
- Confusion Matrix

---

## 📈 Results

| Model            | Accuracy | Macro F1 | Weighted F1 |
|------------------|----------|----------|-------------|
| Random Forest    | **95.5%** | **0.93** | 0.95 |
| XGBoost          | 86.1% | 0.83 | 0.86 |

### 🔎 Key Insights

- Random Forest significantly outperformed XGBoost.
- Elevation was the most important predictive feature.
- Tree-based models effectively captured nonlinear interactions.
- Class weighting successfully mitigated imbalance effects.

---

## 🧠 Feature Importance

Top predictive features:

1. Elevation
2. Horizontal Distance to Roadways
3. Horizontal Distance to Fire Points
4. Hydrology-related distances

These findings align with real-world geographic and ecological patterns.

---

## 🏆 Conclusion

Random Forest proved to be the most effective model for this large-scale structured dataset, achieving high accuracy and strong macro-level performance across minority classes.

Tree-based ensemble methods are highly suitable for complex environmental classification problems involving nonlinear relationships.

---

## 🚀 Recommendations

- Deploy Random Forest as the primary production model
- Apply hyperparameter tuning for further optimization
- Use cross-validation for additional robustness
- Integrate SHAP analysis for deeper interpretability
- Explore ensemble stacking for marginal gains

---

## 🛠 Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib
- Seaborn

---

## 👨‍💻 Author

Ahmed Ayman Soliman  
Machine Learning & Data Science Enthusiast

---

## 🔗 Connect

If you found this project interesting, feel free to connect or explore more of my work.
