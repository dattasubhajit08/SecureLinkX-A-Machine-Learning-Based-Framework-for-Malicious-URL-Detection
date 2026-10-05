# 🔐 SecureLinkX: A Machine Learning-Based Framework for Malicious URL Detection

**SecureLinkX** is a machine learning-based framework designed to detect and classify URLs as **Benign** or **Malicious**. The project analyzes URL-based features and compares multiple machine learning algorithms to identify an effective model for malicious URL detection.

The main objective of this project is to provide an efficient and reliable approach for detecting suspicious URLs that may be associated with **phishing, malware distribution, and other cyber threats**.

---

## 📌 Project Overview

Malicious URLs are commonly used in phishing attacks, malware distribution, identity theft, and other cybercrimes. Traditional blacklist-based methods may struggle to identify newly created or previously unseen malicious URLs.

**SecureLinkX** uses machine learning techniques to identify patterns in URL features and classify URLs into two categories:

* 🟢 **Benign (0)** – Safe or legitimate URL
* 🔴 **Malicious (1)** – Suspicious or harmful URL

The project evaluates multiple machine learning models and compares their performance using standard classification metrics.

---

## 🎯 Objectives

* Detect malicious URLs using machine learning.
* Extract and analyze URL-based features.
* Compare different machine learning algorithms.
* Evaluate models using accuracy, precision, recall, F1-score, and confusion matrix.
* Identify the best-performing model for malicious URL classification.
* Build a foundation for an intelligent URL security system.

---

## 📊 Dataset

The project uses the **PhiUSIIL Phishing URL Dataset**.

### Dataset Information

| Property         | Details                       |
| ---------------- | ----------------------------- |
| Dataset          | PhiUSIIL Phishing URL Dataset |
| Working Dataset  | **5,000 URLs**                |
| Classification   | Binary Classification         |
| Benign Label     | `0`                           |
| Malicious Label  | `1`                           |
| Train-Test Split | 70:30                         |
| Random State     | 42                            |
| Features         | 54                            |
| Environment      | Google Colab                  |

For computational efficiency, a balanced subset of **5,000 URLs** was selected for the main experiments.

---

## 🧠 Machine Learning Models

The following six machine learning algorithms were implemented and compared:

1. 🌳 Decision Tree
2. 🌲 Random Forest
3. 📈 Logistic Regression
4. 🎲 Naive Bayes
5. 📍 K-Nearest Neighbors (KNN)
6. ⚙️ Support Vector Machine (SVM)

---

## 🔬 Methodology

The overall workflow of SecureLinkX is:

```text
                 ┌──────────────────────┐
                 │       Dataset        │
                 │   5,000 URLs         │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │ Data Preprocessing   │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │ Feature Extraction   │
                 │ & Feature Selection  │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │ 70% Training Data    │
                 │ 30% Testing Data     │
                 └──────────┬───────────┘
                            │
                            ▼
              ┌─────────────────────────────┐
              │   Machine Learning Models  │
              ├─────────────────────────────┤
              │ Decision Tree               │
              │ Random Forest               │
              │ Logistic Regression         │
              │ Naive Bayes                 │
              │ KNN                         │
              │ SVM                         │
              └──────────────┬──────────────┘
                             │
                             ▼
                 ┌──────────────────────┐
                 │ Model Evaluation     │
                 │ Accuracy             │
                 │ Precision            │
                 │ Recall               │
                 │ F1-Score             │
                 │ Confusion Matrix     │
                 └──────────────────────┘
```

---

## 🔍 Features

SecureLinkX uses URL-based features to identify suspicious patterns.

Examples include:

* URL length
* Number of special characters
* Presence of an IP address
* Domain-related information
* Character and symbol patterns
* Host-based characteristics
* Other lexical URL features

These features help machine learning models distinguish between legitimate and malicious URLs.

---

## 📈 Results

The experimental results show that **Random Forest achieved the best overall performance**, with approximately **99% accuracy** on the selected dataset.

### Model Comparison

| Model                  | Performance                |
| ---------------------- | -------------------------- |
| 🌲 Random Forest       | ⭐ Best overall performance |
| ⚙️ SVM                 | Excellent performance      |
| 🌳 Decision Tree       | Excellent performance      |
| 📈 Logistic Regression | High recall                |
| 🎲 Naive Bayes         | High recall                |
| 📍 KNN                 | Good performance           |

### Key Findings

* **Random Forest** provided the best overall classification performance.
* **SVM** and **Decision Tree** also showed strong and balanced results.
* **Logistic Regression** and **Naive Bayes** achieved very high recall.
* **KNN** achieved good performance but was comparatively lower than the other models.
* The experiments demonstrate that machine learning can effectively identify malicious URL patterns.

---

## 🛠️ Technologies Used

### Programming Language

* 🐍 Python

### Machine Learning

* Scikit-learn

### Data Processing

* Pandas
* NumPy

### Data Visualization

* Matplotlib

### Development Environment

* Google Colab
* Jupyter Notebook

---

## 📂 Repository Structure

```text
SecureLinkX-A-Machine-Learning-Based-Framework-for-Malicious-URL-Detection/
│
├── 📁 dataset/
│   └── 5000 URL dataset
│
├── 📄 PhiUSIIL_Phishing_URL_Dataset.csv.gz
│
├── 📓 project_urlclassification25_5.ipynb
│
└── 📄 README.md
```

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/dattasubhajit08/SecureLinkX-A-Machine-Learning-Based-Framework-for-Malicious-URL-Detection.git
```

### 2. Open the Project

```bash
cd SecureLinkX-A-Machine-Learning-Based-Framework-for-Malicious-URL-Detection
```

### 3. Open the Notebook

Open:

```text
project_urlclassification25_5.ipynb
```

You can run the notebook using **Google Colab** or **Jupyter Notebook**.

### 4. Install Required Libraries

```bash
pip install pandas numpy scikit-learn matplotlib
```

### 5. Run the Notebook

Execute the notebook cells sequentially to:

```text
Load Dataset
     ↓
Preprocess Data
     ↓
Select Features
     ↓
Split Dataset
     ↓
Train Models
     ↓
Evaluate Models
     ↓
Compare Results
```

---

## 📊 Evaluation Metrics

The models are evaluated using:

### Accuracy

Measures the percentage of correctly classified URLs.

```text
Accuracy = Correct Predictions / Total Predictions
```

### Precision

Measures how many URLs predicted as malicious are actually malicious.

### Recall

Measures how many actual malicious URLs are correctly detected.

### F1-Score

Provides a balance between precision and recall.

### Confusion Matrix

Shows:

```text
                 Predicted
              Benign  Malicious

Actual
Benign       →  TN       FP

Malicious    →  FN       TP
```

---

## 💡 Key Contribution

The main contribution of **SecureLinkX** is the comparative analysis of multiple machine learning algorithms for malicious URL detection using URL-based features.

The project demonstrates that a machine learning approach can provide highly accurate classification while allowing different models to be evaluated under the same experimental setup.

---

## 🔮 Future Improvements

Future versions of SecureLinkX can include:

* Real-time URL detection
* Web-based user interface
* Browser extension integration
* Real-time threat intelligence
* Deep learning models
* Explainable AI techniques
* Larger and more diverse datasets
* Continuous model retraining
* API-based URL prediction

---

## 👨‍💻 Author

### Subhajit Datta

**MCA Student | BCA Graduate | Machine Learning Enthusiast**

GitHub:
https://github.com/dattasubhajit08

---

## ⭐ Acknowledgement

This project was developed as an academic machine learning project focused on cybersecurity and malicious URL detection.

The project uses the **PhiUSIIL Phishing URL Dataset** for experimentation.

---

## 📜 License

This project is intended primarily for **educational and academic purposes**.

---

## 🔗 Repository

**SecureLinkX – A Machine Learning-Based Framework for Malicious URL Detection**

https://github.com/dattasubhajit08/SecureLinkX-A-Machine-Learning-Based-Framework-for-Malicious-URL-Detection
