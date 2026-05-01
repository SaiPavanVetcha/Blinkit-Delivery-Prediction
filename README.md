# 🚚 Blinkit Delivery Delay Prediction (Machine Learning)

An end-to-end machine learning pipeline for predicting delivery delays in quick-commerce systems like Blinkit. This repository focuses on the ML modeling, analysis, and prediction layer, while the data warehouse and ETL pipeline are maintained in a separate repository.

---

## 📌 Project Overview

Quick-commerce platforms rely on ultra-fast logistics, but delivery delays remain a major challenge due to factors like distance, demand fluctuations, and resource constraints.

This project builds a machine learning system to:

- 📊 Analyze delivery patterns  
- ⏱️ Predict delivery delays  
- ⚙️ Support logistics optimization decisions  

---

## 🏗️ Architecture

This repository represents the ML layer of a larger system:
```
blinkit-data-warehouse
└── ETL Pipeline (Bronze → Silver → Gold)
└── PostgreSQL Data Warehouse
↓
Blinkit-Delivery-Prediction
└── Model Training
└── Evaluation & Prediction
```

🔗 **Data Warehouse Repository:** *https://github.com/SaiPavanVetcha/blinkit-data-warehouse*

---

## 🧠 Machine Learning Pipeline

### 1. Data Input
- Processed datasets from the **Gold layer** of the warehouse  
- Structured using a **star schema** (fact + dimension tables)

### 2. Feature Engineering
- Distance-based features  
- Order-level attributes  
- Aggregated delivery metrics  

### 3. Models Implemented

- Logistic Regression (baseline)  
- Random Forest (best performer)  
- XGBoost (gradient boosting)  

---

## 📈 Model Performance

| Model               | Accuracy|
|---------------------|---------|
| Logistic Regression | 58%     |
| Random Forest       | **63%** |
| XGBoost             | 61%     |

- 🎯 **Best Model:** Random Forest  
- 📊 **AUC Score:** 0.679  

---

## 🔍 Key Insights

- 📏 Delivery time increases with distance  
- 🧾 Order features significantly impact delay probability  
- ⚠️ False negatives (missed delays) are critical in real-world logistics  

---

## 🛠️ Tech Stack

- Python  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib / Seaborn  

---

## 📂 Repository Structure
```
├── datasets/ # Processed datasets (optional / sample)
├── notebooks/ # EDA and experimentation
├── models/ # Saved models
├── requirements.txt
└── README.md
```

---

## 🚀 How to Run

```bash
# Clone repo
git clone <your-ml-repo-link>
cd <repo-name>

# Install dependencies
pip install -r requirements.txt

# Train model
python src/train.py

# Evaluate
python src/evaluate.py
```
## 🔗 Integration with Data Warehouse

This ML system depends on structured data from a separate warehouse project:

- Medallion Architecture (Bronze → Silver → Gold)  
- PostgreSQL-based warehouse  
- ETL pipelines for cleaning and transformation  

👉 **Make sure to:**

1. Run the warehouse pipeline  
2. Export Gold layer data  
3. Load it into this ML pipeline  

---

## ⚠️ Limitations

- No real-time data (traffic, weather not included)  
- Moderate accuracy due to complex logistics behavior  
- Dataset constraints may limit generalization  

---

## 🔮 Future Work

- Real-time prediction system  
- Deep learning models  
- Reinforcement learning for delivery optimization  
- Integration with live logistics systems  

---

## 👨‍💻 Authors
  
- Vetcha Venkata Sai Pavan
- Vansh Dev 

---

## 📄 License

This project is for academic / research purposes.
