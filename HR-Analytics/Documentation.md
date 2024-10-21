# HR Data Analytics: Employee Attrition Dashboard in Power BI

## Objective
The objective of this project is to analyze the factors driving employee attrition and provide actionable insights to reduce turnover. This interactive dashboard allows HR teams to explore key workforce metrics and monitor employee satisfaction trends.

---

## Project Overview
This project demonstrates the creation of an **Interactive HR dashboard** in Power BI to analyze employee attrition data. It involves **data preparation, transformation, and visualization** to extract insights that assist in strategic decision-making and improving retention strategies.

---

## Features
- **Interactive Dashboard:** Uses filters and slicers to allow dynamic exploration of data.
- **Comprehensive KPIs:** Includes Attrition Rate, Total Employees, and Monthly Income metrics.
- **Visualizations:** Bar charts, pie charts, KPIs, and matrix tables provide a clear overview of data.
- **Easy-to-Use Interface:** Designed to be accessible and intuitive for non-technical users.

---

## Key Steps
1. **Data Gathering:**
   - Imported the **CSV dataset** into Power BI and cleaned it using **Power Query Editor**.

2. **Data Cleaning:**
   - Removed empty columns, handled missing values, and standardized column names.
   - Detected **data type** of every column using the auto-detect data type function in Power Query Editor.
   - Replaced values in the column with appropriate values by substituting underscores with hyphens in the Business Travel columns.

3. **Data Processing:**
   - Added a new column, **"AttritionCount"**, using conditional logic:
     ```DAX
     AttritionCount = IF([Attrition] = "Yes", 1, 0)
     ```
   - Created a **DAX measure** to calculate the attrition rate:
     ```DAX
     Attrition Rate = (SUM([AttritionCount]))/(SUM([EmployeeCount]))
     ```

4. **Visualization Creation:**
   - Developed visualizations such as **bar charts, pie charts, and KPIs**.
   - Integrated **slicers** for filtering by department and gender.

5. **Insights Extraction:**
   - Identified key trends in attrition across **departments, job roles, and age groups**.

---

## Skills Utilized
- Data Analysis using Power BI
- Data Visualization
- Statistical Analysis
- HR Analytics

---

## Dataset Description
The dataset contains detailed employee data, including demographic information, job roles, and satisfaction metrics. Below are the **key columns** used:

| **Column Name**           | **Description**                                         |
|---------------------------|---------------------------------------------------------|
| EmpID                     | Unique identifier for each employee.                    |
| Age                       | Age of the employee.                                    |
| AgeGroup                  | Age group of the employee (e.g., 25-34).                |
| Attrition                 | Indicates whether the employee left the company.        |
| BusinessTravel            | Frequency of business travel.                           |
| DailyRate                 | Daily rate of employee pay.                             |
| Department                | Department where the employee works.                    |
| DistanceFromHome          | Distance between the employee’s home and workplace.     |
| Education                 | Education level of the employee (1-5 scale).            |
| EducationField            | Field of study of the employee.                         |
| EmployeeCount             | Total number of employees in the dataset.               |
| EnvironmentSatisfaction   | Satisfaction with the work environment (1-4 scale).     |
| JobInvolvement            | Employee's job involvement (1-4 scale).                 |
| JobRole                   | Job role of the employee.                               |
| JobSatisfaction           | Satisfaction with the job (1-4 scale).                  |
| MaritalStatus             | Marital status of the employee.                         |
| MonthlyIncome             | Employee’s monthly income.                              |
| SalarySlab                | Salary category of the employee.                        |
| OverTime                  | Whether the employee works overtime.                    |
| PerformanceRating         | Employee performance rating (1-4 scale).                |
| TotalWorkingYears         | Total years of work experience.                         |
| WorkLifeBalance           | Employee's work-life balance rating (1-4 scale).        |
| YearsAtCompany            | Number of years with the current employer.              |
| YearsInCurrentRole        | Number of years in the current role.                    |
| YearsWithCurrManager      | Number of years with the current manager.               |
| Attrition count           | Total employees who left during a specified period.     |

---

## Technologies Used
- **Power BI:** For data cleaning, transformation, and dashboard creation.
- **DAX (Data Analysis Expressions):** For creating measures and KPIs.
- **Power Query Editor:** For data preprocessing and cleaning.

---

## Dashboard Preview
![Dashboard Screenshot](https://github.com/Ak-AlphaData/Power-BI-Projects/blob/main/HR-Analytics/Dashboard.jpg)

---

## Metrics Visualized
- **Attrition Rate:** Comparison by gender and department.
- **Employee Demographics:** Breakdown by age group, gender, and education field.
- **Departmental Insights:** Attrition trends across different departments.
- **Satisfaction Metrics:** Analysis of job satisfaction and work-life balance.
- **Performance Metrics:** Insights into performance ratings and salary increases.

---

## Insights from Dashboard
1. **Total Employee Count:** The organization currently employs **1,473 individuals**.
2. **Total Attrition:** A total of **237 employees** have left the organization, indicating a noticeable level of turnover.
3. **Attrition Rate:** The attrition rate is calculated at approximately **16.1%**. **140 males** and **79 females** exited, indicating higher attrition among men, suggesting a moderate level of employee turnover that may require further analysis to understand underlying causes.
4. **Average Salary:** The average salary of employees in the organization is around **$65,000**, indicating competitive compensation but warranting a review based on industry standards.
5. **Average Tenure:** Employees have an average tenure of **7** years at the company, suggesting that many employees have stayed for several years, although some may be leaving after a relatively short period.
6. **Attrition by Education:** The highest attrition rate is among employees with a **Life Sciences** education, at **38%**. This indicates potential issues related to engagement or job satisfaction in this educational group.
7. **Attrition by Age:** The age group of **26-35** years shows the highest attrition count at **116** employees, suggesting that younger employees may be seeking opportunities elsewhere.
8. **Attrition by Job Role:** The **Research and Development** department has the highest attrition rate, with a notable **13.8%** percentage of employees leaving, indicating possible dissatisfaction or burnout in this role.
9. **Attrition by Salary:** Employees with salaries in the slab **up to $5K** monthly experience a higher attrition rate, suggesting that competitive compensation is a factor in employee retention.
10. **Attrition by Years at Company:** Employees with **1-3 years** of service show a higher turnover rate, possibly indicating challenges in early employee integration and satisfaction.
11. **Job Satisfaction Based on Gender:** Female employees report lower job satisfaction compared to male employees, which may be worth exploring further to understand the contributing factors.
12. **Departmental Attrition:** HR, Sales, and Research departments exhibit significant attrition rates, particularly:
    - **HR Department:** Lower attrition might indicate dissatisfaction with job roles or management practices.
    - **Sales Department:** Moderate attrition, necessitating immediate retention strategies.
    - **Research Department:** Higher attrition rates suggest potential areas for improving job satisfaction and engagement.

---

## Recommendations
1. **Tailored HR Strategies:** Customize initiatives to boost engagement and retention, focusing on younger employees and females.
2. **Attrition Management:** Strategically address attrition rates in high-turnover departments.
3. **Competitive Salary Review:** Regularly adjust salary structures for competitiveness in high attrition roles.
4. **Targeted Recruitment:** Recruit based on educational backgrounds for roles like Research and Development.
5. **Employee Engagement Initiatives:** Enhance communication, recognition, and development opportunities in high-turnover departments.
6. **Career Development Programs:** Provide training and mentorship for employees in their early years.
7. **Work-Life Balance Initiatives:** Promote flexible arrangements to improve satisfaction, especially in high-pressure roles.
8. **Onboarding and Integration:** Strengthen onboarding processes with mentorship for new hires.

---

## Conclusion
This project demonstrates the power of data analytics in identifying key workforce challenges and informing HR strategies. The insights from the dashboard can help organizations improve employee retention by addressing areas with high attrition rates and focusing on enhancing employee satisfaction.
