# 🏥 Medical Insurance Cost Prediction

## 🔍 Overview

This project predicts individual medical insurance expenses based on personal attributes.

### Workflow:
- 📊 **EDA**: Understand patterns, relationships, and feature importance  
- 🤖 **Modeling**: Build and compare regression models

> ✅ **Best Model:** Gradient Boosting Regressor  
> 📈 **R² = 0.87**, 🧮 **MAE ≈ $2,046**

---

## 📂 Dataset

Uses `insurance.csv` with the following columns:

- `age`: Age of the beneficiary  
- `sex`: Gender  
- `bmi`: Body Mass Index  
- `children`: Number of dependents  
- `smoker`: Smoking status  
- `region`: Residential region (US)  
- `expenses`: Medical insurance cost (target)

---

## 📌 Key Insights from EDA

- `expenses` is **right-skewed** → log-transformed
- **Smokers** have significantly higher costs
- **Obese smokers** are highest risk → engineered `obese_smoker` flag
- Added `bmi_category` for better segmentation

---

## 🤖 Models Used & Results

| Model                       | R² Score | MAE ($)     |
|----------------------------|----------|-------------|
| Gradient Boosting Regressor| 0.8676   | 2,045.68    |
| Random Forest Regressor    | 0.8472   | 2,092.97    |
| Multiple Linear Regression | 0.8215   | 3,698.86    |
| Ridge Regression           | 0.8215   | 3,674.08    |

✅ Ensemble models captured non-linear patterns better than linear ones.

---

