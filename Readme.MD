# Power BI Projects  
This repository contains a collection of Power BI projects that showcase various data analysis workflows, including data extraction, transformation, and loading (ETL) using Power Query, as well as data cleaning, reporting, and dashboard creation. Each project is structured with a dedicated folder containing relevant files, datasets, and reports.

## Repository Structure  
Below is an overview of the folder structure:  

📂 -Power-BI-Projects
│
├── 📁HR_Data_Analytics
│ ├── Dashboard.jpg
│ ├── Dataset.csv
│ ├── HR_Analytics.pbix
│ └── Documentation.md

---

## Project 1: HR Data Analytics - Employee Attrition Dashboard  

**Objective:**  
Analyze employee attrition factors and provide actionable insights to reduce turnover.

**Dataset:**  
`HR_Analytics.csv`  
Contains employee data with columns such as EmpID, Age, Attrition, Department, MonthlyIncome, etc.

**Key Steps:**  

- **Data Cleaning:** Removed empty columns and handled missing values.  
- **Data Transformation using Power Query:**  
  - Added a new column for attrition count and created DAX measures for attrition rate:  
    ```DAX
    AttritionCount = IF([Attrition] = "Yes", 1, 0)  
    Attrition Rate = (SUM([AttritionCount])) / (SUM([EmployeeCount]))
    ```
- **Dashboard:**  
  - Visualized attrition trends, employee demographics, and key performance indicators.  
  - Included slicers for filtering by department and gender.  

**Report File:**  
Report file [HR_Analytics(.pbix)](https://github.com/Ak-AlphaData/Power-BI-Projects/tree/main/HR-Analytics)  

---

## Projects Overview  
Each folder contains a Power BI (.pbix) report, the data sources, and any documentation related to the project. Below are the highlights of what each project covers:  

### Data Importing & Loading  
- Extracted data from multiple sources such as CSV, Excel, and SQL databases.  
- Leveraged Power Query for data transformation.  

### Data Cleaning & Transformation  
- Cleaned datasets (handled missing values, duplicates, and data inconsistencies).  
- Performed data type corrections and column transformations.  
- Merged and appended datasets as needed for analysis.  

### Reporting & Dashboarding  
- Built dynamic dashboards and reports with interactive visuals.  
- Used DAX (Data Analysis Expressions) to create calculated measures and columns.  
- Implemented slicers, filters, and drill-throughs for better insights.  

### Performance Optimization  
- Applied best practices for report optimization (e.g., reducing model size and improving load times).  

---

## Prerequisites  
- Power BI Desktop (latest version)  
- Excel / CSV Reader (for datasets)  
- SQL Server / Database Access (if working with SQL queries in specific projects)  

---

## Technologies Used  
- **Power BI Desktop**  
- **Power Query**  
- **DAX (Data Analysis Expressions)**  
- **SQL / Excel / CSV** for data storage and manipulation  

