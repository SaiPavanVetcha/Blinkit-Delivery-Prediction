# 🤖 Machine Learning & AI Approach

The framework evaluates multiple models to predict the likelihood of delivery delays based on order features.

### 📈 Model Performance Comparison

| Model                | Accuracy | Precision | Recall | F1-Score |
|---------------------|----------|-----------|--------|----------|
| Random Forest       | 0.63     | 0.63      | 0.63   | 0.63     |
| XGBoost             | 0.61     | 0.61      | 0.61   | 0.61     |
| Logistic Regression | 0.58     | 0.58      | 0.58   | 0.58     |

- **Best Performer:** The **Random Forest** model achieved the highest performance with:
  - Accuracy: **63%**
  - Cross-validated AUC: **0.679**

---

## 🚀 Reinforcement Learning (Future Scope)

A **Q-Learning** approach is proposed to optimize delivery partner assignment:

- **State Space:** Distance, order value, and customer type  
- **Action Space:** Selection of a delivery partner  
- **Reward Function:**  

  `Reward = Customer Rating - Delivery Delay`

This approach aims to dynamically improve assignment decisions to maximize customer satisfaction while minimizing delays.
