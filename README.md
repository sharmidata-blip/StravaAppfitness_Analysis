📊 Fitbit/Strava Data Analysis Project
📌 Project Overview

This project analyzes daily activity, sleep, and health metrics of participants using Fitbit data.
We explored patterns in steps, calories burned, distance covered, heart rate, and sleep duration.
The goal is to extract actionable insights into participants’ activity and lifestyle.

🛠️ Tools & Libraries

SQL (MySQL Workbench) – for data cleaning and preprocessing

Python (Pandas, NumPy) – for data analysis

Matplotlib, Seaborn, Plotly – for visualizations

Power BI – for interactive dashboards

📂 Dataset

dailyActivity_merged.csv

sleepDay_merged.csv

hourlyCalories_merged.csv

hourlySteps_merged.csv

📌 Data includes participant ID, activity date, steps, calories, distance, and sleep information.

🔑 Sample SQL Queries
-- 1. Average steps per participant
SELECT Id, AVG(TotalSteps) AS AvgSteps
FROM daily_activity
GROUP BY Id;

-- 2. Average calories burned by weekday
SELECT DAYNAME(ActivityDate) AS Weekday, AVG(Calories) AS AvgCalories
FROM daily_activity
GROUP BY Weekday;

-- 3. Average sedentary minutes per participant
SELECT Id, AVG(SedentaryMinutes) AS AvgSedentary
FROM daily_activity
GROUP BY Id;

-- 4. Sleep duration in hours
SELECT Id, AVG(TotalMinutesAsleep)/60 AS AvgSleepHrs
FROM sleep_day
GROUP BY Id;

📈 Data Analysis & Visualizations
🔹 Activity Patterns

Average steps by weekday 

<img width="1009" height="548" alt="Avg  Steps Taken Weekly" src="https://github.com/user-attachments/assets/4804b46f-ccce-475c-b3dc-06e3a778d0eb" />

Trend of calories burned vs. steps

<img width="737" height="551" alt="stepsvscalories burned" src="https://github.com/user-attachments/assets/9a5cbe85-08fa-4441-9680-844b24123006" />

Daily distance covered 
<img width="716" height="537" alt="avgdistance" src="https://github.com/user-attachments/assets/34427c10-5736-4090-a44b-e93916166ea8" />


🔹 Sleep Analysis

Average sleep duration 

<img width="1064" height="472" alt="avgsleephrs" src="https://github.com/user-attachments/assets/010b703f-0b18-468b-a9d7-7850dd727a36" />

Time in bed vs. minutes asleep 

<img width="905" height="487" alt="Time in bed vs  minutes asleep" src="https://github.com/user-attachments/assets/3832cca2-f646-4fcf-8f71-4abd0b60d1b8" />


🔹 Lifestyle Insights

Sedentary minutes vs. active minutes

<img width="740" height="499" alt="Avg  Sedentary Minutes" src="https://github.com/user-attachments/assets/c49e928b-1625-4a8f-98ca-812fe3e142cc" />

Heart rate vs. calories burned


💡 Insights

Participants are most active on weekdays, with steps peaking mid-week.

Sedentary behavior is higher on weekends.

More distance covered correlates with higher calories burned.

Average sleep hours were below the recommended 8 hrs.

🎯 Recommendations

Encourage participants to walk at least 8,000+ steps daily.

Reduce sedentary time with short activity breaks every 2 hours.

Improve sleep consistency to enhance recovery and performance.

Personalized fitness goals can be set based on activity-tracking.

📑 Project Deliverables

✅ SQL Queries & Cleaning (MySQL Workbench)

✅ Python Notebook (Pandas, Visualizations)

✅ Power BI Dashboard (Interactive insights)

✅ PDF Report (Summary with screenshots)

📥 Repository Structure
📁 Fitbit-Analysis
 ┣ 📂 data
 ┃ ┣ dailyActivity_merged.csv
 ┃ ┣ sleepDay_merged.csv
 ┣ 📂 notebooks
 ┃ ┣ fitbit_analysis.ipynb
 ┣ 📂 visuals
 ┃ ┣ avg_steps_heatmap.png
 ┃ ┣ calories_steps_trend.png
 ┃ ┣ distance_trend.png
 ┃ ┣ sleep_duration.png
 ┃ ┣ sleep_kpi.png
 ┃ ┣ sedentary_active.png
 ┃ ┣ hr_calories.png
 ┣ 📂 reports
 ┃ ┣ Fitbit_Project_Report.pdf
 ┣ README.md

✨ Full Notebook: [StravaFitness.ipynb - Colab.pdf](https://github.com/user-attachments/files/22440329/StravaFitness.ipynb.-.Colab.pdf)


📊 Dashboard PDF: [wellness dashboard.pdf](https://github.com/user-attachments/files/22440333/wellness.dashboard.pdf)

✨ Full Notebook: View Here

📊 Dashboard PDF: Download Here
