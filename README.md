[![PostgreSQL Image](https://kinsta.com/wp-content/uploads/2022/02/postgres-logo.png)](https://github.com/mr-sazzad)



POSTGRE SQL
- 2️⃣ DAY

  ```sql
  -- PAGINATION IN POSTGRE SQL

  ✅ SELECT * FROM Employee ORDER BY name DESC;   --DESCENDING ORDER
  
  ✅ SELECT * FROM Employee ORDER BY name DESC; --ASCENDING ORDER

  ✅ SELECT * FROM Employee ORDER BY name DESC LIMIT 1; -- LAST ITEM OR ONLY ONE ITEM FROM DESCENDING ORDER

  ✅ SELECT * FROM Employee ORDER BY name DESC LIMIT 1 OFFSET 5; -- 6TH ITEM FROM LAST


  -- IN, NOT IN, BETWEEN, LIKE


  ✅ SELECT * FROM Employee WHERE empID IN (3, 5, 244)  -- GIVE ME JUST THOSE ITEMS WHICH CONTAIN THESE ID 🎈

  ✅ SELECT * FROM Employee WHERE empID NOT IN (1, 7, 2)  -- GIVE ME JUST THOSE ITEMS WHICH NOT CONTAIN THESE ID'S 🥗

  ✅ SELECT * FROM Employee WHERE empID BETWEEN 40 AND 50  -- GIVE ME JUST THOSE ITEMS WHICH BETWEEN 40 TO 50 🥱


  -- STRING SEARCHING

  ✅ SELECT * FROM Employee WHERE name LIKE '%A%';  -- GIVE ME JUST THOSE ITEMS WHICH CONTAIN A EOES NOT METTERE WHERE (CASE SENSITIVE 🥵)

  ✅ SELECT * FROM Employee WHERE name LIKE 'A%';  -- GIVE ME JUST THOSE ITEMS WHICH ARE STARTED WITH CHARACTER A (CASE SENSITIVE 🥵)

  ✅ SELECT * FROM Employee WHERE name LIKE '%A';  -- GIVE ME JUST THOSE ITEMS WHICH ARE ENDS WITH CHARACTER A (CASE SENSITIVE 🥵)


  -- SPECIFIC POSITION 👾

  ✅ SELECT * FROM Employee WHERE name LIKE '_A%';  -- GIVE ME JUST THOSE ITEMS THERE SECOND LETTER IS A (CASE SENSITIVE 🥵)

  ✅ SELECT * FROM Employee WHERE name LIKE '__A%';  -- GIVE ME JUST THOSE ITEMS THERE THIRED LETTER IS A (CASE SENSITIVE 🥵)

  ✅ SELECT * FROM Employee WHERE name LIKE '__A__';  -- GIVE ME JUST THOSE ITEMS THERE THIRED/MIDDLE  LETTER IS A (CASE SENSITIVE 🥵)

  ✅ SELECT * FROM Employee WHERE name LIKE 'A%O';  -- GIVE ME JUST THOSE ITEMS THERE FIRST LETTER IS A AND LAST LETTER IS O (CASE SENSITIVE 🥵)

  -- GET ROWS THEIR DEFINED COLUMN IS NULL 🪹

  ✅ SELECT * FROM Employee WHERE name IS NULL;  -- GIVE ME JUST THOSE ITEMS THERE NAME VALUE IS NULL (CASE SENSITIVE 🥵) 1️⃣

  ✅ SELECT * FROM Employee WHERE name = NULL;  -- GIVE ME JUST THOSE ITEMS THERE NAME VALUE IS NULL (CASE SENSITIVE 🥵) 2️⃣


  -- JOINING 🧑‍🤝‍🧑
  -- 1️⃣ INNER JOIN IT WORKS ON TOWDAIMENTION
  
  SELECT e.name, e.job_role, depertment_name    -- name and job_role FROM EMPLOYEE TABLE AND department_name FROM DEPARTMENT TABLE
   FROM Employee e  -- ALIAS
   INNER JOIN Department ON department_id = e.department_id   -- IT'S CALLED 'ON' CONDITION 🥗


  -- AGGREGATE 🎈

  1️⃣ SELECT AVG(salary) avarazeSalary FROM Employees   -- IS'S USED TO GETTING AVARAZE FROM A COLUMN AND avarazeSalary IS ALIAS 💡

  2️⃣ SELECT AVG(salary) AS avarazeSalary FROM Employees   -- WE ALSO CAN USE AS FOR ALIASING 💡

  3️⃣ SELECT MIN(salary) AS maxSalary FROM Employees   -- IT'S USED FOR GETTING MAX VALUE FROM A COLUMN 💡

  4️⃣ SELECT MAX(salary) AS minSalary FROM Employees   -- IT'S USED FOR GETTING MIN VALUE FROM A COLUMN 💡

  5️⃣ SELECT SUM(salary) AS totalSalary FROM Employees   -- IT'S USED FOR GETTING MIN VALUE FROM A COLUMN 💡


  SELECT deptId AVG(salary) FROM employees GROUP BY  deptId  -- CREATE GROUP AND GET THERE SALARY 💡

  SELECT * FROM EMPLOYEES e RIGHT JOIN departments d ON e.edptId = d.deptId  -- COMPLEX RIGHT JOIN MEANS RIGHT SIDE PRIORITY ✅

  SELECT d.name
  FROM EMPLOYEES e FULL JOIN departments d
  ON e.edptId = d.deptId
  GROUP BY d.name


  SELECT d.name, AVG(salary)
  FROM EMPLOYEES e FULL JOIN departments d
  ON e.edptId = d.deptId
  GROUP BY d.name


  SELECT d.name, AVG(salary) , SUM(salary), MAX(salary), MIN(salary)
  FROM EMPLOYEES e FULL JOIN departments d
  ON e.edptId = d.deptId
  GROUP BY d.name


  SELECT d.name, AVG(salary) , SUM(salary), MAX(salary), MIN(salary)
  FROM EMPLOYEES e FULL JOIN departments d
  ON e.edptId = d.deptId
  GROUP BY d.name
  HAVING AVG(e.salary) > 20000
 ```
