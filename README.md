# Market Feasibility Study: Predicting Sales Potential in India of a Japanese Car Company based on sales data of both regions
A data science project analyzing the feasibility for a Japanese automotive company to enter and succeed in the Indian car market.
This study uses machine learning models trained on Japanese sales data and applies them to Indian customer demographics to predict car purchase likelihood, guiding strategic market entry decisions.


## 📋 Project Overview

This project investigates whether the purchasing patterns and demographic correlations observed in the Japanese market hold true for the Indian market — helping the company assess market viability and identify high-value customer segments.

✅ **Model trained on Japanese customer sales data**  
✅ **Applied to Indian customer profiles (same features)**  
✅ **Estimates potential sales volumes & identifies target segments**

> **“Can our success factors in Japan predict comparable outcomes in India?”**

---

## 🎯 Key Features

- **Predictive Analysis:** LightGBM machine learning model with ~70% test accuracy on Japanese data.
- **Customer Segmentation:** Automatically classifies Indian customers by purchase probability (high / medium / low value).
- **Sales Target Evaluation:** Tests if current Indian customer pool can realistically achieve a 10,000-car sales target.
- **Interactive Prediction Tool:** Enter individual customer details to estimate purchase probability.
- **Batch Processing:** Runs predictions on thousands of Indian customer records to produce detailed CSV insights.

---

## 📊 Model Performance Summary

| Metric                         | Value   |
|--------------------------------|---------|
| **Test Accuracy (Japan)**      | 69.7%   |
| **ROC AUC Score**              | 0.781   |
| **Training Accuracy**          | 73.1%   |
| **Predicted Purchase Rate (India)** | 59.1% |

### 🥇 Model Comparison

| Model              | Training Accuracy | Test Accuracy | Status       |
|--------------------|-------------------|---------------|--------------|
| **LightGBM**       | 73.1%             | **69.7%**     | ✅ Best Fit  |
| XGBoost            | 76.1%             | 69.0%         | Good         |
| Logistic Regression| 68.1%             | 67.8%         | Stable       |
| Random Forest      | 99.9%             | 65.4%         | Overfitting  |

---

## 🗂️ Project Structure

market_feasibility_project/
├── new.ipynb # Jupyter notebook: data cleaning, training & analysis
├── predict_car_purchase.py # CLI tool for interactive & batch predictions
├── lightgbm_model.pkl # Trained LightGBM model (Japanese data)
├── scaler.pkl # StandardScaler for feature scaling
├── label_encoder.pkl # LabelEncoder for gender
├── indian_data_with_predictions.csv # Indian customers + prediction probabilities
├── sales_analysis_results.csv # Detailed marketing & sales analysis
├── Copy of JPN Data.xlsx # Original Japanese training data
├── Copy of IN_Data.xlsx # Indian customer profiles
└── business_report.md # Markdown business report

y

## 🚀 Quick Start

### 🔗 Installation

📈 Business Insights
📊 Market Simulation on Indian Data
Target Sales Goal: 10,000 cars

Predicted Sales: 41,365 cars out of 70,000 customers

Success Rate: 59.1%

✅ Status: Target Achievable with current customer base

Segment	Probability Range	Customer Count	Share
High-Value Prospects	≥80%	23,494	33.6%
Medium-Value Prospects	60-80%	7,460	10.7%
Low-Value Prospects	<60%	39,046	55.8%

🛠 Technical Details
🔍 Feature Engineering
Feature	Description	Processing
CURR_AGE	Customer's current age	Standardized via StandardScaler
ANN_INCOME	Annual income in Rupees	Standardized
DT_MAINT_CATEGORY	Maintenance period category	Binned into 4 groups (days since 2019-07-01)
GENDER_ENCODED	Gender (F=0, M=1)	Label encoded

🛠 Data Pipeline
Maintenance dates converted to days since 2019-07-01.

Maintenance periods categorized into: <200, 200-360, 360-500, 500+ days.

Gender encoded: F → 0, M → 1.

Currency conversion: Japanese Yen → Indian Rupees using exchange rate 0.59.

💼 Business Strategy Recommendations
Short-Term (0-3 Months)
Focus on the 23,494 customers with ≥80% probability.

Launch hyper-targeted campaigns & premium follow-ups.

Medium-Term (3-12 Months)
Build referral & loyalty programs.

Expand to similar demographic segments in Tier 1 & Tier 2 cities.

Long-Term (1+ Years)
Gather actual Indian purchase data to retrain the model for local patterns.

Establish financing & dealership partnerships.

⚠️ Caveats & Next Steps
⚠ Model trained on Japanese purchasing behavior.
While demographic features align, validation on real Indian sales outcomes is required before large-scale rollouts.

🔄 Retrain regularly as Indian market evolves.

📝 License
📜 MIT License — for academic, research & internal business analysis.

