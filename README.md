# 🧠 Mental Health & Productivity Analysis Dashboard

An end-to-end data analysis and visualization project exploring the relationship between **mental health, stress, and productivity** in the workplace.  
This project covers **data cleaning, exploratory data analysis (EDA)**, and an **interactive Power BI dashboard** to uncover actionable insights.

---

## 📊 Project Overview

This project analyzes how factors such as **remote work, stress level, work-life balance, and company support** influence employee productivity and mental health outcomes.

**Tech Stack:**
- 🐍 Python (Pandas, NumPy, Seaborn, Matplotlib) – Data Cleaning & EDA  
- 📊 Power BI – Dashboard creation & KPI visualization  
- 🔢 DAX – Custom calculated measures  

---

## 🧩 Dataset

A dataset of **500 employees** with the following key columns:

| Category | Example Columns |
|-----------|-----------------|
| Demographics | `Age`, `Gender`, `Country`, `Education_Level` |
| Work Info | `Employment_Type`, `Industry`, `Department`, `Years_Experience` |
| Mental Health | `Stress_Level`, `Has_Mental_Health_Issue`, `Treatment_Sought` |
| Productivity | `Self_Reported_Productivity`, `Burnout_Symptoms`, `Sleep_Hours` |
| Support & Environment | `Manager_Support_Level`, `Company_Support`, `Work_Life_Balance` |

📁 **File:** `mental_health_productivity_dataset.csv`

---

## 🔍 Data Analysis & EDA

Performed:
- Handling missing values & outliers  
- Encoding categorical variables  
- Visualizing relationships between stress, productivity, and work conditions  

**Key Insights:**
- Higher **stress levels** are linked to lower **productivity** and **job satisfaction**  
- Employees with **remote work** show better **work-life balance**  
- Strong **manager & peer support** reduces burnout  

🧰 **Example Visuals:**
- Correlation Heatmap  
- Stress vs Productivity Scatterplot  
- Treatment by Age & Gender Distribution  

---

## 📈 Power BI Dashboard

The Power BI dashboard visualizes:

| Insight | Visual | Fields |
|----------|---------|--------|
| Gender Distribution | Bar Chart | Gender, Count(Employee_ID) |
| Treatment by Age Group | Column Chart | Age_Group, % Treated |
| Remote vs On-site | Donut Chart | Remote_Work, Treatment Rate % |
| Stress Interference by Department | Clustered Bar | Department, Avg(Work_Interfere) |
| Stress vs Productivity | Scatter Plot | Stress_Level, Self_Reported_Productivity |
| Work-Life Balance vs Remote | Box Plot | Remote_Work, Work_Life_Balance |
| KPIs | Cards | Avg Productivity, Avg Stress, % Treated |

**Interactive Features:**
- Slicers for Country, Gender, and Remote Work  
- Dynamic KPI Cards  
- Calming blue/green color theme  

---

## 🧮 DAX Measures

```DAX
Treatment Rate % = 
DIVIDE(SUM('data'[Treatment_Sought]), COUNT('data'[Employee_ID]), 0)

Avg Productivity = AVERAGE('data'[Self_Reported_Productivity])

Avg Stress = AVERAGE('data'[Stress_Level])
