# Key concepts of databases in MySQL. 

### Primary key

A primary key is a field (or a combination of fields) in a database table that uniquely identifies each record in that table.

Key characteristics of a primary key:

1.	Uniqueness: Each value in the primary key column must be unique. No two records can have the same primary key value.
   
2.	Non-nullability: Every record must have a value for the primary key. It cannot be null.
	
3.	Immutability: The value of a primary key should not change once it is set, as it’s used to identify the record.
  
4.	Efficiency: Primary keys are often indexed to make querying and searching for records faster.
	
For example, in a Students table, a StudentID column might serve as the primary key, where each student gets a unique ID to distinguish them from others.

**How does this differ from a secondary key?**

The main difference between a primary key and a secondary key (often referred to as a foreign key or alternate key, depending on context) lies in their role and usage within a database.

**How are primary and foreign keys related?**

Primary and foreign keys are both crucial concepts in relational databases that help maintain data integrity and establish relationships between tables.

### Real-world example of a one-to-one relationship

A one-to-one relationship in a database occurs when a single record in one table is associated with only one record in another table. A real-world example of this could be:

**Real-World Example: Passport and Citizen**

Imagine a system where each citizen can only have one passport and each passport can only be assigned to one citizen. This represents a one-to-one relationship.

### Real-world example of a one-to-many relationship

A one-to-many relationship occurs when a single record in one table is associated with multiple records in another table. Here's a real-world example:

**Real-World Example: Department and Employees**

Imagine a company where each department can have multiple employees, but each employee works in only one department. This represents a one-to-many relationship.

### Real-world example of a many-to-many relationship

A many-to-many relationship occurs when multiple records in one table are associated with multiple records in another table. A common real-world example of a many-to-many relationship is the students and courses scenario in a university system.

**Real-World Example: Students and Courses**

In a university system, each student can enrol in multiple courses, and each course can have multiple students enrolled. This represents a many-to-many relationship.

### Self-join:

A self join is a type of join where a table is joined with itself. It's useful when you need to compare rows within the same table. This is typically done by treating the same table as two different "tables" by using aliases for each instance of the table. A self join is often used to find relationships within the same set of data.

**Example:**
Consider an "Employees" table that contains information about employees and their managers. The table might have the following columns:

•	EmployeeID

•	EmployeeName

•	ManagerID (this is a foreign key that references the EmployeeID of the manager)

### Right join:

A RIGHT JOIN (or RIGHT OUTER JOIN) in SQL returns all records from the right table and the matched records from the left table. If there is no match, the result is NULL on the left side. This join is particularly useful when you want to ensure that all records from the right table are included, regardless of whether they have matching records in the left table.

### Full join:

A FULL JOIN (or FULL OUTER JOIN) in SQL returns all records when there is a match in either the left table or the right table. If there is no match, the result will contain NULL values for missing matches from either table.
In other words, it combines the results of both LEFT JOIN and RIGHT JOIN, returning all rows from both tables, with NULL where there is no match.

### Inner join:

An INNER JOIN in SQL returns only the rows where there is a match between the two tables based on the condition specified in the ON clause. If no match is found, the row is excluded from the result.

**Key Points:**

•	Only matched records are included in the result.

•	It eliminates rows from both tables that don't meet the join condition.

### Cross join:

A CROSS JOIN in SQL returns the Cartesian product of two tables, meaning it returns every possible combination of rows between the two tables. If table A has m rows and table B has n rows, a CROSS JOIN will return m * n rows. It does not require a condition to join the tables, unlike other types of joins.

**Key Points:**

•	The CROSS JOIN does not require a condition (like ON in other joins).

•	It produces a Cartesian product—each row from the first table is paired with every row from the second table.

•	The result can be quite large, especially if the tables have many rows.

### Left join:

A LEFT JOIN (also known as a LEFT OUTER JOIN) in SQL returns all rows from the left table and the matching rows from the right table. If there is no match in the right table, the result will include NULL values for the columns from the right table.

**Key Points:**

•	All rows from the left table will be included in the result, whether or not there is a match in the right table.

•	If no match exists, the result will contain NULL values for the right table's columns.



**Data Source: Just IT, Google, ChatGPT**

**Full Project work book [here.](https://drive.google.com/file/d/1g0QAXtTUazd8F3VYITU4YQgKn8HzCIps/view?usp=drive_link)**

**Click [here](https://github.com/Alamin-analyser/Designing-Database-in-MySQL) to see another MySQL Project.**




