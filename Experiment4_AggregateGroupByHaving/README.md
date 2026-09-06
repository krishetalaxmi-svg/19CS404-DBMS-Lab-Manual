# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
--
-- How many patients have insurance coverage valid in each year?

```sql
-- select strftime('%Y',validityperiod) as ValidityYear,count(patientid) as TotalPatients
from Insurance group by ValidityYear;
```

**Output:**

<img width="691" height="367" alt="image" src="https://github.com/user-attachments/assets/387bd00d-d809-4ca3-9be4-959a2d8a20d3" />


**Question 2**
---
-- How many prescriptions were written by each doctor?

```sql
-- select DoctorID, count(*) as TotalPrescriptions
from Prescriptions group by DoctorID;
```

**Output:**

<img width="791" height="736" alt="image" src="https://github.com/user-attachments/assets/3bcc244d-4966-495a-aa8d-f188f6625a99" />


**Question 3**
---
--How many prescriptions were written in each frequency category (e.g., once daily, twice daily)?
```sql
-- select Frequency, count(*) as TotalPrescriptions 
from Prescriptions group by Frequency;
```

**Output:**

<img width="761" height="515" alt="image" src="https://github.com/user-attachments/assets/88d737e7-8a94-4da5-8271-b5a4af73238d" />

**Question 4**
---
-- Write a SQL query to find the difference between the maximum and minimum price of fruits?

```sql
-- select MAX(price) - MIN(price) as price_diff
from fruits;
```

**Output:**

<img width="381" height="295" alt="image" src="https://github.com/user-attachments/assets/90f139a7-3fbc-4185-9e59-79a9161a59ec" />


**Question 5**
---
-- Write a SQL query to find the youngest employee in the company?

```sql
-- select  name as Employee_Name , MIN(age) as Age
from employee;
```

**Output:**

<img width="592" height="296" alt="image" src="https://github.com/user-attachments/assets/555228e1-dc93-4527-8236-86621136c41d" />


**Question 6**
---
--Write a SQL query to Calculate the average income of the employees with names starting with 'A':

```sql
-- select avg(income) as avg_income from employee where name LIKE 'A%';
```

**Output:**

<img width="407" height="300" alt="image" src="https://github.com/user-attachments/assets/03699839-f0ed-4d96-928a-6ffdbc5fea5b" />


**Question 7**
---
-- Write a SQL query to calculate the total number of working hours of all employees

```sql
-- select SUM(workhour) as "Total working hours"
from employee1;
```

**Output:**

<img width="507" height="302" alt="image" src="https://github.com/user-attachments/assets/730724eb-3823-42fd-9c49-270ae8fcbeac" />

**Question 8**
---
-- Write the SQL query that accomplishes the selection of average price for each category from the "products" table and includes only those products where the average price falls between 10 and 15.

```sql
-- select category_id, AVG(Price) from  products group by category_id having AVG(price) 
between 10 and 15;
```

**Output:**

<img width="577" height="323" alt="image" src="https://github.com/user-attachments/assets/54591feb-4097-4782-af0e-1a36df61ce63" />


**Question 9**
---
-- Write the SQL query that accomplishes the selection of total number of products for each category from the "products" table, and includes only those products where the minimum category ID is less than 3.

```sql
-- select category_id,count(product_name) from products
group by category_id
having MIN(category_id) <3;
```

**Output:**

<img width="737" height="352" alt="image" src="https://github.com/user-attachments/assets/da366f33-0e32-48d1-91ac-8ead6eafed5b" />


**Question 10**
---
-- Write the SQL query that achieves the selection of product names and the maximum price for each category from the "products" table, and includes only those products where the maximum price is greater than 15.

```sql
-- select category_id,product_name, price as Price
from products group by category_id having MAX(Price) >15;
```

**Output:**

<img width="817" height="370" alt="image" src="https://github.com/user-attachments/assets/bc25a82e-4bcd-4129-9cdb-35d7e5436daf" />



## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
