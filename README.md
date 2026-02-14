# 🏥 Medical Insurance Cost Prediction

![Python](https://img.shields.io/badge/Python-3.14-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-green)

## 📌 Project Overview
This project analyzes medical insurance data to identify the key drivers of healthcare costs and predicts individual premiums with high accuracy. 

By moving beyond simple linear regression and using a **Random Forest Regressor**, we successfully captured non-linear interactions (specifically between BMI and Smoking), achieving an **R² Score of 0.87**.

## 📊 Key Business Insights
Our analysis revealed three critical factors driving insurance costs:

1.  **The "Smoker" Penalty:** Smoking is the #1 cost driver. Smokers pay on average **4x more** than non-smokers (~$32,000 vs. ~$8,000).
2.  **The Obesity Multiplier:** High BMI (>30) alone does not significantly raise costs. However, **Obesity + Smoking** creates a "super-risk" category where costs skyrocket to over $35,000.
3.  **Age Progression:** Costs increase linearly with age, adding approximately **$250 per year** to the premium.

## 🏆 Model Performance
We compared a baseline Linear Regression model against a Random Forest model. The Random Forest significantly outperformed the baseline by capturing the complex interaction between BMI and smoking.

| Model | R² Score | MAE (Mean Absolute Error) | RMSE |
| :--- | :--- | :--- | :--- |
| Linear Regression (Baseline) | 0.78 | ~$4,180 | ~$6,065 |
| **Random Forest (Final)** | **0.87** 🚀 | **~$2,484** | **~$4,576** |

> **Result:** The final model explains **87%** of the variance in insurance costs and is accurate within ~$2,500 on average.

## 📂 Project Structure
```text
insurance-claim-cost-prediction/
├── data/
│   ├── raw/                   # Original dataset
│   └── processed/             # Cleaned data ready for modeling
├── models/
│   └── insurance_model.pkl    # Trained model file (Random Forest)
├── notebooks/
│   ├── 01_data_understanding.ipynb   # Initial data checks
│   ├── 02_eda.ipynb                  # Visualizing Smoker vs. BMI trends
│   ├── 03_feature_engineering.ipynb  # Log transformations
│   ├── 04_modeling.ipynb             # Training & Evaluation
│   └── 05_model_interpretation.ipynb # SHAP analysis (Explainable AI)
├── reports/
│   ├── insights.md            # Detailed business analysis
│   └── metrics.md             # Technical performance report
├── src/
│   ├── preprocessing.py       # Data cleaning & pipeline script
│   └── train.py               # Automated training script
├── requirements.txt           # Python dependencies
└── README.md                  # Project documentation

Gemini said
Here is a professional, portfolio-ready README.md file for your project.

This is the first thing recruiters will see. It highlights your Business Insights and Model Accuracy (0.87) immediately, proving you can deliver value, not just write code.

📄 Copy & Paste into README.md
Markdown
# 🏥 Medical Insurance Cost Prediction

![Python](https://img.shields.io/badge/Python-3.14-blue)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Completed-green)

## 📌 Project Overview
This project analyzes medical insurance data to identify the key drivers of healthcare costs and predicts individual premiums with high accuracy. 

By moving beyond simple linear regression and using a **Random Forest Regressor**, we successfully captured non-linear interactions (specifically between BMI and Smoking), achieving an **R² Score of 0.87**.

## 📊 Key Business Insights
Our analysis revealed three critical factors driving insurance costs:

1.  **The "Smoker" Penalty:** Smoking is the #1 cost driver. Smokers pay on average **4x more** than non-smokers (~$32,000 vs. ~$8,000).
2.  **The Obesity Multiplier:** High BMI (>30) alone does not significantly raise costs. However, **Obesity + Smoking** creates a "super-risk" category where costs skyrocket to over $35,000.
3.  **Age Progression:** Costs increase linearly with age, adding approximately **$250 per year** to the premium.

## 🏆 Model Performance
We compared a baseline Linear Regression model against a Random Forest model. The Random Forest significantly outperformed the baseline by capturing the complex interaction between BMI and smoking.

| Model | R² Score | MAE (Mean Absolute Error) | RMSE |
| :--- | :--- | :--- | :--- |
| Linear Regression (Baseline) | 0.78 | ~$4,180 | ~$6,065 |
| **Random Forest (Final)** | **0.87** 🚀 | **~$2,484** | **~$4,576** |

> **Result:** The final model explains **87%** of the variance in insurance costs and is accurate within ~$2,500 on average.

## 📂 Project Structure
```text
insurance-claim-cost-prediction/
├── data/
│   ├── raw/                   # Original dataset
│   └── processed/             # Cleaned data ready for modeling
├── models/
│   └── insurance_model.pkl    # Trained model file (Random Forest)
├── notebooks/
│   ├── 01_data_understanding.ipynb   # Initial data checks
│   ├── 02_eda.ipynb                  # Visualizing Smoker vs. BMI trends
│   ├── 03_feature_engineering.ipynb  # Log transformations
│   ├── 04_modeling.ipynb             # Training & Evaluation
│   └── 05_model_interpretation.ipynb # SHAP analysis (Explainable AI)
├── reports/
│   ├── insights.md            # Detailed business analysis
│   └── metrics.md             # Technical performance report
├── src/
│   ├── preprocessing.py       # Data cleaning & pipeline script
│   └── train.py               # Automated training script
├── requirements.txt           # Python dependencies
└── README.md                  # Project documentation
```

🚀 How to Run This Project
1. Clone the Repository
```
git clone [https://github.com/YOUR_USERNAME/insurance-claim-prediction.git](https://github.com/suso-van/insurance-claim-prediction.git)
cd insurance-claim-prediction
```
2. Create Virtual Environment
```
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```
3. Install Dependencies
```
pip install -r requirements.txt
```
4. Train the Model
Run the automated training script to generate the model file:

```
python src/train.py
```
Output: Saves the trained model to models/insurance_model.pkl

🛠️ Technologies Used
```
Python: Core programming language.

Pandas & NumPy: Data manipulation.

Matplotlib & Seaborn: Data visualization.

Scikit-Learn: Machine Learning (Random Forest, Pipelines).

SHAP: Model interpretability (Explainable AI).
```

🔮 Future Improvements
Deploy the model as a REST API using FastAPI or Flask.

Build a simple web interface using Streamlit for users to estimate their premiums.
