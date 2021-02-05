# Pewlett Hackard Analysis: Employee Database with SQL

## Project Overview
Pewlett Hackard is a large company, boasting several thousand employees, and it's been around a long time. As baby boomers begin to retire at a rapid rate, Pewlett Hackard is looking towards the future in two ways. First, it's offering a retirement package for those who meet certain criteria. Second, it's starting to think about which positions will need to be filled in the near future. The upcoming retirements, also called the "silver tsunami", will leave thousands of job openings. As an HR analyst at Pewlett Hackard, I've been tasked to perform employee research. Specifically, I've found answers to the following questions:
1. Who will be retiring in the next few years?
2. How many positions will Pewlett Hackard need to fill?

This analysis will assist Pewlett Hackard to generate a list of all employees eligible for the retirement package. The employee data I needed was only available in six .csv files, but leadership finally decided to update the company's methods and instead use SQL. Therefore, I built an employee database with SQL by applying my data modeling, engineering and analysis skills.

## Resources
- **Data Sources**: PH-Employee Database created from departments.csv, dept_emp.csv, dept_manager.csv, employees.csv, salaries.csv & titles.csv
- **Software**: PostgreSQL 11.10, Git Bash 2.29.2, Visual Studio Code 1.52.1

## Challenge Overview
Since creating the employee database and answering leadership's initial questions, the HR director has requested two additional items to help Pewlett Hackard prepare for the "silver tsunami" :
1. determine the number of retiring employees per title; and 
2. identify employees who are eligible to participate in a mentorship program.

## Challenge Results
### Deliverable 1: The Number of Retiring Employees by Title
- Using the ERD I created as a reference and my knowledge of SQL queries, I created a 'Retirement Titles' table that holds all the titles of current employees who were born between January 1, 1952 and December 31, 1955.

<img src="Images/Del 1_retirement_titles.PNG">

- Because some employees may have multiple titles in the database—for example, due to promotions— I used the `DISTINCT ON` statement to create a 'Unique Titles' table that contains the most recent title of each employee. 

<img src="Images/Del 1_unique_titles.PNG">

- Then, I used the `COUNT()` function to create a final 'Retiring Titles' table that has the number of retirement-age employees by most recent job title.

<img src="Images/Del 1_retiring_titles.PNG">

### Deliverable 2: The Employees Eligible for the Mentorship Program
- Using the ERD I created as a reference and my knowledge of SQL queries, I created a 'Mentorship Eligibility' table that holds the current employees who were born between January 1, 1965 and December 31, 1965.

<img src="Images/Del 2_mentorship_eligibility.PNG">

## Challenge Summary

Based on the "Retiring Titles' table I created, there are over 90,000 roles that will need to be filled as the "silver tsunami" begins to make its impact. Almost a third of those are Senior Engineers and close to another third are Senior Staff. Therefore, there are close to 60,000 qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees. That amount of employees is more than enough to get the mentorship program off the ground and running!

Implementing a mentorship program is a highly effective way for baby boomers to transfer their knowledge and expertise to younger employees and prepare for the silver tsunami. Some additional queries that would assist HR develop a successful mentorship program are creating employee tables filtered by title and departmeent, both for retiring employees and mid-career employees. These tables would be a huge help in making mentor and protege matches. For instance, a table of retiring Senior Engineers in Development can be matched up with a table of mid-career Engineers in Development, just like a table of retiring Senior Staff in Quality Management can be matched up with a table of mid-career Staff in Quality Management.

As baby boomers exit the workplace, millennials will make up a larger proportion of Pewlett Hackard's workforce. Retaining and developing this generation of employees will be crucial for Pewlett Hackard's successful transition through the silver tsunami as well. Since millenials value professional development training programs and opportunities to progress as leaders, creating some new tables which are filtered for this age group can help Pewlett Hackard tailor some new continuing education initiatives and training programs to this subset of employees. 

All in all, building a strong mentoring culture and expanding professional development opportunities at Pewlett Hackard will ensure it overcomes the upcoming tidal wave of turnover.
