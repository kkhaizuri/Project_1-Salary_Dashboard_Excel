# Excel Salary Dashboard

<img width="1597" height="714" alt="1  Dashboard" src="https://github.com/user-attachments/assets/653265e3-65d2-4b60-be77-707d073d5e20" />

## Introduction
This data jobs salary dashboard was developed to help job seekers explore salary trends for various roles and assess whether they are being fairly compensated.

The dataset comes from my Excel course, which focuses on building a strong foundation in data analysis using Excel. It includes detailed information on job titles, salaries, locations, and key skills, all of which are visualized in this dashboard.

## Dashboard File
My final dashboard is in [Salary_Dashboard.xlsx](https://github.com/user-attachments/files/25032671/Salary_Dashboard.xlsx)

## Excel Skills Used
The following Excel skills were utilized for analysis:  
- Charts
- Formulas and Functions
- Data Validation

## Data Jobs Dataset
The dataset used for this project contains real-world data science job information from 2023. It includes detailed information on:

- Job titles
- Salaries
- Locations
- Skills

Data Jobs Dataset: [data_jobs_salary.xlsx](https://github.com/user-attachments/files/25894510/data_jobs_salary.xlsx)


## Dashboard Build
### Charts
Data Science Job Salaries - Bar Chart  

<img width="641" height="509" alt="2  Charts" src="https://github.com/user-attachments/assets/ea0cd7a3-d235-4315-9a48-e3dc7db4a608" />  

- Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- Design Choice: Horizontal bar chart for visual comparison of median salaries.
- Data Organization: Sorted job titles by descending salary for improved readability.
- Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

## Country Median Salaries - Map Chart  

<img width="588" height="394" alt="3  Map" src="https://github.com/user-attachments/assets/a53d6eb4-855d-4182-ae4b-1775389f0049" />  

- Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
- Design Choice: Color-coded map to visually differentiate salary levels across regions.
- Data Representation: Plotted median salary for each country with available data.
- Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
- Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.

  ## Formulas and Functions

  ### Median Salary by Job Titles
```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.
- Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.
- Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.
- Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.

Background Table  

<img width="414" height="315" alt="4  Jobtitle_mediansalary" src="https://github.com/user-attachments/assets/0b6b0014-0f22-4e63-a088-a1fb57fee929" />

Dashboard Implementation

<img width="597" height="670" alt="5  Dashboard_implement" src="https://github.com/user-attachments/assets/7d886902-3b7b-479b-b0f4-bef6b4b4e9c4" />

Count of Job Schedule Type

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- Unique List Generation: This Excel formula below employs the `FILTER()` function to exclude entries containing "and: or commas, and omit zero values.
- Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.

Background Table

<img width="328" height="171" alt="6  Work_type" src="https://github.com/user-attachments/assets/642d012b-1dab-4554-b8e5-612d9fccccd6" />

Dashboard Implement

<img width="509" height="659" alt="7  Dashboard_implement_2" src="https://github.com/user-attachments/assets/da52f9e0-2094-4b2e-8dbe-5cc4b8c369ca" />

## Data Validation

Filtered List

- Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:
  - User input is restricted to predefined, validated schedule types
  - Incorrect or inconsistent entries are prevented
  - Overall usability of the dashboard is enhanced

 <img width="331" height="280" alt="8  Data_validation" src="https://github.com/user-attachments/assets/0d4b4e39-ec4d-4e98-b60c-14f47e5a96da" />

 ## Conclusion
 
I created this dashboard to showcase insights into salary trends across various data-related job titles. By using data from my Excel course, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.




