### Assignment: SQL Joins in a Software Company Database

#### Background

You are working with a database for a software company named "SoftwareCo". This database contains several tables that store information about employees, departments, projects, and the technologies used in these projects. Your task is to demonstrate your understanding of SQL joins by writing queries that combine data from these tables in meaningful ways.

#### Database Schema

The database, named `software_company`, consists of the following tables:

1. **employees**

| Column Name   | Type    |
|---------------|---------|
| id            | Integer |
| name          | Text    |
| department_id | Integer |
| project_id    | Integer |

2. **departments**

| Column Name | Type    |
|-------------|---------|
| id          | Integer |
| name        | Text    |

3. **projects**

| Column Name | Type    |
|-------------|---------|
| id          | Integer |
| name        | Text    |
| tech_id     | Integer |

4. **technologies**

| Column Name | Type    |
|-------------|---------|
| id          | Integer |
| name        | Text    |

#### Tasks

1. **List All Employees and Their Project Names**

   Write a query to list all employees and the names of the projects they are working on. Use a LEFT JOIN since not all employees might be assigned to a project.

2. **List All Projects and Their Technology Names**

   Write a query to list all projects along with the names of the technologies used in these projects. Use an INNER JOIN because you are only interested in projects where the technology is known.

3. **List All Departments and Their Technologies**

   This is a more complex query that requires you to use multiple joins. List all departments along with the technologies used in the projects under each department. You might need to join all four tables to achieve this. Use LEFT JOINs to ensure that departments without projects or projects without a specified technology are also included.

4. **Bonus Task: Find Employees Working on a Specific Technology**

   As a bonus, write a query to find all employees who are working on projects that use a specific technology (e.g., "React"). This will require joining multiple tables and filtering on the technology name.

#### Notes

- You are encouraged to experiment with different types of joins (INNER, LEFT, RIGHT, FULL OUTER) to see how they affect your results.
- Pay attention to how you can join tables on columns that are not primary or foreign keys, especially in the bonus task.
- There is no evaluation for this assignment, but completing the bonus task will give you extra recognition for your SQL skills.

#### Submission Guidelines

- Write your SQL queries in a text file named `SQL_Joins_Assignment.sql`.
- Comment each query with the task number and a brief description of what the query does.
- For the bonus task, include the specific technology you chose to filter by in your query.


Good luck, and have fun exploring the power of SQL joins in the context of a software company's database!
