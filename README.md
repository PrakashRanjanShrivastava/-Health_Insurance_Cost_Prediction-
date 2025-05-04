 # 🏥 Health Insurance Expense Prediction - Capstone Project

This project aims to predict individual medical expenses billed by health insurance using a supervised regression approach. By understanding how demographic and personal health attributes influence insurance costs, this model can help insurance providers make informed premium decisions and allow consumers to understand their risk profiles.

---

## 📌 Problem Statement

To estimate the **medical insurance cost** for an individual based on factors like age, sex, BMI, number of children, smoking habits, and region. The dataset provides a foundation to train a model that can predict charges with minimal error.

---

## 🧾 Dataset Overview

The dataset consists of **1338 records** and **7 features**:
- `age`: Age of the primary beneficiary
- `sex`: Gender of the beneficiary
- `bmi`: Body Mass Index (an indicator of health)
- `children`: Number of dependents
- `smoker`: Whether the person is a smoker
- `region`: Residential area in the US
- `charges`: Target variable – medical insurance cost

---

## 📊 Project Pipeline

1. **Exploratory Data Analysis (EDA):**
   - Visualized distributions of numeric/categorical features.
   - Detected skewness and outliers (especially in BMI and Charges).
   - Found that smokers have significantly higher charges.

2. **Data Preprocessing:**
   - Handled categorical variables using Label Encoding and One-Hot Encoding.
   - Normalized features where necessary using `StandardScaler`.

3. **Model Building:**
   - Applied multiple regression models:
     - Linear Regression
     - Lasso & Ridge Regression
     - Decision Tree
     - Random Forest
   - Evaluated using MAE, RMSE, and R² Score.

4. **Best Model:**
   - Random Forest Regressor yielded the best performance with the lowest RMSE and highest R².

5. **Model Saving:**
   - Final model saved using `pickle` for future deployment.

---

## 💡 Insights

- **Smoking** is the most impactful feature affecting charges.
- **BMI > 30 (Obese)** individuals tend to pay more.
- **Age** and **number of children** also have a positive correlation with medical expenses.
- **Regional variation** in charges is minimal.

---

## 🧠 What Could Be Improved

🔧 **Missing or possible extensions:**
- Add polynomial features to model nonlinear effects (e.g., `age²`, `bmi*age`).
- Apply **GridSearchCV** instead of Random Search for better hyperparameter tuning.
- Consider removing or transforming extreme outliers in `charges` to reduce skew.
- Implement **SHAP** or **LIME** for interpretability.
- Build a simple **Flask API** for deployment.
- Evaluate with Cross-Validation (K-Fold) instead of a single test split.
- Include pipeline automation using `Pipeline` from scikit-learn.

---

## 📈 Evaluation Metrics

| Model                | R² Score | RMSE   |
|---------------------|----------|--------|
| Linear Regression   | 0.74     | ~6058  |
| Ridge Regression    | 0.75     | ~5960  |
| Random Forest       | **0.87** | **~4302** |

---

## ✅ Conclusion & Recommendations

- Smoking cessation programs can substantially reduce insurance claims.
- Obesity and high BMI are cost amplifiers – wellness programs should be promoted.
- Young, non-smoking clients are low risk and could be offered discounted premiums.
- This model can assist in **personalized premium pricing** and **fraud detection**.

---

## 📁 Files

- `capstone__project_insurance.ipynb` – All code and outputs
- `model.pkl` – Trained Random Forest model (if saved)
- `README.md` – Project summary
- `Health_Insurance_Report.pdf` – Full analysis (attached in repository)

---

## 🔗 Libraries Used

- pandas, numpy, matplotlib, seaborn
- scikit-learn
- pickle

## 📬 Contact

Made with ❤️ by [Prakash Ranjan](https://github.com/PrakashRanjanShrivastava)  
📧 prkashranjan22@gmail.com
