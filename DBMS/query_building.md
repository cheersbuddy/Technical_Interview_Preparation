# RESOURCES
- [Highest 2nd salary] (https://www.geeksforgeeks.org/sql-query-to-find-second-largest-salary/)
- [avg salary] (https://www.geeksforgeeks.org/finding-average-salary-of-each-department-in-sql-server/)
- [questions] (https://www.geeksforgeeks.org/interview-experience-with-avasoft/?utm_source=chatgpt.com "Interview Experience with Avasoft | GeeksforGeeks")



## 🧠 AVASOFT-Level SQL & Database Management Questions

### 🔹 Question 1: Retrieve Students Who Haven't Graduated

**Table:** `Student`

**Columns:** `id`, `name`, `graduation_status` (`'Completed'` or `'Not Completed'`)

**Task:** Write an SQL query to fetch details of students who have not completed graduation.

---

### 🔹 Question 2: Employees with Salary Above 70,000

**Table:** `Employee`

**Columns:** `emp_id`, `emp_name`, `salary`

**Task:** Write an SQL query to retrieve details of employees earning more than 70,000.

---

### 🔹 Question 3: Second Highest Salary

**Table:** `Employee`

**Columns:** `emp_id`, `emp_name`, `salary`

**Task:** Write an SQL query to find the second highest salary in the Employee table.

---

### 🔹 Question 4: Posts Liked by Followers and Non-Followers

**Table:** `PostLikes`

**Columns:** `post_id`, `user_id`, `is_follower` (`TRUE` or `FALSE`)

**Task:** For each post, count the number of likes from followers and non-followers.

---

### 🔹 Question 5: Employees Without Assigned Projects

**Tables:**

* `Employee`: `emp_id`, `emp_name`
* `ProjectAssignment`: `emp_id`, `project_id`

**Task:** Write an SQL query to find employees who are not assigned to any project.

---

### 🔹 Question 6: Average Salary per Department

**Table:** `Employee`

**Columns:** `emp_id`, `emp_name`, `department_id`, `salary`

**Task:** Write an SQL query to calculate the average salary for each department.

---

### 🔹 Question 7: Top 3 Highest Paid Employees

**Table:** `Employee`

**Columns:** `emp_id`, `emp_name`, `salary`

**Task:** Write an SQL query to retrieve the top 3 highest-paid employees.

---

### 🔹 Question 8: Employees with Same Salary

**Table:** `Employee`

**Columns:** `emp_id`, `emp_name`, `salary`

**Task:** Write an SQL query to find employees who share the same salary.

---

### 🔹 Question 9: Departments with More Than 5 Employees

**Table:** `Employee`

**Columns:** `emp_id`, `emp_name`, `department_id`

**Task:** Write an SQL query to find departments that have more than 5 employees.

---

### 🔹 Question 10: Employees Without Managers

**Table:** `Employee`

**Columns:** `emp_id`, `emp_name`, `manager_id`

**Task:** Write an SQL query to find employees who do not have a manager.

---

### ✅ 1. Corrected:

```sql
SELECT name FROM Student WHERE graduation_status = 'Not Completed';
```

* ❌ Fix: Use `=` not `==` in SQL.
* ✅ Note: SQL uses **single `=`** for comparisons.

---

### ✅ 2. Corrected:

```sql
SELECT emp_name FROM Employee WHERE salary > 70000;
```

* ❌ Fix: Remove comma in `70,000` – SQL doesn't recognize commas in numbers.
* ✅ Tip: Use `> 70000` without formatting.

---

### ✅ 3. Corrected (Second Highest Salary):

```sql
SELECT MAX(salary) 
FROM Employee 
WHERE salary < (SELECT MAX(salary) FROM Employee);
```

* ❌ Fix: Your version `LIMIT 1,1` won't work in all SQL dialects (e.g., not supported in some systems).
* ✅ Tip: Safer to use **nested MAX()** or **DENSE\_RANK() OVER()** for precision.

---

### ✅ 4. Corrected:

```sql
SELECT post_id,
       SUM(CASE WHEN is_follower THEN 1 ELSE 0 END) AS followers,
       SUM(CASE WHEN NOT is_follower THEN 1 ELSE 0 END) AS non_followers
FROM PostLikes
GROUP BY post_id;
```

* ❌ Fix: Typo in alias (`none-followers` → `non_followers`).
* ✅ Tip: Avoid dashes `-` in aliases, use `_`.

---

### ✅ 5. Correct:

```sql
SELECT emp_name 
FROM Employee 
WHERE emp_id NOT IN (SELECT emp_id FROM ProjectAssignment);
```

* ✅ Clean and correct.
* ⚠️ Caution: `NOT IN` fails with `NULL`s. Safer to use `LEFT JOIN ... IS NULL` if nulls are possible.

---

### ✅ 6. Correct:

```sql
SELECT department_id, AVG(salary) AS avg_salary 
FROM Employee 
GROUP BY department_id;
```

* ✅ Perfect.

---

### ❌ 7. Fix (Top 3 Highest Paid Employees):

```sql
SELECT emp_name 
FROM Employee 
ORDER BY salary DESC 
LIMIT 3;
```

* ❌ Your version fetches only top 1, not top 3.
* ✅ Tip: Read questions carefully — they’ll often check precision like "Top **3**".

---

### ❌ 8. Fix (Employees with Same Salary):

```sql
SELECT emp_name 
FROM Employee 
WHERE salary IN (
    SELECT salary FROM Employee GROUP BY salary HAVING COUNT(*) > 1
);
```

* ❌ Fix: Your syntax had `where in` → should be `WHERE salary IN (...)`
* ✅ Tip: Match column types inside `IN (...)`

---

### ❌ 9. Fix (Departments with > 5 Employees):

```sql
SELECT department_id 
FROM Employee 
GROUP BY department_id 
HAVING COUNT(emp_id) > 5;
```

* ❌ Fix: `WHERE count(emp_id)>5` is invalid — use `HAVING` with aggregates.

---

### ✅ 10. Correct:

```sql
SELECT emp_name FROM Employee WHERE manager_id IS NULL;
```

* ✅ Perfect.

---

## 📝 QUICK REVIEW NOTES FOR INTERVIEW (Database/SQL)

### 📌 SQL Comparison Rules:

* Use `=` not `==`
* No commas in numbers: `70000` not `70,000`

### 📌 Aggregation & Filtering:

* Use `HAVING` for aggregates (e.g., `HAVING COUNT(*) > 1`)
* Use `GROUP BY` with any column you're aggregating

### 📌 Subqueries:

* Use `IN` or `EXISTS` to filter with subqueries
* `NOT IN` can be dangerous with `NULL`s — use `LEFT JOIN ... IS NULL` if unsure

### 📌 Ranking Techniques:

* `MAX()` with condition: second highest value
* `DENSE_RANK() OVER (ORDER BY salary DESC)` for top-N safely

### 📌 Join vs Subquery:

* `LEFT JOIN ... IS NULL` → safest way to find "non-matches"
* Use `JOIN` when you need values from both tables

---
