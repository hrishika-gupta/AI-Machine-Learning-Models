# 🤰 Maternal Health Risk Analysis with Deep Learning

Maternal mortality continues to pose a critical challenge in rural regions, especially in countries like Bangladesh, where access to quality healthcare is often delayed or inadequate. Early detection of pregnancy-related complications is essential for saving lives. Leveraging the power of AI and deep learning, this project presents a robust solution for **real-time risk classification** based on vital health indicators. Our system is designed to aid rural healthcare workers and policymakers by offering timely predictions and evidence-backed insights using deep learning models.

---

## 🎯 Problem Statement

Maternal mortality rates remain high in rural Bangladesh due to poor access to healthcare and late detection of risks. This project aims to develop a deep learning–based decision support system for **real-time maternal health monitoring** using physiological indicators to proactively identify and mitigate risks.

---

## 🧭 Project Objectives

- 📊 Predict maternal risk levels (Low, Medium, High) based on six physiological parameters.
- 🧪 Train & compare deep learning models with **Random Search**, **Hyperband**, and **Bayesian Optimization** techniques.
- 🩺 Provide explainable and interpretable predictions for doctors, researchers, and health policymakers.

---

## 📚 Dataset Overview

| Attribute | Value |
|----------|-------|
| 📌 Dataset | Maternal Health Risk Dataset (Bangladesh-based IoT Monitoring) |
| 📊 Instances | 1,013 |
| 🧬 Features | 6 (Age, SystolicBP, DiastolicBP, Blood Sugar, Temperature, Heart Rate) |
| 🏷️ Target | Risk Level — Low, Medium, High (One-hot encoded) |
| ❌ Missing Values | No |

All features are real/integer types and reflect critical maternal health signals used for real-time monitoring.

---

## 🧠 Model Training & Optimization

We trained a deep neural network on the dataset using different hyperparameter tuning strategies to maximize classification performance while minimizing overfitting.

### 🔍 Random Search

- **Best Config:** `Batch size = 16`, `Epochs = 300`, `Units = 16`
- **Accuracy:** `Train = 62.7%`, `Validation = 56%`
- **Note:** Observed overfitting post 200 epochs

### 🧪 Bayesian Optimization

- **Best Config:** `Units = 164`, `Activation = ReLU`, `Epochs = 200`
- **Accuracy:** `Train = 72%`, `Validation = 65%`

### ⚡ Hyperband Optimization

- **Best Config:** `Units = 180`, `Activation = ReLU`
- **Accuracy:** `Train = 71%`, `Validation = 66%`
- **Note:** Fastest convergence (~56 seconds)

---

## 📈 Final Model Performance

| Risk Class     | Precision | Recall | F1-Score | Support |
|----------------|-----------|--------|----------|---------|
| Low Risk       | 0.69      | 0.84   | 0.76     | 128     |
| Medium Risk    | 0.60      | 0.44   | 0.51     | 100     |
| High Risk      | 0.82      | 0.82   | 0.82     | 77      |

- **Overall Accuracy:** `70.2%`
- 🔍 **Insight:** Model performs best for High and Low risk classifications.

---

## 🧾 Key Insights

- 🔺 Blood sugar and BP were highest in high-risk patients.
- 🌡️ High-risk women typically show temperatures in the 101–103°F range.
- 💓 Heart rate >78 bpm strongly correlates with risk.
- 👵 Women of older age groups trend toward higher risk categories.

---

## 💡 Recommendations

- **Glucose & BP Monitoring:** Regular checkups + early intervention
- **Healthcare Access:** Increase rural outreach & health camps
- **Awareness Drives:** Educate women on early warning signs

---

## 🛠️ Tech Stack

- **Languages & Libraries:** Python, NumPy, Pandas, Matplotlib, Seaborn  
- **Frameworks:** TensorFlow, Keras, SciKeras  
- **Optimization:** RandomizedSearchCV, Hyperband, Bayesian Optimization  
- **Notebook Environment:** Google Colab

---

## 📁 Project Structure
```
maternal-health-risk-analysis/
├── random_search_model.ipynb
├── bayesian_optimization_model.ipynb
├── hyperband_optimization_model.ipynb
├── maternal_health_final_notebook.ipynb
└── README.md
```
---

## 📨 Contact

📧 Hrishikagupta15@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/hrishikagupta15)

---

> ⭐ **If you found this useful, consider starring the repo!**

