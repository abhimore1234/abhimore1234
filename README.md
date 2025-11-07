
# 👋 Hi, I'm Abhishek More 

**Data Science & Full Stack Developer**<br><br>
🌐 Explore My Portfolio : [abhimore.netlify.app](https://abhimore.netlify.app/) <br>
A living canvas of my projects, capabilities, and innovations.

---



## 👨‍💻 About Me

I specialize in turning complex data into actionable insights. With a strong foundation in data analysis, machine learning, and statistical modeling, I help organizations unlock valuable patterns and drive informed decisions.

- **Core Skills:** Data analysis, machine learning, statistical modeling
- **Technologies:** Python, R, SQL, Apache Spark, Hadoop
- **Specializations:** Predictive analytics, deep learning, scalable data pipelines
- **Interests:** AI-driven solutions for business optimization and fraud detection
- **Continuous Learning:** Cloud-based AI, MLOps, efficient model deployment


---

## 🚀 What I Do

- Always curious, always learning—exploring the endless possibilities in data science and full stack development.
- Experiment with new tools, frameworks, and approaches to keep my skills sharp.
- Enjoy breaking down complex topics into easy-to-understand concepts.
- Believe in the power of data to make a positive impact, one project at a time.

---

## 🌱 Motto

> “Data doesn’t lie, but interpretation is everything.”

> “Continuous learning is the key to growth.”

---

## 📫 Connect with Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abhishek-more-363bb62b8)

---

_Simplicity is the ultimate sophistication._

## 👨‍💻 About Me

I specialize in turning complex data into actionable insights. With a strong foundation in data analysis, machine learning, and statistical modeling, I help organizations unlock valuable patterns and drive informed decisions.

- **Core Skills:** Data analysis, machine learning, statistical modeling
- **Technologies:** Python, R, SQL, Apache Spark, Hadoop
- **Specializations:** Predictive analytics, deep learning, scalable data pipelines
- **Interests:** AI-driven solutions for business optimization and fraud detection
- **Continuous Learning:** Cloud-based AI, MLOps, efficient model deployment

---

## 🚀 What I Do

- Always curious, always learning—exploring the endless possibilities in data science and full stack development.
- Experiment with new tools, frameworks, and approaches to keep my skills sharp.
- Enjoy breaking down complex topics into easy-to-understand concepts.
- Believe in the power of data to make a positive impact, one project at a time.

---

## 🌱 Motto

> “Data doesn’t lie, but interpretation is everything.”

> “Continuous learning is the key to growth.”

---

## 📫 Connect with Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abhishek-more-363bb62b8)

---

_Simplicity is the ultimate sophistication._ 

1. Table
•	Definition: A table stores structured data in rows and columns.
•	Use: Core data storage unit in relational databases.
✅ Example
CREATE TABLE employees ( emp_id INT PRIMARY KEY, name VARCHAR(100), salary DECIMAL(10,2) ); 
📤 Sample Output
After inserting:
INSERT INTO employees VALUES (101, 'Abhishek More', 60000.00); 
2. View
•	Definition: A virtual table based on a SELECT query.
•	Use: Simplifies complex queries, restricts access, formats data.
✅ Example
CREATE VIEW high_earners AS SELECT name, salary FROM employees WHERE salary > 50000; 
📤 Sample Output
SELECT * FROM high_earners; 
	
	
3. Index
•	Definition: A performance object that speeds up data retrieval.
•	Use: Optimizes queries on large datasets.
✅ Example
CREATE INDEX idx_name ON employees(name); 
📤 Output
No visible result—performance improves internally. You can verify with:
SHOW INDEX FROM employees; 

4. Sequence (Oracle only)
•	Definition: Generates unique numbers, often for primary keys.
•	Use: Auto-incrementing IDs.
5. Synonym (Oracle only)
•	Definition: Alias for another object.
•	Use: Simplifies access, hides actual object name.
✅ 6. Constraints
		
•  PRIMARY KEY: Uniquely identifies each row and prevents duplicates or NULLs.
NOT NULL: Ensures that a column must always have a value.
UNIQUE: Guarantees that all values in a column are distinct.
CHECK: Validates data against a condition to enforce logical rules.
DEFAULT: Automatically assigns a predefined value when none is provided.
FOREIGN KEY: Maintains referential integrity by linking to another table’s primary key.

		
________________________________________
🧱 Step 1: Create Table with Constraints
CREATE TABLE Students (
    student_id INT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    age INT CHECK (age >= 16 AND age <= 30),
    gender VARCHAR(10) CHECK (gender IN ('Male', 'Female', 'Other')),
    city VARCHAR(50) DEFAULT 'Unknown'
);
________________________________________
🧩 Step 2: Insert Sample Values
INSERT INTO Students (student_id, name, age, gender, city) VALUES
(101, 'Abhishek More', 22, 'Male', 'Indapur'),
(102, 'Sneha Patil', 20, 'Female', 'Pune'),
(103, 'Ravi Deshmukh', 19, 'Male', 'Mumbai'),
(104, 'Priya Kulkarni', 21, 'Female', 'Nagpur'),
(105, 'Amit Joshi', 17, 'Male', 'Solapur'),
(106, 'Neha Shinde', 23, 'Female', 'Pune'),
(107, 'Kiran Pawar', 18, 'Male', 'Nashik'),
(108, 'Meera Naik', 25, 'Female', 'Kolhapur'),
(109, 'Omkar Kale', 30, 'Male', 'Satara'),
(110, 'Tanvi Gokhale', 28, 'Female', 'Pune');
________________________________________
✅ Step 3: 12 SQL DML Queries
SELECT * FROM Students;

SELECT * FROM Students
WHERE city IN ('Pune', 'Mumbai');

SELECT * FROM Students
WHERE name LIKE 'A%';

UPDATE Students
SET city = 'Aurangabad'
WHERE student_id = 105;

DELETE FROM Students
WHERE age < 18;

SELECT city, COUNT(*) AS total_students
FROM Students
GROUP BY city;

SELECT UPPER(name) AS uppercase_name, city
FROM Students;

SELECT * FROM Students
WHERE age BETWEEN 18 AND 25;

SELECT * FROM Students
ORDER BY age DESC;

SELECT * FROM Students WHERE city = 'Pune'
UNION
SELECT * FROM Students WHERE city = 'Nagpur';

SELECT * FROM Students
WHERE name LIKE '%e';
UPDATE Students SET city = CASE student_id WHEN 1 THEN 'Pune' WHEN 2 THEN 'Mumbai' WHEN 3 THEN 'Delhi' END WHERE student_id IN (1, 2, 3); 

CREATE VIEW Pune_Students AS
SELECT student_id, name, age, gender
FROM Students
WHERE city = 'Pune';

SELECT * FROM Pune_Students;

CREATE INDEX idx_city ON Students(city);

SELECT * FROM Students WHERE city = 'Pune';

1.	Select all students
SELECT * FROM Students;
2.	Select students from Pune or Mumbai
SELECT * FROM Students
WHERE city IN ('Pune', 'Mumbai');
3.	Select students with name starting with 'A'
SELECT * FROM Students
WHERE name LIKE 'A%';
4.	Update city of a student
UPDATE Students
SET city = 'Aurangabad'
WHERE student_id = 105;
5.	Delete students younger than 18
DELETE FROM Students
WHERE age < 18;
6.	Count students by city
SELECT city, COUNT(*) AS total_students
FROM Students
GROUP BY city;
7.	Display names in uppercase
SELECT UPPER(name) AS uppercase_name, city
FROM Students;
8.	Select students with age between 18 and 25
SELECT * FROM Students
WHERE age BETWEEN 18 AND 25;
9.	Sort students by age descending
SELECT * FROM Students
ORDER BY age DESC;
11.	Use UNION to combine students from Pune and Nagpur
SELECT * FROM Students WHERE city = 'Pune'
UNION
SELECT * FROM Students WHERE city = 'Nagpur';
12.	Select students whose name ends with 'e'
SELECT * FROM Students
WHERE name LIKE '%e';


 13 .Update city using CASE expression
UPDATE Students SET city = CASE student_id WHEN 1 THEN 'Pune' WHEN 2 THEN 'Mumbai' WHEN 3 THEN 'Delhi' END WHERE student_id IN (1, 2, 3); 
1.	

________________________________________


###. Cursors: (All types: Implicit, Explicit, Cursor FOR Loop, Parameterized Cursor) Write a PL/SQL block of code using parameterized Cursor that will merge the data available in the newly created table N_Roll_Call with the data available in the table O_Roll_Call. If the data in the first table already exists in the second table then that data should be skipped. Note: Instructor will frame the problem statement for writing PL/SQL block using all types of Cursors in line with above statement.
Setp 1: -- N_Roll_Call (new data)
CREATE TABLE N_Roll_Call (
    student_id INT PRIMARY KEY,
    student_name VARCHAR2(100),
    birth_date DATE
);
Step 2: -- Insert some records
INSERT INTO O_Roll_Call VALUES (1, 'Shivanna', TO_DATE('1995-08-15','YYYY-MM-DD'));
INSERT INTO O_Roll_Call VALUES (3, 'Cheluva', TO_DATE('1990-12-10','YYYY-MM-DD'));

Step 3: -- O_Roll_Call (old data)
CREATE TABLE O_Roll_Call (
    student_id INT PRIMARY KEY,
    student_name VARCHAR2(100),
    birth_date DATE
);

Step 4: -- Insert some records
INSERT INTO N_Roll_Call VALUES (1, 'Shivanna', TO_DATE('1995-08-15','YYYY-MM-DD'));    -- Already in old table
INSERT INTO N_Roll_Call VALUES (2, 'Bhadramma', TO_DATE('1998-03-22','YYYY-MM-DD'));  -- Unique
INSERT INTO N_Roll_Call VALUES (3, 'Cheluva', TO_DATE('1990-12-10','YYYY-MM-DD'));    -- Already in old table
INSERT INTO N_Roll_Call VALUES (4, 'Devendra', TO_DATE('2000-05-18','YYYY-MM-DD'));   -- Unique

-- Check initial state
SELECT * FROM O_Roll_Call;
SELECT * FROM N_Roll_Call;
🧠 What Are Cursors in PL/SQL?
In PL/SQL, cursors are control structures that allow row-by-row processing of query results. They are essential when a query returns multiple rows and you need to handle each row individually.
Implicit Cursor
Automatically created by Oracle for single-row queries like INSERT, UPDATE, or SELECT INTO.
Explicit Cursor
Manually declared for queries returning multiple rows. Requires OPEN, FETCH, and CLOSE.

🔄 What is ROLLBACK in SQL/PLSQL?
ROLLBACK is a command used to undo all changes made during the current transaction before a COMMIT is issued.
COMMIT; statement at the end, which ensures that all inserted records from N_Roll_Call into O_Roll_Call are permanently saved in the database.












