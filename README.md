# HR Data - Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/ed94899e-141c-4f56-8b41-7214d81a17bf/a61edab19a6b041c9e44?experience=power-bi

## Problem Statement

The HR department of the organization lacks clear visibility into key employee metrics, making it difficult to monitor workforce trends, identify attrition patterns, and make data-driven decisions. Currently, there is no centralized dashboard or standardized set of KPIs to track employee headcount, attrition rates, age demographics, or job satisfaction levels.

Due to the absence of such performance indicators, HR managers face challenges in:

1)Understanding overall workforce composition and employee turnover.

2)Identifying departments or demographics with high attrition.

3)Evaluating job satisfaction and its impact on retention.

4)Planning effective hiring and retention strategies based on workforce insights.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.

- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.

- Step 3: The Column headers were considered as data we converted that row into the headers using the Power BI (Use First Row As Headers) Function.

- Step 4: There were some typos in the department column we corrected them using the Power BI replance values option.

- Step 5: We removed unwanted spaces from the columns Using the Trim Function. 

- Step 6: Using the Column Distribution , Column Profile, Column Quality we checked for the quality of the columns and the data looks good now. 

- Step 7: Added Conditional column name "Attrition Count" using the column "Attrition"

 Additional Column Function Snip, 

![Conditional Column](https://raw.githubusercontent.com/rawdyt/HR-Data/main/Conditional%20column%20for%20Attrition.jpg)


![Conditional Column](https://raw.githubusercontent.com/rawdyt/HR-Data/main/Attrition%20Count%20Column.jpg)


- Step 7 : The same like above way we have added one another conditional column which is "Sort Age"


- Step 8: We have created 2 measured whcih are required 
  for the KPI creation
  

 1)Active employee
  
   Used below DAX query:

     Active Employee = SUM('HR data'[Employee Count])- SUM('HR  
     data'[Attrition Count])

  2)Attrition rate

   Used below DAX query:
    
     Attrition Rate = Attriotion Rate = SUM('HR data'[Attrition 
     Count])/SUM('HR data'[Employee Count])


### Dashboard Creation

- Step 1: Added 4 KPI's one top 
         1) Overall Employee Count
         2) Attrition
         3) Attrition Rate
         4) Active Employee
         5) Average Age

- Step 2: Donut Chart to show Departmet Wise Attrition

- Step 3: Staked Column Chart to show Number of Emoployees by age 
  group and Gender.

- Step 4: Matrix to Job satisfaction as per the job role.

- Step 5: Bar chart to show the Education Wise Attrition.

- Step 6: 4 different Donut chart to show Attrition by different 
  age group

## Insights

- HR data data summary:

   1)Overall Employee Count : 1470

   2)Attrition Count : 237

   3)Attrition Rate : 16.12%
   
   4)Active Employees : 1233

   5)Average Age : 37

  6)R&D department has the high attrition rate than other  
  department

  And HR department has lowest attrition rate.

  7)Most of the Employees are from the age band 25-34 or 35-44 
   and the male count is high than the Female count in this  
  group. 

   8)Life Science is the education filed from which we have 
  highes attrition rate which is 89 out of 237.

  9)25-34 is the age group where we have high attrition rate
  which is 112 out of 237. 

### Snip of the Dashboard

![HR DATA DASHBORD](https://raw.githubusercontent.com/rawdyt/HR-Data/main/HR%20Data%20Dashboard.jpg)

 ### I have attached the file which is consisting of all the  SQL queries used in to verfy our dashboard data.

[📄 SQL Queries](https://github.com/rawdyt/HR-Data/blob/main/HR%20DATA%20SQL%20QUERIES.txt) 

### I have also created a Excel Dashboard for the same data.

![Excel Dashboard Snip](https://raw.githubusercontent.com/rawdyt/HR-Data/main/HR%20DATA%20EXCEL%20DASHBOARD.jpg)

### Excel Dashboard Link : https://1drv.ms/x/c/e0d2e4ac1b1db67c/EY9OquOr0SFKnxXtpxk_tscB95Mpz-nDm24QgckGhiP31A?e=xkabxH
