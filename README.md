![image](https://github.com/user-attachments/assets/55c66eb5-ce90-4351-8fe4-4bdf843d3556)

# SQL: Filtering a SQL query
In this project, SQL was used to retrieve specific subsets of data from a database by applying filtering conditions with the WHERE clause. The goal was to extract meaningful information by narrowing down results based on defined criteria such as dates, user roles, activity status, or device types.

# Environments and Technologies Used.
- Google Cloud Virtual Machines.
- SQL (Structured Query Language).

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
