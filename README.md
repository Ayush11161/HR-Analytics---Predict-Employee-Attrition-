#  HR Analytics – Employee Attrition Prediction

###  Overview
This project aims to **analyze and predict employee attrition** using an HR dataset containing demographic, job-related, and performance variables.  
The goal is to help organizations identify key factors that drive employee turnover and develop data-driven retention strategies.

---

##  Dataset
**Source:** IBM HR Analytics Employee Attrition Dataset  
**Records:** 1,470 employees  
**Features:** 35 columns (Age, Department, MonthlyIncome, OverTime, JobSatisfaction, etc.)  
**Target Variable:** `Attrition` (Yes / No)

| Feature Example | Description |
|-----------------|--------------|
| `Age` | Employee age |
| `Department` | Department name (Sales, R&D, HR) |
| `OverTime` | Whether employee works overtime |
| `JobSatisfaction` | Satisfaction level (1–4) |
| `YearsAtCompany` | Total years spent in the company |
| `Attrition` | Target variable – whether employee left the company |

---

##  Tools & Technologies
- **Programming:** Python (Pandas, NumPy, Scikit-learn)
- **Visualization:** Power BI, Seaborn, Matplotlib
- **Model Explainability:** SHAP
- **Data Preprocessing:** ColumnTransformer, OneHotEncoder, StandardScaler
- **Version Control:** Git & GitHub

---

##  Project Workflow

### 1️. Data Understanding & Cleaning
- Checked for missing values and duplicates  
- Converted categorical variables and encoded target (`Attrition → 0/1`)  
- Removed irrelevant columns (`EmployeeNumber`, `Over18`, `StandardHours`)

### 2️. Exploratory Data Analysis (EDA)
- Visualized attrition distribution across departments, age groups, income levels  
- Found strong correlation between **OverTime**, **MonthlyIncome**, and **Attrition**
- Identified patterns:
  - Employees doing overtime are **3× more likely** to leave  
  - Employees with low job satisfaction or low income tend to churn more

### 3️. Feature Engineering
- Created new categorical bands (e.g., `IncomeBand`, `TenureGroup`)
- One-Hot Encoding for categorical columns
- Standardization of numerical features

### 4️. Model Building
Trained and evaluated multiple classification algorithms:
| Model | Accuracy | ROC-AUC | Key Notes |
|--------|-----------|----------|------------|
| Logistic Regression | ~83% | 0.87 | Simple, interpretable |
| Decision Tree | ~85% | 0.88 | Captures nonlinear relations |
| Random Forest | **87–89%** | **0.90+** | Best performing model |

### 5️. Model Explainability
- Used **SHAP** to identify top predictors of attrition:
  - `OverTime`, `MonthlyIncome`, `JobRole`, `JobSatisfaction`, `Age`
- Created dependence plots and summary plots for interpretability.

### 6️. Dashboard & Insights (Power BI)
Developed an **interactive dashboard** showing:
- Attrition by department, gender, job role  
- Attrition vs. monthly income and overtime  
- Employee satisfaction and retention trends  
- Predictive insights from the ML model

---

##  Key Findings
1. Employees working overtime have **significantly higher attrition rates**.
2. Attrition is **highest among younger employees (25–35 years)**.
3. Low **JobSatisfaction** and **WorkLifeBalance** are major churn drivers.
4. Departments with higher **OverTime** ratios experience the most turnover.
5. Salary increments and managerial support can reduce attrition risk.

---

##  Deliverables
- ✅ `HR_Attrition_Prediction.ipynb` – main notebook  
- ✅ `attrition_predictions_for_pbi.csv` – model output for Power BI  
- ✅ Power BI dashboard – interactive visualization of key insights  
- ✅ `HR_Attrition_Report.pdf` – 2-page project summary  
- ✅ Trained model (`rf_model.joblib`)

---

##  Dashboard Preview
**Power BI Visuals:**
- 📉 Attrition by Department  
- 💸 Attrition vs Monthly Income  
- ⏰ Attrition by OverTime  
- 😊 Job Satisfaction vs Attrition  
- 🧑‍💼 High-risk employee segments (based on prediction probability)

---

##  Business Recommendations
- Improve work-life balance and limit overtime workloads.  
- Introduce employee engagement and satisfaction programs.  
- Offer competitive salary packages for mid-level employees.  
- Strengthen manager-employee relationships through regular feedback.  

---

##  Learning Outcomes
- Built a complete **end-to-end data analysis and prediction pipeline**
- Gained experience in **EDA, ML modeling, and interpretability**
- Improved proficiency in **Power BI dashboards** and storytelling with data
- Understood how data analytics can drive **HR decisions** and **employee retention**

---

##  Author
**Ayush Rawat**  
🎓 B.Tech Student | Data Analyst Enthusiast  
📧 rawatayush608@gamil.com  
💻 [GitHub Profile](https://github.com/Ayush11161) | [LinkedIn](https://linkedin.com/in/yourprofile)

---

⭐ *If you found this project insightful, give it a star on GitHub!* ⭐# HR-Analytics---Predict-Employee-Attrition-
