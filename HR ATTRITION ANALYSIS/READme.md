# 📌 HR Attrition Analysis Dashboard Using Excel & Power Query

## 🧠 Problem Statement

Employers often overlook the hidden reasons behind rising attrition rates — from low pay and long commutes to poor job satisfaction and work conditions. Today, employees switch jobs faster than ever, driving up recruitment costs and disrupting teams.  
To shed light on this, I analyzed a real-world HR dataset from Kaggle, exploring the key drivers of attrition in a company of 1,470 staff. This project reveals where HR leaders should focus to reduce turnover and keep talent.

---

## 🎯 Objectives

This project was designed to:

- Transform raw CSV data into a structured, clean format using **Power Query**
- Build a dynamic, interactive **Excel dashboard** for HR decision-makers
- Enable stakeholders to filter, slice, and drill down attrition insights easily
- Highlight key drivers influencing attrition
- Provide actionable, visual insights to inform better HR strategies

---

## 🗂️ Dataset Information

- **Source:** [Kaggle Dataset](https://www.kaggle.com/datasets/saadharoon27/hr-analytics-dataset)
- **Format:** CSV
- **Rows:** ~1,470 records
- **Columns:**  
  `EmpID`, `Age`, `Attrition`, `BusinessTravel`, `Department`, `DistanceFromHome`, `Education`, `EducationField`, `EnvironmentSatisfaction`, `Gender`, `JobInvolvement`, `JobRole`, `JobSatisfaction`, `MaritalStatus`, `MonthlyIncome`, `NumCompaniesWorked`, `OverTime`, `PercentSalaryHike`, `PerformanceRating`, `RelationshipSatisfaction`, `StockOptionLevel`, `TotalWorkingYears`, `TrainingTimesLastYear`, `WorkLifeBalance`, `YearsAtCompany`, `YearsInCurrentRole`, `YearsSinceLastPromotion`, `YearsWithCurrManager`, `SalaryBucket`, `Age Bracket`, `% Attrition`, and gender splits.

---

## 🔧 Tools & Technologies

- **Microsoft Excel:** Dashboard design and visualization
- **Power Query:** Data cleaning, transformation & column creation
- **Techniques:** Descriptive analysis, segmentation by department and job roles, correlation analysis
- **Kaggle:** Dataset source

---

## ⚙️ Data Cleaning & Transformation (Power Query)

**Dropped columns:** redundant, constant, or identifiers with little value:

- `EmployeeCount` — constant (1 per row)
- `Over18` — constant value ("Y")
- `StandardHours` — constant
- `AgeGroup` and `Age Bucket` — replaced with `AGE BRACKET`
- `MonthlyRate` and `DailyRate` — replaced by `MonthlyIncome`

**Standardized values:**

- Shortened long job role names for cleaner visuals
- Renamed **Salary Slab** to **Salary Bucket**
- Adjusted ranges (e.g., 5k → 500k) for realistic salary bands
- Multiplied `MonthlyIncome` by 100 to align currency scale

**Created new columns:**

- `Female Attrition` and `Male Attrition`
- `Leaver’s Monthly Income`
- `Leavers Salary Above Overall Average`

**Other steps:**

- Removed duplicates & nulls using `EmpID`
- Ensured consistent data types

---

## 📊 Dashboard Highlights

**Key features and visuals include:**

**KPI Cards:**

- Total Headcount
- Attrition Count
- Average Salary of Leavers
- Average Tenure at Company
- Average Distance from Home

**Charts:**

- Column Chart
- Tree Map
- Bar Chart
- Scatter Plot
- Pie Chart

**Slicers:**

- Department
- Job Role

**Pivot Tables:**

- Dynamic summaries to drill down by department, role, and gender

---

## 🔍 Data Exploration & Insights

### 📌 KPI Cards: Insight

- A moderate attrition rate (~16%) suggests the organization needs targeted retention strategies.
- Leavers have an average experience of 7 years — valuable employees are exiting.

---

### 💼 Job Roles with Highest Attrition

**Insight:**

- 1 out of every 4 leavers is a **Lab Technician** — a critical red flag.
- Sales-related roles show high attrition, hinting at job pressure or target-related stress.
- Roles like **Healthcare Manager** and **HR** show much lower attrition, suggesting stronger satisfaction or career paths.

---

### 🗺️ Department-Age Attrition Heatmap (R&D Focus)

**Insights:**

- Young professionals in **R&D** are leaving at alarming rates — possibly due to limited growth or engagement.
- The age group **24–26** is most vulnerable, suggesting onboarding or early-career support gaps.

---

### 💰 Does Low Salary Contribute to Attrition?

**Insights:**

- Most leavers earn below **₦500K**, facing retention challenges.
- Those earning over **₦1M** are the least likely to leave — compensation matters.
- However, attrition exists across all salary bands — pay is not the sole driver.

---

### 😊 Job Satisfaction Rating of Leavers

**Insights:**

- No leaver reported perfect satisfaction — a sign of workplace dissatisfaction.
- Lower-paid employees (below ₦500k) make up the largest group leaving.
- Highest satisfaction is among those earning **₦1M–₦1.5M**, yet some still leave — other factors (career growth, culture) matter.

---

### ⏰ Overtime Analysis

**Insights:**

- Lab Techs doing overtime correlate with high attrition — potential burnout.
- Sales roles and Support Staff also show overtime pressure.
- Overworking may be linked with dissatisfaction and exits.

---

### 🚗 Salary vs Distance from Home

**Insights:**

- High earners don’t necessarily live closer to the office.
- Commute may influence comfort but not enough to affect salary range.
- A few low earners live far away — possibly increasing stress or dissatisfaction.

---

### 💍 Marital Status % by Attrition

**Insights:**

- Married employees may face work-life balance stressors.
- Many single employees also left — attrition isn’t strictly tied to marital status.
- **Lab Tech** shows high attrition regardless of marital status — deeper role issues may exist.

---

## ✅ Conclusion

- **Lab Technicians** showed the highest attrition.
- Employees aged **24–26** were most likely to leave.
- **Sales Executives** worked more overtime than other roles.
- Employees living farther away tended to earn below **₦500,000**.
- Overtime, low satisfaction, and low pay consistently contribute to exits.
- Strategic intervention is needed — especially for early-career employees and technical roles.

---

## 🔁 Recommendations

- Target **Lab Techs** and **Sales Staff** with tailored retention programs (mentorship, better hours, career growth).
- Improve onboarding and engagement for employees aged **24–26**.
- Address overtime stress via shift management and workload balancing.
- Use pulse surveys to track job satisfaction regularly and respond proactively.
