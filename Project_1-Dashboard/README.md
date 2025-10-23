# Excel Salary Dashboard  

<img width="1575" height="598" alt="Project_1_Dashboard_3" src="https://github.com/user-attachments/assets/59b475bb-a327-4930-bcf6-b49509ae5e81" />  

### Introduction  

This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.  

The data is from my Excel course, which provides a foundation in analyzing data using this powerful tool. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.

### Dashboard File  
My final dashboard is in [1_Salary_Dashboard.xlsx](https://github.com/user-attachments/files/23098750/1_Salary_Dashboard.xlsx).  

### Excel Skills Used  
- __📉 Charts__
- __🧮 Formulas and Functions__
- __❎ Data Validation__

### Data Jobs Dataset  

The dataset used for this project contains real-world data science job information from 2023. 
The dataset is available via my excel course,which provides a foundation for analyzing data using Excel. It includes detailed information on:  
- __👨‍💼 Job titles__
- __💰 Salaries__
- __📍 Locations__
- __🛠️ Skills__

 ### Dashboard Build  

 #### 📉 Charts  
__📊 Data Science Job Salaries - Bar Chart__  

 <img width="490" height="297" alt="Chart_Project_1" src="https://github.com/user-attachments/assets/95b98fae-8e22-45e1-9b64-9a9f72872993" />  
 
 - __🛠️ Excel Features:__ Utilized bar chart feature(with formatted salary vakues) and optimiized layout for clarity.  
 - __🎨 Design Choice:__ Horizontal bar chart for visual comparison of median salaries.
 - __📉 Data Organization:__ Sorted job titles by descending salary for improved readability.
 - __💡 Insights Gained:__ This enables quick identification of salary trends, noting that Senior roles and engineers are higher-payimg than Analst roles.

 __🗺️ Country Median Salaries - Map Chart__  
 
 <img width="522" height="267" alt="Chart_Project_Country_1" src="https://github.com/user-attachments/assets/e75da8e9-76fb-4be0-a012-1d2281831d97" />  
 
- __🛠️ Excel Features:__ Utilized Excel's map chart feature to plot median salaries glodally.
- __🎨 Design Choice:__ Color-coded map to visually differentiate salary levels across regions.
- __📊 Data Representation:__ Plotted median salary for each country with available dat.
- __👁️ Visual Enhancement:__ Improved readability and immediate understanding of geographic salary trends.
- __💡 Insights Gained:__ Enables quick grasp of global disparities and highlights high/low salary regions.

### 🧮 Formulas and Functions  

__💰 Median Salary by Job Titles__  
```DAX
=Median(
IF(
   (jobs[job_title_short]=A2)*
   (jobs[job_country]=country)*
   (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```
- __🔍 Multi-Criteria Filtering:__ Checks job title, country, schedule type, and excludes blanks salaries.
- __📊 Array Formula:__ Utilizes MEDIAN() function with nested IF() statement to analyze an array.
- __🎯 Tailored Insights:__ Provides specifics salary information for job titles, regions, and schedule types.
- __🔢 Formula Purpose:__ This formula populates the tables below, returning the median salary based on job title, country, and type.

#### 🍽️ Background Table

<img width="317" height="267" alt="Median_Salary_Project_2" src="https://github.com/user-attachments/assets/a0464dc8-00ea-47b9-bae3-948dc35eb88d" />  

#### 📉 Dashboard Implementation  

![Median_Salary_Project_Display_1](https://github.com/user-attachments/assets/55512ca7-b05f-4008-b051-130474979e96)  

#### ⏰ Count of Job Schedule type  
```DAX
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- __🔍 Unique List Generation:__ This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.
- __🔢 Formula Purpose:__ This formula populates the table below, which gives us a list of unique job schedule types.

#### 🍽️ Background Table  

![Background Table](https://github.com/user-attachments/assets/e32e49e8-7590-42cd-8525-452b3ef102c5)  

#### 📉 Dashboard Implementation 

![Dashboard Implementation](https://github.com/user-attachments/assets/4075edc3-0c49-4cef-b989-957fd71b433f)  

### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:
  - 🎯 User input is restricted to predefined, validated schedule types
  - 🚫 Incorrect or inconsistent entries are prevented
  - 👥 Overall usability of the dashboard is enhanced
    
![Project_1_Dashboard_4 png](https://github.com/user-attachments/assets/0c2369b2-26ed-43fb-8ddb-6ed7ef3b3984)


### Conclusion  

I created this dashboard to showcase insights into salary trends across various dat-related job titles. Utilizing data from my Excel course, this dashboard allows users to make informed decisions about their careerpaths. Exploring the functionalities to understand how job country and job type influence salaries.
