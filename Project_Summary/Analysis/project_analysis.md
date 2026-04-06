# Project Analysis
## INX Future Inc — Employee Performance | IABAC™

---

## 1. Algorithm Selection

### Why Random Forest?

| Algorithm | CV Accuracy | Test Accuracy | Chosen? |
|---|---|---|---|
| Logistic Regression | 72% | 73% | No |
| SVM | 83% | 84% | No |
| Gradient Boosting | 88% | 89% | No |
| **Random Forest** | **92%** | **93%** | ✅ Yes |

Random Forest was selected because:
- Highest accuracy across all metrics
- Handles mixed data types and scales well
- Provides interpretable feature importance scores
- Robust to overfitting via ensemble averaging

---

## 2. Data Processing Choices

| Decision | Reason |
|---|---|
| Dropped `EmpNumber` | Identifier — no predictive value |
| Binary map for `OverTime`, `Attrition` | Only 2 values — simple 0/1 is sufficient |
| Ordinal encoding for `BusinessTravelFrequency` | Natural order exists (None < Rarely < Frequently) |
| One-hot encoding for `Gender`, `Department`, `JobRole` etc. | No natural order — avoid false ranking |
| Oversampling minority classes | Rating 2 (16%) and Rating 4 (11%) are underrepresented |
| Top 25 features selected | Reduces noise, speeds up training without accuracy loss |

---

## 3. Top 3 Important Features

1. **EmpLastSalaryHikePercent** (Importance: ~0.184)
   - Highest predictive power
   - Excellent performers consistently received higher hikes
   - Clear policy lever management can act on

2. **EmpEnvironmentSatisfaction** (Importance: ~0.172)
   - Second strongest predictor
   - Low satisfaction = high probability of low performance rating
   - Actionable: workspace improvements, culture change

3. **YearsSinceLastPromotion** (Importance: ~0.082)
   - Longer gaps → lower performance
   - Indicates disengagement from stalled career growth

---

## 4. Department-wise Findings

| Department | Avg Rating | Status |
|---|---|---|
| Development | 3.086 | ✅ Best |
| Data Science | 3.050 | ✅ Good |
| Research & Development | 2.921 | ⚠️ Average |
| Human Resources | 2.926 | ⚠️ Average |
| Sales | 2.861 | ❌ Below Average |
| Finance | 2.776 | ❌ Worst |

---

## 5. Key Analytical Findings

- **Class imbalance** was a key challenge (Rating 3 = 72.8%) — handled with oversampling
- **Salary hike** and **environment satisfaction** together explain the majority of performance variation
- **Overtime** slightly negatively correlates with performance
- **Training frequency** positively correlates — more training = better performance
- **Promotion gaps** act as a disengagement signal
