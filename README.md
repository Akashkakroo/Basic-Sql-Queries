# Basic-Sql-Queries

Tables:-

1/ Departments 

CREATE TABLE departments (
    id INT PRIMARY KEY,
    dept_name VARCHAR(50)
);

INSERT INTO departments (id, dept_name) VALUES
(1, 'HR'),
(2, 'Engineering'),
(3, 'Sales');


2/ Employees 

CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT,
    salary DECIMAL(10, 2),
    department_id INT,
    FOREIGN KEY (department_id) REFERENCES departments(id)
);

INSERT INTO employees (id, name, age, salary, department_id) VALUES
(1, 'Alice', 30, 50000, 1),
(2, 'Bob', 25, 45000, 2),
(3, 'Charlie', 28, 55000, 1),
(4, 'David', 35, 60000, 3),
(5, 'Eve', 29, 52000, 2);
