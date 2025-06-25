PROBLEM STATEMENT

Collecting call data is an easy procedure for many organizations, however, the data is stored in spreadsheets and is not readily accessible for interpretation. Business executives require a way to track performance, find bottlenecks, and act in an efficient manner visually. The Excel dashboard provided in this solution renders call logs into a decision-making management tool.

**OBJECTIVES**

After exploring the dataset, I crafted business questions to guide the analysis. These questions were inspired by patterns I observed in the data:

1. **Key Metrics**
    - Total number of calls
    - Total amount generated
    - Total duration of calls
    - Average caller ratings
    - Maximum call duration
2. **Monthly Trend**: What’s the trend of calls over the months?
3. **Weekly Volume**: How do calls vary across the days of the week?
4. **Department Performance**: How many issues were resolved vs. unresolved across departments?
5. **Satisfaction Levels**: What are the distribution and trends of customer satisfaction ratings?
6. **Agent Contribution**: How many calls did each agent handle, and how much revenue did they generate?
7. **Resolution Patterns by Agent**: How do agents perform across various departments?

## Dataset Source

I sourced the call center dataset from Kaggle. https://www.kaggle.com/datasets/ashishpandey5210/call-center-dataset which aligned well with a recent lecture I attended on customer service analytics.

# DATA TRANSFORMATION (power query)

1. Created a “Duration Bucket”
    - Short Call (< 120 seconds)
    - Medium Call (120–300 seconds)
    - Long Call (> 300 seconds)
2. Created a second column converting durations to seconds (whole number). I did so to help me when grouping.
3. Added a new column where I converted the Avg Duration Column to a true Duration type because it was giving “ERROR” alert when I tried changing it without conversion.
4. Extracted Time only
5. Renamed to Avg Duration
- AvgTalkDuration column comprises of date and time, so I performed the following:
- Filtered the “null” rows out.
- Reinterpreted the Speed Ratings column as a proxy for **Purchase Amount**, given that no monetary field was available
- Replaced “Y” and “N” with “YES” and “NO” in the Answered and Resolved column for clarity
- Converted the Date column type to Date because it comprises of date and time.
- Removed duplicate values from the Call ID column

I took the data to power query for a transformation. Below is the summary of the cleaning and transformation steps I took:

# Data Exploration & Insights

***Question 1: Key metrics*

***Question 2:** What is the trend of calls over the months?.*  

Insight:

**March recorded the highest number of calls (175), slightly surpassing January (171) and February (168).**

While the difference across months is not drastic, the **upward trend in March may indicate a seasonal increase in customer engagement or issues.**

***Questions 3:** How do calls vary across the days of the week?*

Insight:

**Wednesday recorded the highest number of calls (96), indicating a midweek peak in customer engagement or issues.**

This suggests that **workload or support demand tends to be heaviest midweek,** especially compared to Thursday (51), which had the lowest

***Questions 4:** How many issues were resolved vs. unresolved across departments?*

Insight:

While the **Toaster department** had the **highest number of resolved calls** (99), a closer look at resolution **percentage** reveals that the **Air Conditioner department** is actually the **overall best performer**, with the **highest resolution rate of 92.2%**.

This suggests that the **Air Conditioner team** is not only effective but also consistent in resolving a high proportion of issues, making them the most efficient team overall.

**Question 5:** The satisfactory ratings level of the callers.   

Insight:

**Most customers rated their calls as either 3 or 4, with 4 receiving the highest count (159 out of 514 total ratings).** This suggests that **customers are generally satisfied** but **not overly impressed,** as the majority of scores fall just below the perfect rating of 5.

***Question 6:** How many calls did each agent handle, and how much revenue did they generate?*   

Insight:

- **Jim** handled the highest number of calls (**536**) and also achieved one of the top total purchase amounts (**₦35,560**), indicating both **efficiency and high conversion**.
- **Martha** generated the **highest total purchase amount** (**₦35,717**) from **514 calls**, showing a strong **ability to close high-value sales.**
- **Joe**, despite handling the **fewest calls (484)**, achieved a **relatively high purchase amount (₦34,358)**, which suggests **quality over quantity** in his interactions.
- **Diane**, with **501 calls and ₦33,200**, has the **lowest purchase total**, which may signal the need for coaching or support in improving conversion rates.

***Question 7:** How do agents perform across various department.*
