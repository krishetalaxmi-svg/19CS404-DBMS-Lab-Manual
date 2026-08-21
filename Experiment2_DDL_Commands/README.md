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
<img width="1167" height="240" alt="Screenshot 2026-08-21 084621" src="https://github.com/user-attachments/assets/084e98e6-4b69-45e4-88ac-35a4de2f398d" />


sql


<img width="641" height="53" alt="Screenshot 2026-08-21 084826" src="https://github.com/user-attachments/assets/ca5d848f-e4bb-4945-bcf5-5045c4a18abb" />


**Output:**
<img width="1237" height="332" alt="Screenshot 2026-08-21 085043" src="https://github.com/user-attachments/assets/a7642efc-8c3c-44da-92a8-25fe6a87eb80" />






**Question 2**

<img width="1215" height="388" alt="Screenshot 2026-08-21 085211" src="https://github.com/user-attachments/assets/6f5f515d-bc81-43f3-8987-98663c36ef4f" />

sql
<img width="540" height="197" alt="Screenshot 2026-08-21 085317" src="https://github.com/user-attachments/assets/7f30c039-5ed7-45fb-bb37-c5c0cf3babd5" />

**Output:**
<img width="1235" height="425" alt="Screenshot 2026-08-21 085406" src="https://github.com/user-attachments/assets/4aafbfca-8a01-496b-a4f9-c63cbe195d46" />



**Question 3**

<img width="993" height="437" alt="Screenshot 2026-08-21 085509" src="https://github.com/user-attachments/assets/c7e9bdf4-f373-4d0f-b102-effaf157a223" />


sql
<img width="257" height="185" alt="Screenshot 2026-08-21 085638" src="https://github.com/user-attachments/assets/8f0bb3f5-ec3a-48c7-abb3-b8707bd33e63" />



**Output:**
<img width="1237" height="503" alt="Screenshot 2026-08-21 085714" src="https://github.com/user-attachments/assets/662d2ad6-7f4d-409c-bea6-34e8761e65b3" />

**Question 4**
<img width="1237" height="378" alt="Screenshot 2026-08-21 085801" src="https://github.com/user-attachments/assets/3a62b7e8-311d-417e-81e7-e7c573f68a26" />

sql
<img width="551" height="178" alt="Screenshot 2026-08-21 085916" src="https://github.com/user-attachments/assets/96f59e90-acf3-47c6-887c-c2daba81974e" />



**Output:**
<img width="1237" height="372" alt="Screenshot 2026-08-21 085951" src="https://github.com/user-attachments/assets/62a2e2a2-b577-45b0-8458-3f3138e82878" />


**Question 5**
<img width="995" height="318" alt="Screenshot 2026-08-21 090029" src="https://github.com/user-attachments/assets/2499ba37-133c-43d7-b263-ebf7c5761abb" />

sql
<img width="287" height="96" alt="Screenshot 2026-08-21 090113" src="https://github.com/user-attachments/assets/f5e63622-5eef-4d2d-bd73-97afa7c9b4be" />

**Output:**
<img width="1236" height="432" alt="Screenshot 2026-08-21 090143" src="https://github.com/user-attachments/assets/81aca84c-07f3-4575-bebf-50190212fe51" />


**Question 6**
<img width="838" height="377" alt="Screenshot 2026-08-21 090447" src="https://github.com/user-attachments/assets/59220aa1-baeb-46d5-beaa-d4aa6c4da352" />

sql
<img width="652" height="142" alt="Screenshot 2026-08-21 090524" src="https://github.com/user-attachments/assets/dda1bf0e-ebbe-405a-b361-00d1a5ed794a" />


**Output:**

<img width="1233" height="482" alt="Screenshot 2026-08-21 090600" src="https://github.com/user-attachments/assets/3b427db3-1933-4232-bdd5-32942a9d198b" />




**Question 7**
<img width="961" height="397" alt="Screenshot 2026-08-21 091016" src="https://github.com/user-attachments/assets/0a46442e-3241-4d4d-afba-1e74ceea6f96" />

sql
<img width="282" height="145" alt="Screenshot 2026-08-21 091050" src="https://github.com/user-attachments/assets/89e4e863-010c-4385-b1e8-815baef20ee9" />

**Output:**
<img width="1263" height="471" alt="Screenshot 2026-08-21 091138" src="https://github.com/user-attachments/assets/ddac6cee-4654-4b3f-b760-217c7fee3713" />



**Question 8**
<img width="1165" height="337" alt="Screenshot 2026-08-21 091254" src="https://github.com/user-attachments/assets/ad655801-8fd1-4ae4-a81b-e375321d9aef" />

sql
<img width="620" height="122" alt="Screenshot 2026-08-21 091434" src="https://github.com/user-attachments/assets/6f749fa3-c2bf-43d7-aaf9-6b0e08ca3ec4" />


**Output:**
<img width="1232" height="407" alt="Screenshot 2026-08-21 091508" src="https://github.com/user-attachments/assets/4a9a5635-29d5-428a-a43f-c9e75dd75b3d" />


**Question 9**
<img width="1220" height="330" alt="Screenshot 2026-08-21 091745" src="https://github.com/user-attachments/assets/66e70fd9-6db5-422f-9a0f-e5250a927f9f" />

sql
<img width="541" height="117" alt="Screenshot 2026-08-21 091835" src="https://github.com/user-attachments/assets/45e811b7-593d-426d-aa5e-f456db43ab41" />

**Output:**
<img width="1243" height="352" alt="Screenshot 2026-08-21 091913" src="https://github.com/user-attachments/assets/7b57d52d-56a8-440e-b83b-3942dce5fbd5" />

**Question 10**
<img width="1052" height="402" alt="Screenshot 2026-08-21 091958" src="https://github.com/user-attachments/assets/d44cb27f-64d3-4280-9a58-f1b556687cad" />

sql
<img width="597" height="282" alt="Screenshot 2026-08-21 092119" src="https://github.com/user-attachments/assets/f815753a-6f74-4b18-b12f-23c178b07059" />

**Output:**
<img width="1232" height="441" alt="Screenshot 2026-08-21 092159" src="https://github.com/user-attachments/assets/d514ad7b-1057-41dd-a388-d9ba4572a440" />



## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
