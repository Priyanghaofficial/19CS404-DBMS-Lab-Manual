# Experiment 2: DDL Commands

## AIM
To study and implement DDL commands and different types of constraints.

## THEORY

### 1. CREATE
Used to create a new relation (table).

**Syntax:**
```sql
CREATE TABLE (
  field_1 data_type(size),
  field_2 data_type(size),
  ...
);
```
### 2. ALTER
Used to add, modify, drop, or rename fields in an existing relation.
(a) ADD
```sql
ALTER TABLE std ADD (Address CHAR(10));
```
(b) MODIFY
```sql
ALTER TABLE relation_name MODIFY (field_1 new_data_type(size));
```
(c) DROP
```sql
ALTER TABLE relation_name DROP COLUMN field_name;
```
(d) RENAME
```sql
ALTER TABLE relation_name RENAME COLUMN old_field_name TO new_field_name;
```
### 3. DROP TABLE
Used to permanently delete the structure and data of a table.
```sql
DROP TABLE relation_name;
```
### 4. RENAME
Used to rename an existing database object.
```sql
RENAME TABLE old_relation_name TO new_relation_name;
```
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE) or after it is created (using ALTER TABLE).
### 1. NOT NULL
When a column is defined as NOT NULL, it becomes mandatory to enter a value in that column.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) NOT NULL
);
```
### 2. UNIQUE
Ensures that values in a column are unique.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) UNIQUE
);
```
### 3. CHECK
Specifies a condition that each row must satisfy.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) CHECK (logical_expression)
);
```
### 4. PRIMARY KEY
Used to uniquely identify each record in a table.
Properties:
Must contain unique values.
Cannot be null.
Should contain minimal fields.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) PRIMARY KEY
);
```
### 5. FOREIGN KEY
Used to reference the primary key of another table.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size),
  FOREIGN KEY (column_name) REFERENCES other_table(column)
);
```
### 6. DEFAULT
Used to insert a default value into a column if no value is specified.

Syntax:
```sql
CREATE TABLE Table_Name (
  col_name1 data_type,
  col_name2 data_type,
  col_name3 data_type DEFAULT 'default_value'
);
```

**Question 1**
--
<img width="736" height="305" alt="image" src="https://github.com/user-attachments/assets/fffdf580-dec7-4b9b-adf6-7aff8eb9fc8e" />


```
CREATE TABLE Products
(
ProductID PRIMARY KEY,
ProductName TEXT NOT NULL,
Price REAL CHECK(Price>0),
Stock INTEGER CHECK(Stock>=0)
)

```

**Output:**

<img width="1067" height="181" alt="image" src="https://github.com/user-attachments/assets/f0135fa3-9650-461f-8baf-2612558bb51e" />


**Question 2**

<img width="894" height="447" alt="image" src="https://github.com/user-attachments/assets/18a6b1f6-a43c-4891-b630-6d2791a7bc20" />

```
ALTER TABLE customer ADD COLUMN email VARCHAR(100)

```

**Output:**

<img width="1328" height="279" alt="image" src="https://github.com/user-attachments/assets/1ef7797d-e6a4-4c10-b18b-8bfd4edb783e" />


**Question 3**

<img width="1159" height="325" alt="image" src="https://github.com/user-attachments/assets/b0208327-70e3-4621-92e2-fd64410c0652" />

```
INSERT INTO Customers(CustomerID ,Name,Address ,City,ZipCode)
VALUES(306 ,'Diana Prince',  'Themyscira',NULL,NULL);
INSERT INTO Customers(CustomerID ,Name,Address ,City,ZipCode)
VALUES(307,'Bruce Wayne',   'Wayne Manor',  'Gotham',10007);
INSERT INTO Customers(CustomerID ,Name,Address ,City,ZipCode)
VALUES(308,'Peter Parker',  'Queens',NULL, 11375);
```

**Output:**

<img width="1003" height="189" alt="image" src="https://github.com/user-attachments/assets/94e99cf6-604d-4ddf-a03d-5129dd9cdb8c" />


**Question 4**
<img width="1031" height="233" alt="image" src="https://github.com/user-attachments/assets/8d937bc8-7fd7-4d56-b9a5-e7774368f548" />


```
CREATE TABLE Products 
(
ProductID INTEGER PRIMARY KEY,
ProductName TEXT UNIQUE NOT NULL,
Price REAL CHECK (Price>0),
StockQuantity INTEGER CHECK (StockQuantity>0)
)
```

**Output:**

<img width="1295" height="184" alt="image" src="https://github.com/user-attachments/assets/f39c2022-b506-47b4-8393-6b8afe0950f5" />


**Question 5**
---
-- Paste Question 5 here

```sql
-- Paste your SQL code below for Question 5
```

**Output:**

![Output5](output.png)

**Question 6**
<img width="724" height="149" alt="image" src="https://github.com/user-attachments/assets/7a0e583d-ca1a-487a-9012-c68c0bbe4ac6" />

```
create table contacts
(
contact_id INTEGER PRIMARY KEY,
first_name TEXT NOT NULL,
last_name TEXT NOT NULL,
email TEXT,
phone TEXT NOT NULL CHECK(LENGTH(phone)>=10)


);
```

**Output:**

<img width="1311" height="227" alt="image" src="https://github.com/user-attachments/assets/a711d194-f2a8-495a-8c24-e3063eabc10e" />


**Question 7**
---
-- Paste Question 7 here

```sql
-- Paste your SQL code below for Question 7
```

**Output:**

![Output7](output.png)

**Question 8**
---
-- Paste Question 8 here

```sql
-- Paste your SQL code below for Question 8
```

**Output:**

![Output8](output.png)

**Question 9**
---
-- Paste Question 9 here

```sql
-- Paste your SQL code below for Question 9
```

**Output:**

![Output9](output.png)

**Question 10**
---
-- Paste Question 10 here

```sql
-- Paste your SQL code below for Question 10
```

**Output:**

![Output10](output.png)


## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
