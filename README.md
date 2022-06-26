# Pewlett-Hackard-Analysis
## Overview of the analysis: 
In order to finish the assignments from managers and provide a report and help prepare Bobby’s manager for the “silver tsunami” as many current employees reach retirement age, in this challenge, first of all, we need to generate a table including the number of retiring employees by title, then create the table of the employees eligible for the mentorship program. Lastly, we will utilize the tables to provide two analysis deliverables and a written report.

## Results 
- Join the employees table with Titles table on the primary key and filter on the birth_date column to retrieve the employees who were born between 1952 and 1955. Then order by the employ number. We reached to the first point table, below:

![retirement_titles](https://user-images.githubusercontent.com/103073631/170626765-0fca0024-f463-4eb3-a92d-083d2d90a4bc.png)

- From the first table, we noted that there are duplicates entrries for some people because they have switched titles over the years. So Use the ```DISTINCT ON``` statement to retrieve the first occurrence of the employee number for each set of rows, to get below table, as unique table:

![unique_titles](https://user-images.githubusercontent.com/103073631/170627231-5ef144ba-1ef7-4843-b6c3-a166e3a2b7dd.png)

- Then table with retrieve the number of employees by their most recent job title who are about to retire, as below, with column count and titles:

![retiring_titles](https://user-images.githubusercontent.com/103073631/170627427-180b7ab1-186e-40ca-9080-6f0b55443bc2.png)

- Last, Join the Employees and the Department Employee tables on the primary key, and also join the Employees and the Titles tables on the primary key. The Employees Eligible for the Mentorship Program table was generated as below:

![mentorship_eligibilty](https://user-images.githubusercontent.com/103073631/170627630-31b07278-5595-4512-be78-370c6cc1931d.png)

***The major findings about the retiring employees***

1. The employees who are about to retire, the top two tiles are all in ***"Senior"*** titles;
2. The employees eligible for the Mentorship Program table shows that most of titles are clarrified as ***"Senior"*** too; 
3. From the retiring titles table, we get total 72,458 employees are about to retire, and the mentioship eligibilty table, there are 1549 qualified to mentor. It is about 47 retiring emplyees per mentor.
4. The Retiring titles table also shows two major titles are about to retire, one is for engineer and the other is staff. Senior engineers, Engineers and assistant engineers are totally equal to 36,291 (25,916+9,285+1,090); and the total for staffs is 32,562 (24,926+7,636).

## Summary
Provide high-level responses to the following questions, then provide two additional queries or tables that may provide more insight into the upcoming "silver tsunami."
- How many roles will need to be filled as the "silver tsunami" begins to make an impact?
  From Retiring titles table, we know that the list below who are about to retire
    - 25,916 Senior Engineer
    - 24,926 Senior Staff
    - 9,285 Engineer
    - 7,636 Staff
    - 3,603 Technique Leader
    - 1,090 Assistant Engineer
    - 2 Manager
    
    Total will be ```72,458``` employees are about to retire, which means positions will be opening after these employees retired and in preparation for these openings, potential candidates have to be filled when these employees retired.
    
    ![image](https://user-images.githubusercontent.com/103073631/170628755-3b9f7adb-be45-45b9-9863-5f1c9323efa3.png) 

    
- Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?
  
  From the last table ```mentoship_eligibilty```, there are only 1,549 qualified, retirement-ready employees in the departments to mentor the next generation, comparing with protential opening positions, there are not enough employees to be mentors.
  
  ![image](https://user-images.githubusercontent.com/103073631/170632796-7d47cf9a-4cd4-4092-a548-7db9b1c8c207.png)
