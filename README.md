# 🚢 Intermodal Congestion Predictor

## 📌 Project Overview

Logistics disruptions at ports and rail terminals cause cascading delays, increased costs, and poor service reliability. This project builds a **predictive analytics system** that estimates the **probability of shipment delay before it happens**, using operational, congestion, and external risk signals.

The solution combines **machine learning** with an **interactive Streamlit dashboard**, simulating a real-world logistics **control tower** used by rail operators, port authorities, and supply chain planners.

---

## 🎯 Business Problem

> *How can logistics operators proactively identify shipments at high risk of delay due to congestion, weather, and operational constraints?*

Traditional reporting only explains **what already went wrong**. This project shifts the focus to **predictive management**, enabling teams to:

* Re-route shipments early
* Allocate resources proactively
* Reduce knock-on supply chain disruptions

---

## 🧠 Solution Summary

* Define a **delay risk classification problem**
* Engineer time-based and operational features
* Train a machine learning model to predict delay probability
* Deploy results in an interactive Streamlit dashboard for scenario analysis

---

## 🗂️ Dataset

**Source:** Dynamic Supply Chain Logistics Dataset (CSV)

**Key Feature Groups:**

* **Congestion Signals:** traffic congestion, port congestion
* **Operational Factors:** loading/unloading time, customs clearance time, equipment availability
* **Risk & Reliability:** route risk, supplier reliability, driver behavior, fatigue monitoring
* **Temporal Factors:** day of week, month, hour of day

### Target Variable

A shipment is labeled as **delayed** if:

> `ETA variation > 2 hours`

This threshold reflects realistic operational tolerance in intermodal logistics.

---

## ⚙️ Tech Stack

* **Python**
* **pandas / numpy** – data preparation
* **scikit-learn** – modeling
* **XGBoost / Random Forest** – advanced models (optional)
* **Streamlit** – interactive dashboard

---

## 📈 Modeling Approach

1. Feature engineering from raw logistics data
2. Train/Test split with class stratification
3. Baseline model: **Logistic Regression** (explainable)
4. Advanced model: **Tree-based classifier** for non-linear effects
5. Evaluation using:

   * ROC-AUC
   * Precision / Recall

> False negatives are especially costly, as unflagged delays propagate downstream disruptions.

---

## code
https://github.com/nte-samuel/Intermodal-Delay-Risk-Predictor/blob/main/Untitled44.ipynb

---

## 📁 Project Structure

```
Intermodal-Congestion-Predictor/
│
├── data/
│   └── dynamic_supply_chain_logistics_dataset.csv
│
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_feature_engineering.ipynb
│   └── 03_modeling.ipynb
│
├── app.py
├── requirements.txt
└── README.md
```

---

## 💡 Key Insights (Example)

* Port congestion and customs clearance time are the strongest predictors of delay risk
* Delay probability increases significantly during peak weekday hours
* Reliability scores meaningfully reduce delay likelihood

---

## 🔮 Future Enhancements

* SHAP-based explainability
* Real-time weather and port congestion APIs
* Cost impact estimation per delayed shipment
* Integration with routing optimization systems

---

## 👤 Author

**Samuel**
Data Analyst | Logistics & Supply Chain Analytics

---

## ⭐ Why This Project Matters

This project demonstrates the ability to:

* Translate logistics pain points into predictive models
* Work with real operational data
* Deliver decision-ready analytics, not just charts

It directly aligns with **rail, port, mining, and logistics operators** transitioning toward predictive and proactive supply chain management.
