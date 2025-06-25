

````markdown
# 🌍 Earthquake Magnitude Classification with XGBoost 📊

This project aims to classify earthquake magnitudes into categories — Minor, Moderate, and Strong — using time-based feature engineering, preprocessing pipelines, class balancing (SMOTE), and a regularized XGBoost model. Evaluation is conducted using confusion matrix, ROC-AUC curves, and classification reports.

---

## 📚 Table of Contents

- [Introduction 🎯](#introduction-🎯)
- [Installation 🛠️](#installation-🛠️)
- [Usage 🚀](#usage-🚀)
- [Methodology 🧠](#methodology-🧠)
  - [Data Preprocessing 🧼](#data-preprocessing-🧼)
  - [Feature Engineering 🏗️](#feature-engineering-🏗️)
  - [Balancing Classes ⚖️](#balancing-classes-⚖️)
  - [Model Training 🧪](#model-training-🧪)
  - [Evaluation 📉](#evaluation-📉)
- [Results 📈](#results-📈)
- [Contributing 🤝](#contributing-🤝)
- [License 📄](#license-📄)

---

## Introduction 🎯

This project classifies earthquake events based on their magnitude. Using real-world data, we categorize magnitudes into:

- **Minor** (< 4.0)
- **Moderate** (4.0–6.0)
- **Strong** (≥ 6.0)

The goal is to train a robust classifier that can predict these categories using engineered features and imbalanced-learning techniques.

---

## Installation 🛠️

Install all dependencies via pip:

```bash
pip install pandas numpy scikit-learn xgboost imbalanced-learn matplotlib seaborn
````

---

## Usage 🚀

1. Place your dataset CSV file (e.g. `query.csv`) in the project directory.
2. Update the path inside the script if needed.
3. Run the main Python script:

```bash
python earthquake_classification.py
```

---

## Methodology 🧠

### Data Preprocessing 🧼

* Load and clean the dataset.
* Handle missing values using `SimpleImputer`.
* Label encode categorical variables.
* Drop unnecessary columns like `id`, `place`, and `updated`.

### Feature Engineering 🏗️

* Extract time features: `year`, `month`, `day`, and `hour` from the `time` field.
* Drop original timestamp and non-predictive columns.

### Balancing Classes ⚖️

* Use **SMOTE** to oversample underrepresented magnitude categories.
* Normalize features using `StandardScaler`.

### Model Training 🧪

* Train a **multi-class XGBoost** model with early stopping and regularization:

  * `reg_alpha`, `reg_lambda`, `max_depth`, `colsample_bytree`, etc.
* Use `DMatrix` objects for optimized performance.

### Evaluation 📉

* Generate:

  * Confusion matrix
  * ROC-AUC curves per class
  * Classification reports on both train and test data

---

## Results 📈

* Achieved strong classification accuracy across the three magnitude categories.
* **ROC-AUC Curves** show good class separation.
* Confusion matrix and precision/recall metrics help identify misclassifications.

<!-- Optional image references if added to the repo -->

<!-- ![ROC Curve Sample](assets/roc_curve.png) -->

<!-- ![Confusion Matrix Sample](assets/confusion_matrix.png) -->

---

## Contributing 🤝

Contributions, bug reports, and feature requests are welcome!
Open a pull request or issue to get started.

---

## License 📄

This project is open-sourced under the [MIT License](LICENSE).

````

---

### ✅ To add this to GitHub:
1. Save the above content as `README.md` in your root project directory.
2. Commit and push:
   ```bash
   git add README.md
   git commit -m "Add project README"
   git push origin main
````


