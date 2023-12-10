# sql-challenge

In this challenge we were asked to design the tables to hold the data from provided CSV files, import the CSV files into a SQL database, and then answer questions about the data. The challenge was divided into three parts: data modeling, data engineering, and data analysis.

In the first part of the challenge, we created an entitly relationship diagram using the QUICKDBD tool. By looking at the individual provided CSV files, I chose to use title_id as the primary key in the titles dataset, emp_no as the primary key in the employees dataset and dept_no as the primary key in the departments dataset because these variables contained unique values.

In the second part of this challenge, we exported the ERD into postgres, create tables, and load in CVS into their corresponding tables. It was important to specifiy the data types as either VARCHAR(30), INT, and DATE. To avoid errors the CSV tables containing primary keys had to be loaded in first. The CSVs were loaded in order from: titles, employees, salaries, department, dept_emp, and dept_manager. 

In the final part of the challenge, we utilized the query tool to analyze the data and answer questions. 
  1. List the employee number, last name, first name, sex, and salary of each employee.
  2. List the first name, last name, and hire date for the employees who were hired in 1986.
  3. List the manager of each department along with their department number, department name, employee number, last name, and first name.
  4. List the department number for each employee along with that employee’s employee number, last name, first name, and department name.
  5. List first name, last name, and sex of each employee whose first name is Hercules and whose last name begins with the letter B.
  6. List each employee in the Sales department, including their employee number, last name, and first name.
  7. List each employee in the Sales and Development departments, including their employee number, last name, first name, and department name.
  8. List the frequency counts, in descending order, of all the employee last names (that is, how many employees share each last name).
  
Through the use of QuickDBD, Stack Overflow, Github, and class notes, I was able to find the code for:
- ALTER TABLE "table_1" ADD CONSTRAINT "fk_table_1_var_1" FOREIGN KEY("var_1") REFERENCES "table 2" ("var_2");
- WHERE hire_date >= '<start date>' AND hire_date <= '<end date>';
- COUNT(last_name) AS "last_name_frequency" ORDER BY "last_name_frequency" DESC;
