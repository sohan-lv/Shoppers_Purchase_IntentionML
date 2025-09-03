# Predicting Online Shopper's Purchase Intentions

This project aims to predict whether an online user will complete a purchase during a browsing session. It applies multiple machine learning models and advanced techniques like class imbalance handling and experiment tracking using MLflow. The approach is inspired by the academic paper:

> Sakar et al. (2018). Real-time prediction of online shoppers’ purchasing intention using multilayer perceptron and LSTM recurrent neural networks. *Neural Computing and Applications, 31*, 6893–6908.  
> [Read the Paper](https://link.springer.com/article/10.1007/s00521-018-3523-0)

---

## Project Presentation

- View the full presentation [here](deliverables/Shopper_Intention_Prediction_Presentation.pdf)

---

## Business Use Case

**Problem**: E-commerce platforms often face high rates of cart abandonment and user drop-off. Identifying high-intent customers in real-time can:
- Increase conversion rates through targeted actions
- Reduce marketing waste on low-intent users
- Improve personalized recommendations and user experience

**Use Case Scenarios**:
- Trigger discounts or nudges when high-intent is predicted
- Prioritize customer support/chatbot resources
- Inform A/B testing strategies for landing pages and checkout flows

---

## ML Concepts Used

### Preprocessing & Feature Engineering
- Encoding categorical features (`Month`, `VisitorType`, etc.)
- Scaling numerical values
- Creating training/test splits with **stratified sampling**

### Imbalance Handling
- Applied **SMOTE** to synthetically oversample the minority (purchase) class
- Evaluated results using **F1-score** and **ROC-AUC** (better for imbalance than accuracy)

### Models Trained
- **Logistic Regression** (with hyperparameter tuning)
- **Decision Tree**
- **Random Forest**
- **SVC (Support Vector Classifier)**
- **MLPClassifier (Neural Net)**
- **XGBoost Classifier**

### Experiment Tracking
- Tracked all model runs using **MLflow**
- Logged metrics, parameters, and models for reproducibility
- Each experiment was versioned and compared with automated metrics

---

## Key Insights

- **Exit Rate** and **Page Values** are strong predictors of purchase
- **Weekend users** show slightly different behavior from weekday users
- **Random Forest** and **XGBoost** consistently outperformed others
- **MLPClassifier** performance aligns closely with results from literature

---

## Conclusion

This project shows how e-commerce platforms can leverage ML to:
- Predict and influence customer purchase decisions
- Build real-time personalization pipelines
- Increase revenue through data-driven optimization


