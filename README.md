
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
## 1 🧱 Step 1: Create Table with Constraints

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
##Here’s a complete SQL script that creates two tables—`student` and `department`—inserts sample data, and demonstrates all five types of joins with clear examples.

---

## 2 🧾 **Step-by-Step SQL Script**

### 🔹 Step 1: Create `student` Table
```sql
CREATE TABLE student (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    dept_id INT
);
```

### 🔹 Step 2: Create `department` Table
```sql
CREATE TABLE department (
    dept_id INT PRIMARY KEY,
    age INT,
    dept_name VARCHAR(100)
);
```

### 🔹 Step 3: Insert Sample Data

#### Students
```sql
INSERT INTO student VALUES (1, 'Alice', 101);
INSERT INTO student VALUES (2, 'Bob', 102);
INSERT INTO student VALUES (3, 'Charlie', NULL);
INSERT INTO student VALUES (4, 'Daisy', 104);
```

#### Departments
```sql
INSERT INTO department VALUES (101, 40, 'Physics');
INSERT INTO department VALUES (102, 35, 'Chemistry');
INSERT INTO department VALUES (103, 45, 'Mathematics');
```

---

## 🔍 **Join Queries**

### 1️⃣ **INNER JOIN** – Students with matching departments
```sql
SELECT student.name, department.dept_name
FROM student
INNER JOIN department
ON student.dept_id = department.dept_id;
```

### 2️⃣ **LEFT JOIN** – All students, even if department is missing
```sql
SELECT student.name, department.dept_name
FROM student
LEFT JOIN department
ON student.dept_id = department.dept_id;
```

### 3️⃣ **RIGHT JOIN** – All departments, even if no students
```sql
SELECT student.name, department.dept_name
FROM student
RIGHT JOIN department
ON student.dept_id = department.dept_id;
```

### 4️⃣ **FULL OUTER JOIN** – All students and departments (MySQL simulation using `UNION`)
```sql
SELECT student.name, department.dept_name
FROM student
LEFT JOIN department ON student.dept_id = department.dept_id
UNION
SELECT student.name, department.dept_name
FROM student
RIGHT JOIN department ON student.dept_id = department.dept_id;
```

### 5️⃣ **CROSS JOIN** – Every possible student–department combination
```sql
SELECT student.name, department.dept_name
FROM student
CROSS JOIN department;
```
### view 
CREATE VIEW view_inner_join AS
SELECT student.name AS student_name, department.dept_name AS department_name
FROM student
INNER JOIN department ON student.dept_id = department.dept_id;

SELECT * FROM view_inner_join;

---

________________________________________


## . Cursors: (All types: Implicit, Explicit, Cursor FOR Loop, Parameterized Cursor) Write a PL/SQL block of code using parameterized Cursor that will merge the data available in the newly created table N_Roll_Call with the data available in the table O_Roll_Call. If the data in the first table already exists in the second table then that data should be skipped. Note: Instructor will frame the problem statement for writing PL/SQL block using all types of Cursors in line with above statement.

-- Step 1: Create O_Roll_Call first

CREATE TABLE O_Roll_Call (
    student_id INT PRIMARY KEY,
    student_name VARCHAR2(100),
    address VARCHAR2(255)
);

-- Step 2: Insert old records

INSERT INTO O_Roll_Call VALUES (1, 'Shivanna', '123 Green Street');
INSERT INTO O_Roll_Call VALUES (3, 'Cheluva', '456 Blue Avenue');

-- Step 3: Create N_Roll_Call

CREATE TABLE N_Roll_Call (
    student_id INT PRIMARY KEY,
    student_name VARCHAR2(100),
    address VARCHAR2(255)
);

-- Step 4: Insert new records

INSERT INTO N_Roll_Call VALUES (1, 'Shivanna', '123 Green Street');
INSERT INTO N_Roll_Call VALUES (2, 'Bhadramma', '789 Yellow Blvd');
INSERT INTO N_Roll_Call VALUES (3, 'Cheluva', '456 Blue Avenue');
INSERT INTO N_Roll_Call VALUES (4, 'Devendra', '101 Red Road');

-- Step 5: Check initial state

SELECT * FROM O_Roll_Call;
SELECT * FROM N_Roll_Call;

-- Step 6: Merge using Parameterized Cursor

DECLARE
    -- Cursor to check if student exists in O_Roll_Call
    CURSOR check_student(p_id INT) IS
        SELECT student_id FROM O_Roll_Call WHERE student_id = p_id;

    -- Cursor to loop through new students
    CURSOR new_students IS
        SELECT student_id, student_name, address FROM N_Roll_Call;

    v_dummy O_Roll_Call.student_id%TYPE;
BEGIN
    FOR rec IN new_students LOOP
        OPEN check_student(rec.student_id);
        FETCH check_student INTO v_dummy;

        IF check_student%NOTFOUND THEN
            INSERT INTO O_Roll_Call (student_id, student_name, address)
            VALUES (rec.student_id, rec.student_name, rec.address);
        END IF;

        CLOSE check_student;
    END LOOP;

    COMMIT;

    DBMS_OUTPUT.PUT_LINE('✅ Merge complete. New students added to O_Roll_Call.');
END;
/

-- Step 7: Final check after merge

SELECT * FROM O_Roll_Call;


🧠 What Are Cursors in PL/SQL?
In PL/SQL, cursors are control structures that allow row-by-row processing of query results. They are essential when a query returns multiple rows and you need to handle each row individually.
Implicit Cursor
Automatically created by Oracle for single-row queries like INSERT, UPDATE, or SELECT INTO.
Explicit Cursor
Manually declared for queries returning multiple rows. Requires OPEN, FETCH, and CLOSE.

🔄 What is ROLLBACK in SQL/PLSQL?
ROLLBACK is a command used to undo all changes made during the current transaction before a COMMIT is issued.
COMMIT; statement at the end, which ensures that all inserted records from N_Roll_Call into O_Roll_Call are permanently saved in the database.


## Problem statement: 3. MongoDB Queries: 
Design and Develop MongoDB Queries using CRUD operations. (Use CRUD 
operations, SAVE method, 
logical operators etc.). 
1. Mongosh
   
3. Show dbs(default)
   
1.create collection

db.createCollection(“c_name”); 

2.show collection 

show Collections; 

3.data insert one 

db.c_name.insertOne({//data}) 
db.c_name.insertOne({name:”abc”, age:21, city:”xyz”}); 

4.data insert many 

db.c_name.insertMany([ {}, {} ,{}, {} ]); 
db.c_name.insertMany([{name:”abc”, age:2}, {name;”xyz”, age:4}]); 

5.see the data 

db.c_name.find(); 
db.student.find(); 
db.student.find().limit(3); 
[limit(3)--- show only 3 documents  
Find()----show all the documents] 

6.greater than  

db.student.find ({age:  {$ gt:21}}); 

7.less than  

db.student.find ({age:  {$ lt:21}}); 

8.less than or equal to  

db.student.find({age: {$ lte 21}}); 

9.greater than or equal to

db.student.find({age: {$ gte 21}}); 

10.match any value inside the given list 

db.student.find({age: {$ in: [20,21,22 ]}}); 

11.finding data 

db.c_name.findOne({name: “abc”}); 

12.update or add one data 

db.student.updateOne({name: “abc”}, {$set: {email: “abc@gmail.com”}}); 

13. update or add many data
14.  
db.student.updateMany({age: {$gt: 19}, {$set: {city: “pune”}}});

14.delete one  

db.student.deleteOne ({age: 5}); 

15.delete many 

db.student.deleteMany({age: 20}); 

16.logical operator and  

db.collection.find({ 
$and: [ 
{ age: { $gt: 25 } }, 
{ status: "active" } 
] 
})


## connectivity
### # mysql -u root -p

### # show database;

### # CREATE DATABASE collage;

### # USE collage;

### # CREATE TABLE student (
### #   id INT AUTO_INCREMENT PRIMARY KEY,
### #    name VARCHAR(100),
### #    age INT,
### #    city VARCHAR(100)
### # );

### # INSERT INTO student (name, age, city) VALUES
### # ('John', 21, 'Delhi'),
### # ('Priya', 22, 'Mumbai'),
### # ('Amit', 20, 'Chennai'),
### # ('Sara', 23, 'Kolkata');

### # SELECT USER();



import mysql.connector # pip install mysql-connector-python
con =mysql.connector.connect(
host="localhost",
user="root",
password ="DON@1234rocky",  #pass=123456
database = "collage"
)
if con.is_connected():
    print("sucessful")
while True :
    cursor = con.cursor()
    print("1 insert the record")
    print("2 view the records")
    print("3 update the records")
    print("4 delete the records ")
    print("5 exit")

    choice = int(input("Enter the no:"))
    if choice == 1:
        name =input("Enter the name :")
        age = int(input("Enter the age :"))
        city = input("Enter the city :")
        sql = "insert into student (name,age,city) values (%s,%s,%s)"
        values= (name,age,city)
        cursor.execute(sql,values)
        con.commit()
        print("Record insert successfully")

    if choice == 2:
        cursor.execute("select * from student")
        records= cursor.fetchall()
        for rec in records:
            print(rec)

    if choice == 3:
        name = input("Enter the name:")
        city = input("Enter the age :")
        sql = "update student set age = %s where name = %s"
        values =(city , name)
        cursor.execute(sql,values)
        con.commit()
        print("Record update")

    if choice == 4:
        name = input("Enter the name :")
        sql = "delete from student where name = %s"
        cursor.execute(sql,(name,))
        con.commit()
        print("Record delete successfully")

    if choice == 5:
        print("exit",exit())




cursor.close()
con.close()
