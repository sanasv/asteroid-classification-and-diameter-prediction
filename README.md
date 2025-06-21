# 🚀 Asteroid Hazard and Size Prediction

This project explores statistical and machine learning methods to classify potentially hazardous asteroids and predict their sizes using NASA's publicly available dataset. The goal is to assist early detection systems and risk assessment pipelines in planetary defense initiatives.

---

## 📌 Objectives

* **Classification**: Identify whether an asteroid is potentially hazardous.
* **Regression**: Predict the size (diameter) of an asteroid using orbital and physical parameters.
* **Feature Analysis**: Understand the influence of various features through statistical and visual analysis.

---

## 📂 Dataset

* Source: [NASA JPL Small-Body Database (via Kaggle)](https://www.kaggle.com/datasets/sameepvani/nasa-asteroids-classification)
* Contains physical and orbital data on \~90,000 asteroids.

## 🧪 Methods

### 🔍 Exploratory Analysis

* Correlation matrices, scatterplots, and boxplots
* Inferential statistics: chi-square tests, one-way and two-way ANOVA, point-biserial correlation

### 🤖 Classification Model

* **Logistic Regression** with pipeline (scaling + training)
* **Downsampling** to address class imbalance (only 0.22% labeled hazardous)

### 📈 Regression Model

* **Linear Regression** with:

  * Log-transformed target (Box-Cox)
  * PCA to reduce dimensionality
  * Evaluation using R² and residual plots

---

## ✅ Results

### Classification

| Metric               | Downsampled | Original |
| -------------------- | ----------- | -------- |
| Accuracy             | 100%        | 99%      |
| F1 Score (macro avg) | 100%        | 56%      |
| F1 Score (weighted)  | 100%        | 100%     |

> Note: False positives are considered acceptable given the risk of missing a real threat.

### Regression

* **Test R²:** 84.27%
* **Best features:** Inclination, perihelion distance, absolute magnitude

---

## 📊 Key Takeaways

* Statistical tests help filter and interpret impactful features.
* False positives are tolerable in hazardous asteroid detection due to the high cost of false negatives.
* PCA and transformation significantly improved regression performance.
* The model is lightweight and interpretable, suitable for early-warning systems.

---

## 🛠 Tech Stack

* Python (NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn)
* Jupyter Notebook

---

## 📌 Future Work

* Try ensemble methods (Random Forest, XGBoost) for regression
* Deploy model as an API for integration with space monitoring systems
* Explore real-time hazard prediction with orbital simulation data

---

## 🧠 Credits

This project was developed as part of a machine learning and data analysis course project, using public data from NASA’s JPL and Kaggle.
