# Assignment-7 Full-stack (DBMS & PostgreSQL)

### Assignment Description

In this assignment, you will work with PostgreSQL, a powerful open-source relational database management system. Your task involves creating 02 tables based on the provided sample data and then writing and executing queries to perform various database operations such as creating, reading, updating etc. Additionally, you will explore concepts like LIMIT and OFFSET, JOIN operations, GROUP BY, aggregation and LIKE.

## Instructions:

### Database Setup:

-  Ensure PostgreSQL is installed on your system if not already installed.
-  Create a fresh database titled **"company_db"** or any other suitable name.

## Table Creation:

Create an **employees table** with the following fields:

-  `employee_id` (Primary Key): Integer, unique identifier for employees.
-  `employee_name`: String, representing the employee's name.
-  `age`: Integer, indicating the employee's age.
-  `email`: String, storing the employee's email address.
-  `department_id`: Integer, referencing the department the employee belongs to.
-  `salary`: Numeric, indicating the employee's salary.
-  `status`: String, storing the employee's employment status.

Create a **departments table** with the following fields:

-  `department_id` (Primary Key): Integer, unique identifier for departments.
-  `department_name`: String, indicating the department's name.

## Sample Data

-  Use the following sample data to insert into the tables:

### Departments Table:

| department_id | department_name |
| ------------- | --------------- |
| 1             | Engineering     |
| 2             | Marketing       |
| 3             | Finance         |

### Employees Table:

| employee_id | employee_name | age | email                      | department_id | salary | status |
| ----------- | ------------- | --- | -------------------------- | ------------- | ------ | ------ |
| 1           | Alice         | 30  | mailto:alice@example.com   | 1             | 60000  | NULL   |
| 2           | Bob           | 35  | mailto:bob@example.net     | 2             | 65000  | NULL   |
| 3           | Charlie       | 28  | mailto:charlie@google.com  | 1             | 55000  | NULL   |
| 4           | David         | 33  | mailto:david@yahoo.com     | 2             | 62000  | NULL   |
| 5           | Eve           | 31  | mailto:eve@example.net     | 3             | 58000  | NULL   |
| 6           | Frank         | 29  | mailto:frank@example.com   | 1             | 59000  | NULL   |
| 7           | Grace         | 34  | mailto:grace@google.com    | 2             | 63000  | NULL   |
| 8           | Henry         | 32  | mailto:henry@yahoo.com     | 3             | 57000  | NULL   |
| 9           | Ivy           | 27  | mailto:ivy@gmail.com       | 1             | 56000  | NULL   |
| 10          | Jack          | 36  | mailto:jack@example.net    | 2             | 64000  | NULL   |
| 11          | Karen         | 29  | mailto:karen@gmail.com     | 3             | 60000  | NULL   |
| 12          | Liam          | 33  | mailto:liam@gmail.com      | 1             | 59000  | NULL   |
| 13          | Mia           | 31  | mailto:mia@yahoo.com       | 2             | 62000  | NULL   |
| 14          | Nora          | 28  | mailto:nora@yahoo.com      | 3             | 57000  | NULL   |
| 15          | Oliver        | 35  | mailto:oliver@example.net  | 1             | 61000  | NULL   |
| 16          | Penelope      | 30  | mailto:penelope@google.com | 2             | 63000  | NULL   |
| 17          | Quinn         | 32  | mailto:quinn@google.com    | 3             | 59000  | NULL   |
| 18          | Rachel        | 27  | mailto:rachel@gmail.com    | 1             | 55000  | NULL   |
| 19          | Sam           | 34  | mailto:sam@example.net     | 2             | 64000  | NULL   |
| 20          | Taylor        | 31  | mailto:taylor@yahoo.com    | 3             | 58000  | NULL   |

## You will get the code to insert above table rows in insertData.sql file.

## Execute SQL queries to fulfill the task below:

### Query 1:

Retrieve all employees with a salary greater than 60000

**Sample Result Data:**

| employee_id | employee_name | age | email                      | department_id | salary | status |
| ----------- | ------------- | --- | -------------------------- | ------------- | ------ | ------ |
| 4           | David         | 33  | mailto:david@yahoo.com     | 2             | 62000  |        |
| 7           | Grace         | 34  | mailto:grace@google.com    | 2             | 63000  |        |
| 10          | Jack          | 36  | mailto:jack@example.net    | 2             | 64000  |        |
| 13          | Mia           | 31  | mailto:mia@yahoo.com       | 2             | 62000  |        |
| 15          | Oliver        | 35  | mailto:oliver@example.net  | 1             | 61000  |        |
| 16          | Penelope      | 30  | mailto:penelope@google.com | 2             | 63000  |        |
| 19          | Sam           | 34  | mailto:sam@example.net     | 2             | 64000  |        |
| 2           | Bob           | 35  | mailto:bob@example.net     | 2             | 65000  |        |

### Query 2:

Retrieve the names of employees using a limit of 2, starting from the 3rd employee.

**Sample Result Data:**

employee_name

---

Charlie

---

David

---

### Query 3:

Calculate and display the average age of all employees.

**Sample Result Data:**

average_age

---

31.6

---

### Query 4:

Retrieve the names of employees whose email addresses contain '[example.com](http://example.com/)', '[example.net](http://example.net/)', or '[google.com](http://google.com/)'.

**Sample Result Data:**

employee_name

---

Alice

---

Bob

---

Charlie

---

Eve

---

Frank

---

Grace

---

Jack

---

Oliver

---

Penelope

---

Quinn

---

Sam

---

### Query 5:

Retrieve the names of all employees who belong to the department titled 'Engineering'.

**Sample Result Data:**

employee_name

---

Alice

---

Charlie

---

Frank

---

Ivy

---

Liam

---

Oliver

---

Rachel

---

### Query 6:

Update the status of the employee with the highest salary to 'Promoted'

Note: You can use a subquery to identify the employee with the highest salary,

### Query 7:

Retrieve the department name and the average salary of employees in each department:

**Sample Result Data**

| department_name | avg                |
| --------------- | ------------------ |
| Engineering     | 57857.142857142857 |
| Marketing       | 63285.714285714286 |
| Finance         | 58166.666666666667 |

Prepare the SQL code for table creation, sample data insertion, and the seven queries in a .sql file. Include comments explaining each query's purpose and functionality. **Save your document as "postgreSQL_assignment.sql" or any other appropriate name. don't add multiple file keep all the 7 queries in a single file**

# **Private repository link**

## **Questions (Answer 10 Questions):**

1. **What is PostgreSQL?**
2. **What is the purpose of a database schema in PostgreSQL?**
3. **Explain the primary key and foreign key concepts.**
4. **What is the difference between the VARCHAR and CHAR data types?**
5. **Explain the purpose of the WHERE clause in a SELECT statement.**
6. **What are the LIMIT and OFFSET clauses used for?**
7. **How can you perform data modification using UPDATE statements?**
8. **What is the significance of the JOIN operation, and how does it work in PostgreSQL?**
9. **Explain the GROUP BY clause and its role in aggregation operations.**
10.   **How can you calculate aggregate functions like COUNT, SUM, and AVG in PostgreSQL?**
11.   **What is the purpose of an index in PostgreSQL, and how does it optimize query performance?**
12.   **Explain the concept of a PostgreSQL view and how it differs from a table.**

**Provide detailed answers to these questions in your assignment GitHub repository's README file as part of your assignment submission.**


### **Private Repo:** [Click Here ](https://classroom.github.com/a/OfHRl2JS)<!-- _blank -->



### **Submission:**

- Submit only the GitHub repository link containg your solution file

### **Deadline:**

-  60 marks: March 5, 2024 11.59 AM
-  50 marks: March 6, 2024 11.59 PM
-  30 marks: After March 6, 2024 11.59 PM

**Important Note: *Attendance in this assignment is obligatory for all participants. As a follow-up, there will be two further assignments involving Prisma and PostgreSQL backends, specifically tailored for individuals with aspirations of becoming proficient full-stack developers. Approach this task with a thorough perspective and a commitment to achieving excellence. Wishing you the best of luck in your endeavors.***
