# 📊 HR Analytics Dashboard | Power BI

An interactive Power BI dashboard that analyzes workforce data for **400 employees** across **8 departments** and **5 Indian cities**. It tracks headcount, hiring, attrition, exit reasons, performance, salary, and education, so HR teams can see where and why people leave.

## 🖼️ Dashboard Preview

[HR Analytics Dashboard]
 

## 🎯 Objective
Help HR answer key questions:
- How many employees are active vs. exited, and what is the attrition rate?
- Which departments and locations lose the most employees?
- Why are employees resigning?
- Does performance rating relate to attrition?
- How does hiring vary across the year?
- What does the workforce look like by department, location, and education?

## 📁 Dataset
| Item | Details |
|---|---|
| File | `data/HR.xlsx` (sheet: `Employee_Data`) |
| Records | 400 employees |
| Columns | 18 |
| Key fields | Emp_ID, Gender, DOB, Education, Joining_Date, Department, Job_Title, Location, Annual_Salary_INR, Performance_Rating, Status, Exit_Date, Exit_Reason, Avg_Monthly_OT_Hrs, Leaves_Taken_Yearly, Training_Hours_Yearly, Tenure_Months |

*The dataset is synthetic and used for learning purposes.*

## 🧩 Dashboard Components

**Filters (slicers):** Gender, Department, Year, Location, Status

**KPI cards**
| KPI | Value |
|---|---|
| Average Salary | ₹1.06M |
| Average Performance | 3.05 / 5 |
| Total Employees | 400 |
| Active Employees | 306 |
| Total Exits | 94 |

**Visuals**
- **Quarterly Hiring Trend:** area chart of joinings per quarter
- **Attrition Rate % by Performance Rating:** column chart
- **Reason for Exit:** pie chart
- **Employees by Department:** bar chart
- **Location-wise Employees:** donut chart
- **Employee Education & Department:** stacked bar chart

## 🔍 Key Insights
- **Attrition rate is 23.5%.** 94 of 400 employees have resigned.
- **Finance has the highest attrition (~34.5%)**, followed by IT/Technical (~27.9%) and R&D (~26.7%). Operations (~16.7%) and Customer Support (~17.3%) retain best.
- **Attrition peaks at performance rating 3 (0.30)**, so average performers are the most likely to leave. Ratings 4 and 5 sit near 0.19-0.21.
- **Personal Reasons are the top exit reason (22%)**. Relocation, Health Issues, and Performance Issue follow at roughly 15-16% each, with Career Change and Better Opportunity close behind.
- **Hiring was strongest in Q1 (110) and weakest in Q2 (87)**, then recovered in Q3 (104) and Q4 (99).
- **Operations is the largest department (60 employees)**, and Supply Chain the smallest (40).
- **Workforce is evenly spread across locations:** Mumbai 22%, Bangalore 21%, Delhi 19%, Pune 19%, Hyderabad 18%.
- **Pune has the highest location attrition (~30%).**
- **Employees who resigned had a shorter average tenure** (~34 months vs. ~59 months for active staff).

## 💡 Recommendations
- Investigate why Finance and IT/Technical lose more people, for example through compensation benchmarking and stay interviews.
- Create development paths for mid-performers (rating 3), who show the highest attrition.
- Look into Pune's higher attrition and the factors behind early exits (under ~3 years of tenure).
- Address the top exit reasons with flexible work and wellness support.

## 🛠️ Tools & Techniques
- **Power BI Desktop**: dashboard design and interactivity
- **Power Query**: data cleaning and transformation
- **DAX**: calculated measures
- **Data Modeling**: date and attribute analysis

## 🧮 Sample DAX Measures
```DAX
Total Employees = COUNTROWS(Employee_Data)

Total Exit = CALCULATE([Total Employees], Employee_Data[Status] = "Resigned")

Total Active Employee = CALCULATE([Total Employees], Employee_Data[Status] = "Active")

Attrition Rate % = DIVIDE([Total Exit], [Total Employees], 0)

Avg Salary = AVERAGE(Employee_Data[Annual_Salary_INR])

Avg Performance = AVERAGE(Employee_Data[Performance_Rating])
```

## 🚀 How to Use
1. Download `HR_Analytics_Dashboard.pbix`
2. Open it in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
3. Use the slicers at the top to filter by gender, department, year, location, and status

## 📂 Repository Structure
```
HR-Analytics-Dashboard/
├── HR_Analytics_Dashboard.pbix
├── data/
│   └── HR.xlsx
├── screenshots/
│   └── dashboard_overview.png
└── README.md
```

## 👤 Author
Akash Kumar
[LinkedIn]( https://www.linkedin.com/in/akash-kumar-7b442a309/) | [Email](rudraakash8773@gamil.com)
