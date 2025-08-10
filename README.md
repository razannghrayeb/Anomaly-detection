# 💳 Credit Card Fraud Detection System — Anomaly Detection Project

## 📌 Overview
This project is a **robust anomaly detection system** designed to identify fraudulent credit card transactions using **unsupervised machine learning** techniques. It supports both **real-time** and **batch processing**, empowering businesses to detect fraud efficiently and make informed decisions to safeguard financial transactions.

---

## 🌟 Why Anomaly Detection?

- Fraud detection is critical because fraudulent transactions are extremely rare and data is highly imbalanced.
- This system **automatically detects unusual transaction patterns** without relying on labeled fraud data.
- Provides **clear visual insights** for interpreting anomalies and making data-driven decisions.

---

## 📁 Dataset

| Feature | Description                                     |
|---------|------------------------------------------------|
| Source  | Kaggle - Credit Card Fraud Detection           |
| Records | 284,807 transactions                            |
| Features| - V1-V28: PCA-transformed anonymized features <br> - Time: Seconds elapsed between transactions <br> - Amount: Transaction amount <br> - Class: Binary label (0 = legitimate, 1 = fraud) |
| Imbalance | Only 492 fraud cases (0.17%) vs. 284,315 legitimate transactions |

---

## 🧠 Models Used

### 1. Isolation Forest
- **How it works:** Randomly isolates anomalies by partitioning data points.
- **Strengths:**  
  - Efficient in high-dimensional spaces  
  - Handles imbalanced data well  

### 2. One-Class SVM
- **How it works:** Learns a boundary around normal transactions; flags outliers.
- **Strengths:**  
  - Effective for novelty detection  
  - Robust to noise  

---

## 📊 Evaluation Metrics

| Model             | Precision | Recall | F1-Score | Accuracy |
|-------------------|-----------|--------|----------|----------|
| Isolation Forest  | 0.26     | 0.25  | 0.26    | 0.998    |
| One-Class SVM     | 0.13     | 0.52  | 0.2    | 0.993    |

**Key Insights:**

- Isolation Forest yields higher **precision** (fewer false positives).
- One-Class SVM achieves higher **recall** (detects more frauds but with more false alarms).
- The **precision-recall trade-off** should be balanced based on business priorities:  
  - Block as much fraud as possible (favor recall)  
  - Minimize false declines (favor precision)

---

## 🎯 Objectives

- ✅ Detect rare fraud cases without requiring labeled training data.
- ✅ Effectively handle extreme class imbalance (~0.17% fraud).
- ✅ Compare and benchmark Isolation Forest and One-Class SVM models.
- ✅ Provide intuitive visualizations such as confusion matrices and classification reports.

---

## 🛠️ Tech Stack

| Category     | Tools & Libraries                          |
|--------------|--------------------------------------------|
| Language     | Python                                     |
| Data Handling| Pandas, NumPy                              |
| Machine Learning | Scikit-learn                             |
| Visualization| Matplotlib, Seaborn                        |
| Environment  | Jupyter Notebook                           |

---

## Future Enhancements

- Integrate Deep Learning models like Autoencoders for superior anomaly detection.

- Develop a real-time REST API service to deploy the model in production.

- Explore advanced feature engineering by incorporating time-series and sequential transaction patterns.

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook

### Installation

```bash
git clone https://github.com/razannghrayeb/anomaly-detection.git
cd anomaly-detection
pip install -r requirements.txt
