# Data Dictionary — INX Future Inc Employee Performance Dataset

## Target Variable

| Column | Type | Description |
|---|---|---|
| PerformanceRating | Integer | Employee performance: 2=Low, 3=Good, 4=Excellent |

## Employee Demographics

| Column | Type | Description |
|---|---|---|
| EmpNumber | String | Unique Employee ID (not used in modeling) |
| Age | Integer | Employee age in years |
| Gender | Categorical | Male / Female |
| MaritalStatus | Categorical | Single / Married / Divorced |
| EducationBackground | Categorical | Field of education (Marketing, Life Sciences, etc.) |
| EmpEducationLevel | Integer | Education level (1-5 scale) |

## Work-related Features

| Column | Type | Description |
|---|---|---|
| EmpDepartment | Categorical | Department (Sales, Development, etc.) |
| EmpJobRole | Categorical | Specific job role |
| EmpJobLevel | Integer | Job level (1-5) |
| BusinessTravelFrequency | Categorical | Travel frequency (Non-Travel / Rarely / Frequently) |
| DistanceFromHome | Integer | Distance from home to office (miles) |
| OverTime | Categorical | Whether employee works overtime (Yes/No) |
| Attrition | Categorical | Whether employee left the company (Yes/No) |

## Satisfaction and Engagement Scores (1-4 scale)

| Column | Type | Description |
|---|---|---|
| EmpEnvironmentSatisfaction | Integer | Satisfaction with work environment |
| EmpJobSatisfaction | Integer | Satisfaction with job role |
| EmpJobInvolvement | Integer | Level of job involvement/engagement |
| EmpRelationshipSatisfaction | Integer | Satisfaction with workplace relationships |
| EmpWorkLifeBalance | Integer | Work-life balance rating |

## Compensation

| Column | Type | Description |
|---|---|---|
| EmpHourlyRate | Integer | Hourly compensation rate |
| EmpLastSalaryHikePercent | Integer | Last salary hike percentage |

## Experience and Tenure

| Column | Type | Description |
|---|---|---|
| NumCompaniesWorked | Integer | Number of companies worked at before INX |
| TotalWorkExperienceInYears | Integer | Total work experience in years |
| ExperienceYearsAtThisCompany | Integer | Years at INX |
| ExperienceYearsInCurrentRole | Integer | Years in current role |
| YearsSinceLastPromotion | Integer | Years since last promotion |
| YearsWithCurrManager | Integer | Years with current manager |

## Learning and Development

| Column | Type | Description |
|---|---|---|
| TrainingTimesLastYear | Integer | Number of training sessions attended last year |
