# INX Future Inc — Employee Performance Analysis
## Project Summary | IABAC™ Data Science Project

---

## 1. Project Overview

INX Future Inc, a leading data analytics and automation solutions provider with 15+ years of global presence, has been experiencing declining employee performance indexes. Client satisfaction dropped by 8 percentage points, and internal escalations increased. CEO Mr. Brain initiated this data science project to identify root causes and predict employee performance — enabling targeted interventions without broadly impacting employee morale.

---

## 2. Dataset Summary

| Property | Value |
|---|---|
| Total Records | 1,200 employees |
| Features | 27 (26 input + 1 target) |
| Target Variable | PerformanceRating (2=Low, 3=Good, 4=Excellent) |
| Missing Values | None |
| Class Distribution | Rating 2: 16.2% | Rating 3: 72.8% | Rating 4: 11.0% |

---

## 3. Algorithm and Training Method

**Primary Model: Random Forest Classifier** (with GridSearchCV hyperparameter tuning)

| Model | CV Accuracy | Test Accuracy |
|---|---|---|
| Logistic Regression | ~72% | ~73% |
| Support Vector Machine | ~83% | ~84% |
| Gradient Boosting | ~88% | ~89% |
| **Random Forest (Tuned)** | **~92%** | **~93%** |

**Why Random Forest?**
- Handles mixed data types well
- Robust to outliers and feature scaling
- Provides interpretable feature importance scores
- Excellent ensemble performance on tabular HR data

**Techniques Used:**
- **SMOTE** (Synthetic Minority Oversampling Technique) to address class imbalance
- **StandardScaler** for feature normalization
- **StratifiedKFold (k=5)** cross-validation
- **GridSearchCV** for hyperparameter optimization

---

## 4. Top 3 Important Factors Affecting Employee Performance

### Factor 1: EmpLastSalaryHikePercent (Last Salary Hike %)
Employees receiving higher salary hikes demonstrate significantly better performance. Excellent performers (Rating 4) received a mean hike of ~20%, versus ~11% for low performers.

### Factor 2: EmpEnvironmentSatisfaction (Work Environment Satisfaction)
Employees who feel satisfied with their work environment perform substantially better. Low environment satisfaction scores (1-2) strongly predict low performance ratings.

### Factor 3: EmpJobSatisfaction (Job Satisfaction)
Job satisfaction is a direct predictor of performance output. Employees with satisfaction scores of 3-4 are 2.3x more likely to be rated as excellent performers.

---

## 5. Department-wise Performance

| Department | Avg Rating | % Excellent (4) | % Low (2) |
|---|---|---|---|
| Development | 3.12 | 12.8% | 15.1% |
| Data Science | 3.09 | 11.6% | 14.7% |
| Research & Development | 3.07 | 10.9% | 16.4% |
| Finance | 3.05 | 10.2% | 17.2% |
| Sales | 3.03 | 9.8% | 18.1% |
| Human Resources | 2.98 | 8.5% | 19.6% |

---

## 6. Recommendations to Improve Employee Performance

1. **Revise Salary Hike Policy** — Implement performance-linked pay with clear tiers. Ensure salary hikes of at least 15% for good performers to sustain motivation.

2. **Improve Work Environment** — Conduct quarterly environment satisfaction surveys. Invest in workspace improvements, ergonomics, and remote work flexibility.

3. **Boost Job Satisfaction** — Provide meaningful roles aligned with employee interests. Introduce job rotation and cross-functional project opportunities.

4. **Training Investment** — Employees with 3+ training sessions per year show markedly better performance. Mandate at least 3 training sessions annually per employee.

5. **Manage Overtime** — Excessive overtime correlates with reduced performance. Introduce proper workload distribution and flexible scheduling.

6. **Focus on Human Resources and Sales Departments** — These have the highest proportion of low performers. Department-specific coaching and mentoring programs are recommended.

7. **Predictive Hiring** — The trained model can be integrated into the HR hiring pipeline to predict a candidate's likely performance rating before onboarding.

---

## 7. Project Structure

```
INX_Project/
├── Project_Summary/
│   ├── Requirement/
│   ├── Analysis/
│   └── Summary/  ← You are here
├── data/
│   ├── raw/                 ← Original dataset
│   ├── processed/           ← Processed data, model, charts
│   └── external/
├── src/
│   ├── Data_Processing/
│   │   ├── data_processing.ipynb
│   │   └── data_exploratory_analysis.ipynb
│   ├── models/
│   │   ├── train_model.ipynb
│   │   └── predict_model.ipynb
│   └── visualization/
│       └── visualize.ipynb
└── references/
    └── data_dictionary.md
```
