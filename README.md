# 📊 Car Seat Sales Prediction & Model Comparison

## 📌 Project Overview

Accurate sales forecasting is critical for retail organizations to optimize inventory planning, pricing strategy, and marketing investment.  
This project develops and evaluates multiple predictive models to forecast car seat sales using store-level demographic, pricing, and merchandising attributes.

The analysis progresses from interpretable baseline models to advanced machine learning techniques, followed by a structured model comparison and final model selection.

---

## 🎯 Business Objective

The primary objectives of this project are to:

- Predict car seat sales across retail stores  
- Compare multiple modeling approaches using a consistent evaluation framework  
- Balance predictive accuracy with interpretability and business usability  
- Select a final, production-ready model for deployment  

Sales are measured in **hundreds of units**, enabling scalable interpretation for real-world retail environments.

---

## 📂 Dataset Description

The dataset contains store-level attributes related to competition, demographics, and merchandising.

### 🎯 Target Variable

- **Sales** – Number of car seats sold (measured in hundreds)

### 📈 Predictor Variables

- **CompPrice** – Competitor pricing  
- **Income** – Average local income (in $000s)  
- **Advertising** – Advertising spend (in $000s)  
- **Population** – Local population size (in $000s)  
- **Price** – Store price  
- **ShelfLoc** – Shelf location quality (Good / Medium / Bad)  
- **Age** – Average customer age  
- **Education** – Average education level  
- **Urban** – Urban location indicator  
- **US** – U.S. store indicator  

The variable **Store** is excluded from modeling as it serves only as a unique identifier.

---

## 🧠 Modeling Approach

To ensure a fair and robust comparison, all models were:

- Trained on the same dataset  
- Evaluated using k-fold cross-validation  
- Compared using **Root Mean Squared Error (RMSE)**  

### Models Implemented

| Model | Purpose |
|-----|--------|
| Multiple Linear Regression (MLR) | Interpretable baseline model |
| CART | Simple non-linear decision rules |
| Random Forest | High-accuracy ensemble model |
| Neural Network | Flexible model for complex patterns |

---

## 📊 Model Performance Comparison

All models were evaluated using cross-validated RMSE.

| Model | CV Folds | RMSE |
|-----|---------|------|
| Random Forest | 5 | **5.13** |
| Neural Network | 5 | 5.19 |
| Multiple Linear Regression | 5 | 5.23 |
| CART | 5 | 5.57 |

📌 Lower RMSE indicates better predictive accuracy.

---

## 🏆 Final Model Selection

### ✅ Recommended Model: **Random Forest**

**Why Random Forest?**

- Lowest cross-validated RMSE  
- Strong generalization to unseen data  
- Robust to noise and outliers  
- Captures non-linear relationships and feature interactions  
- Scales well for production environments  

While Neural Networks achieved comparable accuracy, Random Forest offers a superior balance between **performance, stability, and operational reliability**.

---

## 🔍 When to Use Other Models

### Multiple Linear Regression
- High interpretability  
- Useful for stakeholder communication and baseline benchmarking  

### CART
- Simple, rule-based explanations  
- Useful for instructional or decision-rule contexts  

### Neural Network
- Effective for highly complex, non-linear patterns  
- Best suited when interpretability is not a priority  

