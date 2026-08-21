# Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**
<img width="1222" height="507" alt="Screenshot 2026-08-21 101605" src="https://github.com/user-attachments/assets/9328a3d9-88d4-4345-8ebc-89d6a1f236ea" />

sql
<img width="407" height="180" alt="Screenshot 2026-08-21 101638" src="https://github.com/user-attachments/assets/0a8ce1c1-2958-4565-9f46-206cf753742f" />




**Output:**
<img width="1237" height="406" alt="Screenshot 2026-08-21 101649" src="https://github.com/user-attachments/assets/79ba853a-ac85-46ae-aa5c-2fbba9ee9db2" />


![Output1](output.png)

**Question 2**
<img width="917" height="557" alt="Screenshot 2026-08-21 101659" src="https://github.com/user-attachments/assets/d0dcab9e-a864-4f21-baae-561d68ac3ef7" />



sql
<img width="363" height="210" alt="Screenshot 2026-08-21 101705" src="https://github.com/user-attachments/assets/f957661f-6d1d-4156-bd61-3b9c323aa3b2" />



**Output:**
<img width="1268" height="477" alt="Screenshot 2026-08-21 101717" src="https://github.com/user-attachments/assets/7d82c2c6-e64e-4f71-89a1-194137f91fc6" />




**Question 3**
<img width="1246" height="686" alt="Screenshot 2026-08-21 101734" src="https://github.com/user-attachments/assets/a2650a92-1daa-4bb3-b60e-d959cfdc83cf" />


sql
<img width="1232" height="310" alt="Screenshot 2026-08-21 101750" src="https://github.com/user-attachments/assets/8a6ad5b3-ff09-483d-b5a9-b12ef24f4bc3" />


**Output:**
<img width="1288" height="535" alt="Screenshot 2026-08-21 101804" src="https://github.com/user-attachments/assets/726d7eff-ba6c-4566-aa9c-e302b9b25c2d" />




**Question 4**
<img width="1237" height="636" alt="Screenshot 2026-08-21 101835" src="https://github.com/user-attachments/assets/ac209cf4-7f66-40f9-8f8f-2bc578c11965" />


sql
<img width="593" height="222" alt="Screenshot 2026-08-21 101844" src="https://github.com/user-attachments/assets/7930f84c-f512-46fb-b3b6-6a70ce257490" />



**Output:**
<img width="1260" height="842" alt="Screenshot 2026-08-21 101856" src="https://github.com/user-attachments/assets/2b7a1c1a-aa5b-48a4-ae86-400885e431bb" />



**Question 5**
<img width="1247" height="517" alt="Screenshot 2026-08-21 101908" src="https://github.com/user-attachments/assets/6a83ed11-7637-433f-97e7-8b3f73e82fc7" />

sql
<img width="551" height="247" alt="Screenshot 2026-08-21 101914" src="https://github.com/user-attachments/assets/ae74c1de-193d-44a7-92ce-d1d4acde68b0" />



**Output:**
<img width="585" height="371" alt="Screenshot 2026-08-21 101919" src="https://github.com/user-attachments/assets/7989e142-4787-48ea-bf14-929a646e0f55" />



**Question 6**
<img width="1177" height="636" alt="Screenshot 2026-08-21 102119" src="https://github.com/user-attachments/assets/824c1773-07bb-41d8-862c-934d9b6435ef" />

sql
<img width="797" height="250" alt="Screenshot 2026-08-21 102131" src="https://github.com/user-attachments/assets/1d9899c8-2eb7-436c-ae62-d073c72a2c21" />

**Output:**
<img width="1272" height="647" alt="Screenshot 2026-08-21 102143" src="https://github.com/user-attachments/assets/2eff2938-a1ec-4d38-b2c4-bdf011f25976" />



**Question 7**
<img width="1252" height="633" alt="Screenshot 2026-08-21 102156" src="https://github.com/user-attachments/assets/29a30e7b-e07d-4280-93b1-2cf283882665" />

sql
<img width="600" height="220" alt="Screenshot 2026-08-21 102208" src="https://github.com/user-attachments/assets/6a71a93b-5f65-4935-874b-db7878f6476f" />


**Output:**
<img width="1267" height="486" alt="Screenshot 2026-08-21 102217" src="https://github.com/user-attachments/assets/02660708-45e5-416b-be66-d1a6921b631c" />



**Question 8**
<img width="1246" height="552" alt="Screenshot 2026-08-21 102226" src="https://github.com/user-attachments/assets/c12e4498-7bb1-4d53-8627-aeb5234f475e" />


sql
<img width="427" height="130" alt="Screenshot 2026-08-21 102232" src="https://github.com/user-attachments/assets/ba2bee62-58cd-44bb-9908-cb4c305ed651" />


**Output:**
<img width="1261" height="557" alt="Screenshot 2026-08-21 102240" src="https://github.com/user-attachments/assets/acf3699e-8e32-4ace-8315-cace12353ed0" />



**Question 9**
<img width="781" height="462" alt="Screenshot 2026-08-21 102248" src="https://github.com/user-attachments/assets/52294a9f-7e62-4162-a034-d2bf66ccca83" />


sql
<img width="447" height="156" alt="Screenshot 2026-08-21 102257" src="https://github.com/user-attachments/assets/9b646ed4-0058-4ccf-81c9-ed41219d41d2" />



**Output:**
<img width="1241" height="827" alt="Screenshot 2026-08-21 102311" src="https://github.com/user-attachments/assets/d4dbcb1e-2c27-48d1-a491-2cb98f825900" />


**Question 10**

-- Paste Question 10 here
<img width="1245" height="630" alt="Screenshot 2026-08-21 102324" src="https://github.com/user-attachments/assets/f46e5ccc-5faf-4e5b-bdf2-2675eaab0fd4" />

sql
<img width="437" height="138" alt="Screenshot 2026-08-21 102329" src="https://github.com/user-attachments/assets/3769a9c9-041f-49ba-983c-3c264e90a628" />
**Output:**
<img width="1272" height="320" alt="Screenshot 2026-08-21 102337" src="https://github.com/user-attachments/assets/f8e364c7-d537-4762-9985-362ffc610fa7" />




## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
