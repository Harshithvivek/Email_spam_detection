# Email Spam Detection using Logistic Regression

A clean, production-ready machine learning pipeline for binary text classification, designed to detect whether an email is **Spam** or **Ham (Not Spam)**. This repository contains an optimized baseline model using Logistic Regression evaluated with complete multi-class classification metrics.

## 📊 Dataset Overview
The dataset (`emails.csv`) consists of **5,172 unique emails** preprocessed into a numerical feature matrix. 
* **Features:** 3,000 columns representing individual word frequencies (Bag-of-Words/Token Count representation).
* **Identifier:** `Email No.` (Dropped during preprocessing).
* **Target:** `Prediction` (`0` for Ham / Safe, `1` for Spam).

---

## 🛠️ Tech Stack & Dependencies
* **Language:** Python 3.x
* **Environment:** Google Colab / Jupyter Notebook
* **Libraries:** * `pandas` & `numpy` (Data Manipulation)
  * `scikit-learn` (Machine Learning Engine)

---

## 🚀 Model Architecture & Pipeline
1. **Data Ingestion:** Loading pre-vectorized email datasets.
2. **Preprocessing:** Isolating target labels and removing unique string identifiers.
3. **Data Splitting:** 80/20 train-test stratification to ensure unbiased validation.
4. **Model Training:** Fitting a standard Logistic Regression model optimized with `max_iter=1000` to prevent gradient convergence issues over high-dimensional feature spaces.
5. **Evaluation:** Generating exact accuracy, precision, recall, and a visual confusion matrix layout.

---

## 📈 Evaluation Results

The model achieves exceptional performance on unseen test data due to the strong predictive signals of specific high-frequency keywords:

* **Overall Accuracy:** `~97.20%`
* **Precision (Spam):** `~0.94` (Minimizes False Positives, ensuring valid emails aren't accidentally filtered to spam)
* **Recall (Spam):** `~0.96` (Ensures the vast majority of actual malicious spam emails are successfully captured)

### Confusion Matrix Breakdown
* **True Negatives (Correctly identified safe emails):** 722
* **True Positives (Correctly caught spam):** 284
* **False Positives (Safe emails sent to spam):** 17
* **False Negatives (Spam emails missed):** 12

---

## 💻 How to Run
1. Clone this repository:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git)
