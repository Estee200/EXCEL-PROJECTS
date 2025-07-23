📌 HR Attrition Analysis Dashboard Using Excel & Power Query
 
🧠 Problem Statement
Employers often overlook the hidden reasons behind rising attrition rates, from low pay and long commutes to poor job satisfaction and work conditions. Today, employees switch jobs faster than ever, driving up recruitment costs and disrupting teams. To shed light on this, I analyzed a real-world HR dataset from Kaggle, exploring the key drivers of attrition in a company of 1,470 staff. This project reveals where HR leaders should focus to reduce turnover and keep tale.
 
***🎯 Objectives
This project was designed to:
•	Transform raw CSV data into a structured, clean format using Power Query
•	Build a dynamic, interactive Excel dashboard for HR decision-makers
•	Enable stakeholders to filter, slice, and drill down attrition insights easily
•	Highlight key drivers influencing attrition
•	Provide actionable, visual insights to inform better HR strategies
 
🗂️ Dataset Information
•	Source: Kaggle – https://www.kaggle.com/datasets/saadharoon27/hr-analytics-dataset
•	Format: CSV
•	Rows: ~1,470 records
•	Columns: EmpID, Age, Attrition, BusinessTravel, Department, DistanceFromHome, Education, EducationField, EnvironmentSatisfaction, Gender, JobInvolvement, JobRole, JobSatisfaction, MaritalStatus, MonthlyIncome, NumCompaniesWorked, OverTime, PercentSalaryHike, PerformanceRating, RelationshipSatisfaction, StockOptionLevel, TotalWorkingYears, TrainingTimesLastYear, WorkLifeBalance, YearsAtCompany, YearsInCurrentRole, YearsSinceLastPromotion, YearsWithCurrManager, SalaryBucket, Age Bracket, % Attrition, and gender splits.
 
***🔧 Tools & Technologies
•	Microsoft Excel: Dashboarding design and visualization
•	Power Query: Data cleaning, transformation & column creation
•	Techniques: Descriptive analysis, segmentation by department and job roles, correlation analysis
•	Kaggle: Dataset Source
 
 Data Cleaning & Transformation (Power Query)
Dropped the following columns because they are either redundant, constants, or identifiers, and may not add value to my analysis:
•	EmployeeCount – Usually a constant (often always 1 per row).
•	Over18 – It has just one constant letter constant ("Y").
•	StandardHours – Often constant.
•	AgeGroup and Age Bucket – I added a new column called AGE BRACKET, so I remove the Age Group Column
•	MonthlyRate and DailyRate – I dropped the two column because I have Monthly Income column already.
•	Replaced the jobe role names to a shorter names so that my dashboard will not look too conjested.
Standardized values:
•	Shortened long job role names for cleaner visuals
•	Renamed Salary Slab to Salary Bucket
•	Replaced ranges (e.g., 5k → 500k) for realistic salary bands
•	Multiplied MonthlyIncome by 100 to align with currency scale
Created new columns to aid my calculation:
•	Female Attrition and Male Attrition.
•	Leaver’s Monthly income
•	Leavers Salary above overall average salary.
Removed duplicates & nulls via EmpID
•	Ensured consistent data types for analysis.
 
📊 Dashboard Highlights
Key features and visuals included:
KPI Cards:
•	Total Headcount
•	Attrition Count
•	Avg. Salary of Leavers
•	Avg. Tenure at Company
•	Avg. Distance from Home
Charts:
•	Column Chart, Tree Map, Bar Chart, Scatter Plot, Pie Chart
Slicers:
•	Department
•	Job Role
Pivot Tables:
•	Dynamic summaries to drill down by department, role, and gender.
 
🧠Data Exploration and Insights
1. KPI Cards:
Insight:
•	A moderate attrition rate (~16%) suggests the organization needs targeted retention strategies.
•	Leavers have an average experience of 7 years, meaning valuable employees are exiting.

2. what is the Job Roles with Highest Attrition.

Insight:
•	One out of every four leavers is a Lab Technician, this is a critical red flag.
•	Sales-related roles also show high attrition, hinting at possible job pressure or target-related stress.
•	Roles like Healthcare Manager and HR show much lower attrition, suggesting stronger satisfaction or career paths.

3. What is the Department-Age Attrition Heatmap (R&D Focus)


Insights:
•	Young professionals in R&D are leaving at alarming rates, possibly due to limited growth or lack of engagement.
•	The age group 24–26 is most vulnerable, suggesting onboarding or early-career support gaps.


4. Does low salary contribute to the Attrition rate?



Insights:
•	Most leavers earn below ₦500K, indicating that lower salary bands face retention challenges.
•	Those earning over ₦1M are the least likely to leave, reinforcing the idea that compensation matters.
•	However, attrition still exists across all salary bands — pay is not the sole driver.


5. What is the Job Satisfaction Rating of Leavers

Insights:
•	No leaver reported a perfect satisfaction score, a clear sign of workplace dissatisfaction.
•	Lower-paid employees (below 500k) make up the largest group leaving the company.
•	the highest satisfaction rating is among those earning 1m–1.5m, yet some still leave, implying other factors besides pay influence their decision (like career growth or culture)



6. Let us see the Overtime Analysis


Insights:
•	Lab Techs doing overtime correlate directly with high attrition, potential burnout.
•	Sales roles and Support Staff also show overtime pressure.
•	Overworking may be linked with dissatisfaction and eventual exits.


7. How about the Salary vs Distance from Home?


Insights:
•	High earners are not necessarily living closer to the office, commute may not influence salary decisions.
•	Distance from home may influence comfort but not enough to affect salary range.
•	A few low earners live far away, possibly increasing stress levels or job dissatisfaction.


8. Show me the Marital Status % by Attrition

Insights:
•	Married employees may have additional stressors affecting their work-life balance
•	A significant number of single employees also left, showing attrition is not strictly tied to marital status.
•	Lab Tech role shows high attrition regardless of status, deeper job role issues may be the root cause.


✅ Conclusion

•	Lab Technicians showed the highest attrition.
•	Employees aged 24–26 were most likely to leave.
•	Sales Executives worked more overtime than other roles.
•	Employees living farther away tended to earn below ₦500,000.
•	Overtime, low satisfaction, and low pay are consistent contributors to exits.
•	Strategic intervention is needed, particularly for early-career employees and those in technical roles.



🔁 Recommendations

•	Target Lab Techs and Sales Staff with tailored retention programs (mentorship, better hours, career growth).
•	Improve onboarding and engagement for employees aged 24–26.
•	Address overtime stress through shift management and workload balancing.
•	Use pulse surveys to track job satisfaction regularly and respond proactively.

<img width="468" height="637" alt="image" src="https://github.com/user-attachments/assets/db24af6a-4803-4acc-84f7-2dd8ea1e0263" />
