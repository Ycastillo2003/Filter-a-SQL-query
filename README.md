![image](https://github.com/user-attachments/assets/55c66eb5-ce90-4351-8fe4-4bdf843d3556)

# SQL: Filtering an SQL query
In this project, SQL was used to retrieve specific subsets of data from a database by applying filtering conditions with the WHERE clause. The goal was to extract meaningful information by narrowing down results based on defined criteria such as dates, user roles, activity status, or device types.


# Environments and Technologies Used.
- Google Cloud Virtual Machines.
- SQL (Structured Query Language).

# Operating Systems Used </h2>
- Linux.

# Actions and observations.

 In this scenario, we need to get specific information about employees, their machines, and the departments they’re in. Our team needs this data to perform various tasks, such as running updates, posting a privacy notice in certain departments, and sending an alert to an employee with an issue on a machine.

![image](https://github.com/user-attachments/assets/24fcef1e-b1d8-4e04-808a-9d0ebd0722db)

- using SELECT device_id, operating_system FROM machines;.

![image](https://github.com/user-attachments/assets/34f6ca3d-8c79-4bb5-aee6-dd0dce74d9bd)

- Receiving over 200 rows of data.

![image](https://github.com/user-attachments/assets/582e24ad-5ef7-4de0-adc3-40262e3255a8)

- Using the WHERE clause and making  operating_system = OS 2 to further narrow our search.

![image](https://github.com/user-attachments/assets/d30286b5-b449-4fe5-9ed1-bdbf99200183)

- Now our search has been reduced from 200 rows to 80, and we have filtered for OS 2 using the WHERE clause.

 In this task, we need to retrieve a list of all the employees in the Finance and Sales departments to obtain their office numbers. A notice about handling confidential financial information will be posted to these offices.

![image](https://github.com/user-attachments/assets/5e9b6dba-4864-4fa1-96e7-dac8e59c40ae)

- We will start with the finance department, as you can see in the picture above, with the SELECT * FROM employees WHERE department = 'Finance'; command to only get finance department data from the employees tables.

![image](https://github.com/user-attachments/assets/178588d4-1f91-4153-b970-9f27a3a8bd7d)

- Now we can see all the info pertaining to the employees in the finance department.

![image](https://github.com/user-attachments/assets/8e61c067-7fd3-468e-b7ad-663cf4083e45)

- Now we are going to do the same thing, but for the sales department.

![image](https://github.com/user-attachments/assets/5721bc4b-a9fb-4a8f-bbab-a84fc4217172)

- Now we have the info for employees for the sales department.

Our team recently discovered that there are issues with machines in the South building. In this task, we need to obtain certain employee and computer information.

A machine in 'South-109' has an issue. WE need to determine which employee uses that computer so you can send them an alert.

![image](https://github.com/user-attachments/assets/4290e83a-4d8b-4deb-a803-af4558873a02)

- After using the WHERE clause to filter the Office Column of the employees table, we see that Jlasnky in the finance department, employee_id 1010, is who we have to notify.


Next, our team has determined that there is an issue with all the machines in the South building. Offices in the organization are named with the building name, a hyphen, and the office number in that building (for example, 'South-109').

WE Modify the query we used in the previous step so that it returns information on all the employees in the 'South' building.

![image](https://github.com/user-attachments/assets/1c1650fd-6ac4-4c33-aee9-27cd46e79d6c)

- Using comparison operator LIKE 'south%' to filter for entries that have zero or more characters after south

![image](https://github.com/user-attachments/assets/a7d1e65b-e840-4743-8193-24e51abf2920)

- Now we have an entire overview of the south building.

In this next task, we need to investigate a recent security incident. To do this, you need to gather information about login attempts made after a certain date.

![image](https://github.com/user-attachments/assets/4c2a9719-b09d-4cba-a32c-404f6bba75df)

- The operator > lets us filter for dates greater than. In this example, we need dates greater than 22-05-09.

![image](https://github.com/user-attachments/assets/93953087-7aea-4cf7-82a2-c0efd4f528d0)

- Now the data we get back from the log_in_attempts TABLE are all after the 22-05-09 date since we used the operator >.
  
![image](https://github.com/user-attachments/assets/95ef6592-0bbd-448e-bd0a-5931c42d18af)![image](https://github.com/user-attachments/assets/1d1a7c59-2d37-43b0-b31e-6e5edc2738cd)

- Now to have more context investigating this security incident so using >= we make it so the data we get back from the query  are the events that happened on 22-05-09 and after. 

     We figured out that the accident happened before 22-05-11 so to get results that happened between 22-05-09 and 22-05-11.

![image](https://github.com/user-attachments/assets/b30c6b85-28bf-4893-b2fa-4b673283229f)![image](https://github.com/user-attachments/assets/62235f0a-03ef-4faa-acf2-ccc9bb339b8f)

- Using THE operators BETWEEN & AND, we filtered our query search to show events happening between 2 certain dates. Now we also know the incident happened after work hours, so we can filter the time to only show data from after work hours.

![image](https://github.com/user-attachments/assets/fb556d6c-18ce-41ec-9599-c053ead364fa)![image](https://github.com/user-attachments/assets/da018278-2aa4-4798-83d2-bc8fd9ff8351)

- With this query, we narrow it down to login attempts between 2022-05-09 and 2022-05-11 and only the ones that happened after work hours Now that our search has been narrowed, it is easer to analyze the data and locate when and where the incident happen.


    Now we need to investigate a suspicious event that occurred on '2022-05-09'. We want to retrieve all login attempts that occurred on 2022-05-09 and the day before 2022-05-08.


 ![image](https://github.com/user-attachments/assets/5855f5ab-9225-4e71-b089-ef854d608827)![image](https://github.com/user-attachments/assets/e9e6a03c-c644-4fbe-a562-c177aa1e1b9a)


- With this query, we can get login attempts that happened on those specific dates. Using the logical operator OR, it retrieves data that either happened on one date or the other.


 Our team is updating employee machines, and you need to obtain the information about employees in the 'Marketing' department who are located in all offices in the East building (such as 'East-170' or 'East-320').


![image](https://github.com/user-attachments/assets/13cfa63c-6c3a-408e-aca9-14810f20237c) ![image](https://github.com/user-attachments/assets/1674b5d4-45c4-4850-a99e-f6fdd5903b02)


- This query selects all employees who work in the Marketing department and whose office is located in any location starting with "East" (like East-170, East-320, etc.). The LIKE 'East%' pattern matches any office name beginning with "East".


Our team needs to make one more update. This update was already made to employee computers in the Information Technology department. The team needs information about employees who are not in that department.l

![image](https://github.com/user-attachments/assets/dc2ffc8f-3c6d-4b35-8bd2-ed91792b0683)![image](https://github.com/user-attachments/assets/23c0b683-dd92-4f53-b022-0ca3845f1271)

- This query selects all employees whose department is not Information Technology. The NOT operator reverses the condition, so it excludes anyone in the IT department. Now we know every device that needs an update.
























   In this lab, we practiced retrieving and analyzing data from a database using SQL filtering techniques. WE used the WHERE clause along with comparison and logical operators (such as =, >, <, AND, OR, LIKE, NOT, and BETWEEN) to narrow down query results based on specific conditions.
