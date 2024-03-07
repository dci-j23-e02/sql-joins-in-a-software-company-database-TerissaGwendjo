1.) List All Employees and Their Project Names:

SELECT e.name AS name, p.name AS name
FROM employees e
LEFT JOIN projects p ON e.id = p.id;

![Alt Text] (jetbrains://idea/navigate/reference?project=sql-joins-in-a-software-company-database-Terissa&path=Screenshot from 2024-03-07 12-04-48.png)

// We are selecting data from the employees table (e) and the projects table (p).
We're using a LEFT JOIN to ensure that all employees are listed, even if they are not assigned to a project.
The ON clause specifies the condition for joining the two tables, linking the project_id from the employees table to the id of the projects table.
We're selecting the name column from both tables and using aliases (e and p) to differentiate between the two tables.

2.) List All Projects and Their Technology Names
SELECT p.name AS name, t.name AS name
FROM projects p
INNER JOIN technologies t ON p.tech_id = t.id;

// We are selecting data from the projects table (p) and the technologies table (t).
We're using an INNER JOIN because we want to retrieve only projects where the technology is known and present in the technologies table.
The ON clause specifies the condition for joining the two tables, linking the tech_id from the projects table to the id of the technologies table.
We're selecting the name column from both tables and using aliases (p and t) to differentiate between the two tables.

3.) List All Departments and Their Technologies:
SELECT d.name AS name, t.name AS name
FROM departments d
LEFT JOIN projects p ON d.id = p.id
LEFT JOIN technologies t ON p.tech_id = t.id;

//We are selecting data from the departments table (d), the projects table (pr), and the technologies table (t).
We're using LEFT JOIN to ensure that departments without projects or projects without a specified technology are also included.
We perform two LEFT JOINs: one between the departments and projects tables and another between the projects and technologies tables.
The ON clauses specify the conditions for joining the tables based on their respective foreign keys (department_id and tech_id).
We're selecting the name column from both the departments and technologies tables and using aliases to differentiate between the tables.

4.) Bonus Task: Find Employees Working on a Specific Technology:
SELECT e.name AS name, p.name AS name
FROM employees e
LEFT JOIN projects p ON e.id = p.id
LEFT JOIN technologies t ON p.tech_id = t.id
WHERE t.name = 'Linac';

//We are selecting data from the employees table (e), the projects table (p), and the technologies table (t).
We're using LEFT JOINs to ensure that all employees are included, even if they are not assigned to a project, and to include projects even if their technology is not specified.
We specify the condition for joining the technologies table based on the tech_id in the projects table.
We filter the results using a WHERE clause to include only projects where the technology name is 'Java'.
We're selecting the name column from the employees and projects tables and using aliases to differentiate between the tables.
