# HR-Analytics-Report: MeriSkill Internship Project
# Introduction
MeriSkill Internship provides a rich and valuable learning experience in uncovering insights from raw dataset. The internship creates the opportunity to gain invaluable hands-on experience in various facets of data analysis and interpretation. This includes tasks such as data collection, analysis, visualization, and drawing meaningful insights. This project involves analyzing a historic human resource dataset with the aim of understanding an organization staff structure and tracking staff performance. This project gives an insight into the employee and salary structure of an organization.
The dataset consists of 1471 records and 35 features stored in a  CSV File. The dataset comprises of numerical and categorical columns. Some of the features are monthly income, monthly rate, overtime, percent salary hike, performance rating, relationship satisfaction, standard hours, total working years, age, attrition, department, education, gender, education field etc. 
# Objectives
- Perform data wrangling
- Data Modelling
- Analyze the dataset
- Create visuals and dashboard to identify trends and make informed decision.
- Provide recommendations
# Tools used
- Excel - Data Source and Inspection
- Power BI - Creating Reports
- Power Query - Data Cleaning and Data Analysis
- DAX - Data Analysis Expressions
# Data Cleaning/Preparation
The following tasks were performed in the data wrangling stage
- Data loading and inspection
- Renaming of columns
- Handling missing and null values
- Eliminate redundant data
- Validating columns data types
# Data Modelling and Visualization
Data Modelling was not created in this project because the dataset is stored in a single table. Creating data modelling is necessary when multiple tables are involved as it improves data quality and performance.

![Data modelling view](https://github.com/DannyRukks/HR-Analytics-Report/assets/97890440/f5474a36-82f7-4eb4-8aa9-9f5ba44f412b)

In order to extract insights and patterns from the dataset, The measures below were created and metrics as displayed below:
```
Total Number of Employees = COUNTROWS('hr data')
```
```
Attrition Count = COUNTROWS(FILTER(
    'hr data',
    'hr data'[Attrition] = "Yes"))
```
```
Active Employees = [Total Number of Employees] - [Attrition Count]
```
```
Average Employee Performance = AVERAGE('hr data'[PerformanceRating])
```
```
Average Salary = AVERAGE('hr data'[MonthlyIncome])
```
```
Employee Average Age = AVERAGE('hr data'[Age])
```
```
Attrition Rate = DIVIDE(
    [Attrition Count], [Total Number of Employees])
```
```
Employee Average Age = AVERAGE('hr data'[Age])
```
```
Total Income = SUM('hr data'[MonthlyIncome])
```
Separate dashboards were created to extract insight from the employees and salary information. The employees dashboard enable us to extract significant information about the employees working in the organization. The dashboard is displayed below:

![Employee View](https://github.com/DannyRukks/HR-Analytics-Report/assets/97890440/93cce697-e68d-42eb-b7d1-522c680dbeda)

In a similar faction, the income dashboard enable us to draw useful insight about the staff salary of employees working in the organization and make informed decisions. The dashboard is displayed below:

![Income view](https://github.com/DannyRukks/HR-Analytics-Report/assets/97890440/131b8b24-cdf5-443f-abfd-2bafffdac68a)

# Insights
### Here are some useful insights from the employees view
- There are 1470 employees with 1233 being the active employees with an attrition rate of 16.12%.
- The average age of an employee is 37 years.
- The overall average performance of the employees is 3.15
- 60% of the staff workforce are females while 40% of the staff workforce are males. Majority of the staff are married. 45.78% of the staff are married, 31.97% of the staff are single and 22.24% of the staff are divorced.
- Majority of the staff have 0-5 years experience. Few staff have more than 20+ years of experience
- Research and development department has the highest number of employees with a staff size of 828.
  
### Insights from the income view are presented below
- The total income of the employee is approximately $9.56 million with an average income of $6.5 thousand.
- A manage earned the highest salary which is around $20.00 thousand
- The top 3 education field with the highest income are life sciences, medical and marketing
- Average income of an employee with less than 20 years of experience is approximately $2.7 thousand. This income increases with an increase in the years of experience.
- The top 5 job roles with the highest income are managers, research directors, health care representative, manufacturing director and sales executives.
# Recommendations
- The organization should set up policies that will improve employee retention especially employees that have spent more than ten years working with the company.
- The organization should adopt policies to bridge the gap between the male and female employees
- Measures should be put in place to increase the job satisfaction level of the employees
- The company should revisit the working hours of the employees and make it more flexible for better performance.
- Incentives and a rewarding system should be put in place to encourage hard working staff 


