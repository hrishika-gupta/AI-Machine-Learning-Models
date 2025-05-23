# 🤰 Maternal Health Risk Analysis with Deep Learning

A deep learning-based risk prediction system built to identify high-risk pregnancies using real-time physiological data. The model supports rural healthcare workers and policymakers in Bangladesh to intervene early and reduce maternal mortality.

---

## 🎯 Problem Statement

Maternal mortality rates remain high in rural Bangladesh due to poor access to healthcare and late detection of risk. This project aims to develop a deep learning solution for **real-time maternal health monitoring** using key health indicators.

---

## 🚀 Objectives

- Predict maternal risk level (Low, Medium, High) using six physiological parameters.
- Compare and optimize deep learning models using **Random Search**, **Hyperband**, and **Bayesian Optimization**.
- Provide interpretable health insights for **doctors**, **policymakers**, and **researchers**.

---

## 📊 Dataset Overview

- 📦 1,014 instances | 🧬 6 input features
- No missing values
- Features: Age, Systolic BP, Diastolic BP, Blood Sugar, Temperature, Heart Rate
- Target: Risk Level (`Low`, `Medium`, `High`) – one-hot encoded

---

## 🧪 Model Training & Optimization

We trained a deep neural network using different hyperparameter tuning methods:

### 🔹 Random Search
- Best Config: `Batch size = 16`, `Epochs = 300`, `Units = 16`
- Accuracy: **Train = 62.7%**, **Validation = 56%**
- Observed overfitting after 200 epochs

### 🔹 Bayesian Optimization
- Best Config: `Units = 164`, `Activation = ReLU`, `Epochs = 200`
- Accuracy: **Train = 72%**, **Validation = 65%**

### 🔹 Hyperband Optimization
- Best Config: `Units = 180`, `Activation = ReLU`
- Accuracy: **Train = 71%**, **Validation = 66%**
- Fastest runtime (~56 seconds)

---

## 🧾 Final Model Performance

| Class       | Precision | Recall | F1-Score | Support |
|-------------|-----------|--------|----------|---------|
| Low Risk    | 0.69      | 0.84   | 0.76     | 128     |
| Medium Risk | 0.60      | 0.44   | 0.51     | 100     |
| High Risk   | 0.82      | 0.82   | 0.82     | 77      |

- **Overall Accuracy:** 70.2%
- Confusion matrix insights reveal strong performance for `Low` and `High` risk classes.

---

## 📈 Visual Insights

- 🔺 Blood sugar & blood pressure were highest in high-risk individuals.
- 🌡 High-risk women tend to show temperatures between **101–103°F**.
- ❤️ Heart rate above 78 bpm correlates with increased risk.
- 👩‍🦳 Older women are more likely to fall under the `High Risk` category.

---

## 🧠 Recommendations

- **Glucose & BP Monitoring:** Regular checks + early intervention
- **Healthcare Access:** Monthly checkup camps in underserved rural areas
- **Education Campaigns:** Build awareness on identifying early risk signs

---

## 🛠 Tech Stack

- Python · Pandas · NumPy · Matplotlib · Seaborn  
- TensorFlow · Keras · SciKeras · RandomizedSearchCV  
- Google Colab · Hyperparameter Optimization Libraries

---

## 📂 Project Structure

```
maternal-health-risk-analysis/
├── random_search_model.ipynb
├── bayesian_optimization_model.ipynb
├── hyperband_optimization_model.ipynb
├── maternal_health_final_notebook.ipynb
└── README.md
```

---

## 📬 Contact

📧 Hrishikagupta15@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/hrishikashalvigupta)

---

⭐ *If you found this useful, consider giving this repo a star!*
