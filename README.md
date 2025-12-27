# 🦉 BBO Owl Detection & Movement Analysis

### Behavioral Patterns, Predictive Modeling, and Explainable Machine Learning

## 📌 Project Summary

This project was completed in partnership with the **Beaverhill Bird Observatory (BBO)** to study and model the movement behavior of **Northern Saw-whet Owls** using telemetry data collected through the **Motus Wildlife Tracking System**.

The work presents a full **end-to-end data science workflow**, starting from raw wildlife telemetry data and progressing through exploratory analysis, feature engineering, machine learning, explainable AI, and deployment via an interactive **Streamlit** application. The goal is to transform complex tracking data into actionable and interpretable ecological insights.

---

## 🎯 Project Goals

* Examine owl movement behavior across time, direction, and signal characteristics
* Engineer behaviorally meaningful features from raw detection data
* Develop machine learning models to:

  * Classify migratory vs. non-migratory activity
  * Predict detection duration
  * Predict signal strength (SNR)
* Apply **Explainable AI (SHAP)** to interpret model predictions
* Deploy an interactive Streamlit dashboard for researchers and stakeholders

---

## 🗂️ Data Overview

**Data Source:** Motus Wildlife Tracking System (via BBO)
**Study Period:** July 2024 – November 2024

**Dataset Size**

* 102,678 detection records
* 57 total features (raw + engineered)

### Core Features

* **Telemetry metrics:** signal-to-noise ratio (SNR), noise, frequency drift
* **Temporal variables:** timestamp, hour, day, month
* **Antenna & direction data:** SE, SW, N, Omni
* **Tag deployment metadata**

### Engineered Variables

* `migration_activity`
* `direction_str`
* `days_since_deployment`
* Movement category labels

---

## 🔍 Exploratory Data Analysis

Key observations from exploratory analysis include:

* Detection activity peaks between **4–8 AM**, reflecting nocturnal owl behavior
* **September–October** shows the highest detection frequency, consistent with fall migration
* Predominant movement directions are **southeast and southwest**
* Migratory detections tend to have **higher SNR values**
* Signal strength declines gradually as tag age increases
* Distinct movement patterns emerge, including one-night passers, short stays, and multi-day migrants

All EDA findings are visualized within the Streamlit application.

---

## 🤖 Machine Learning Models

Three **Random Forest–based models** were trained and evaluated:

### **Model A – Migration Activity Classification**

* **Type:** Binary Classification
* **Objective:** Identify migratory vs. non-migratory detections
* **Technique:** SMOTE applied to handle class imbalance
* **Performance:**

  * Accuracy ≈ 96%
  * F1-score ≈ 0.97

### **Model B – Detection Duration Prediction**

* **Type:** Regression
* **Objective:** Predict duration of detection events
* **Performance:**

  * R² ≈ 0.99

### **Model C – Signal Strength (SNR) Prediction**

* **Type:** Regression
* **Objective:** Estimate signal strength based on movement and tag-age features
* **Performance:**

  * R² ≈ 0.85

---

## 🧠 Explainable AI (XAI)

Model interpretability was prioritized using **SHAP**:

* Both **global and local explanations** were generated
* Key influential features include:

  * Signal strength
  * Movement direction
  * Time of detection
  * Days since tag deployment

SHAP visualizations are embedded directly into the Streamlit dashboard for transparent interpretation.

---

## 🚀 Application Deployment

The project is deployed as a **multi-page Streamlit application**, allowing users to:

* Explore EDA results interactively
* Generate predictions using trained ML models
* Interpret outputs through SHAP plots
* Visualize owl movement behavior through dashboards

---

## 🛠️ Tools & Technologies

* Python, Pandas, NumPy
* Scikit-learn
* SHAP
* Plotly
* Streamlit
* GitHub
* Google Colab

---

## ⚠️ Challenges & Mitigation

* **Noisy telemetry signals:** Cleaned and standardized timestamps and signal values
* **Class imbalance:** Addressed using SMOTE
* **Large model artifacts:** Optimized model storage and deployment
* **Complex movement behavior:** Tree-based models chosen for robustness and interpretability

---

## 👥 Collaboration & Stakeholder Input

* Ongoing feedback from BBO researchers
* Emphasis on multi-day tag analysis (e.g., tags 80830, 80821, 80805)
* Modeling and visualization decisions aligned with ecological research priorities

---

## ✅ Final Remarks

This project demonstrates how **machine learning combined with explainable AI** can effectively support ecological research. By integrating predictive modeling, transparency, and interactive deployment, the solution provides BBO with a scalable and interpretable framework for understanding owl migration dynamics and telemetry behavior.

---

## 📎 Repository

🔗 GitHub Repository: 

---

