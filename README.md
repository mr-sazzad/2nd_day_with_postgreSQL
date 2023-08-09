POSTGRE SQL
- 2️⃣ DAY

  ```sql
  -- PAGINATION IN POSTGRE SQL

  ✅ SELECT * FROM Employee ORDER BY name DESC;   --DESCENDING ORDER
  
  ✅ SELECT * FROM Employee ORDER BY name DESC; --ASCENDING ORDER

  ✅ SELECT * FROM Employee ORDER BY name DESC LIMIT 1; -- LAST ITEM OR ONLY ONE ITEM FROM DESCENDING ORDER

  ✅ SELECT * FROM Employee ORDER BY name DESC LIMIT 1 OFFSET 5; -- 6TH ITEM FROM LAST


  -- IN, NOT IN, BETWEEN, LIKE


  ✅ SELECT * FROM Employee WHERE empID IN (3, 5, 244)  -- GIVE ME JUST THOSE ITEMS WHICH CONTAIN THESE ID'S 🎈

  ✅ SELECT * FROM Employee WHERE empID NOT IN (1, 7, 2)  -- GIVE ME JUST THOSE ITEMS WHICH NOT CONTAIN THESE ID'S 🥗

  ✅ SELECT * FROM Employee WHERE empID BETWEEN 40 AND 50  -- GIVE ME JUST THOSE ITEMS WHICH BETWEEN 40 TO 50 🥱


  -- STRING SEARCHING

  ✅ SELECT * FROM Employee WHERE name LIKE '%A%';  -- GIVE ME JUST THOSE ITEMS WHICH CONTAIN A EOES NOT METTERE WHERE (CASE SENSITIVE 🥵)

  ✅ SELECT * FROM Employee WHERE name LIKE 'A%';  -- GIVE ME JUST THOSE ITEMS WHICH ARE STARTED WITH CHARACTER A (CASE SENSITIVE 🥵)

  ✅ SELECT * FROM Employee WHERE name LIKE '%A';  -- GIVE ME JUST THOSE ITEMS WHICH ARE ENDS WITH CHARACTER A (CASE SENSITIVE 🥵)


  -- SPECIFIC POSITION ![ValeuValtatuiPositivoValtatuiGIF](https://github.com/mr-sazzad/2nd_day_with_postgreSQL/assets/97055612/f96e4857-82bb-47bf-b059-d9ff979b6014)


  ✅ SELECT * FROM Employee WHERE name LIKE '_A%';  -- GIVE ME JUST THOSE ITEMS THERE SECOND LETTER IS A (CASE SENSITIVE 🥵)

  ✅ SELECT * FROM Employee WHERE name LIKE '__A%';  -- GIVE ME JUST THOSE ITEMS THERE THIRED LETTER IS A (CASE SENSITIVE 🥵)

  ✅ SELECT * FROM Employee WHERE name LIKE '__A__';  -- GIVE ME JUST THOSE ITEMS THERE THIRED/MIDDLE  LETTER IS A (CASE SENSITIVE 🥵)

  ✅ SELECT * FROM Employee WHERE name LIKE 'A%O';  -- GIVE ME JUST THOSE ITEMS THERE FIRST LETTER IS A AND LAST LETTER IS O (CASE SENSITIVE 🥵)

  -- GET ROWS THEIR DEFINED COLUMN IS NULL 🪹

  ✅ SELECT * FROM Employee WHERE name IS NULL;  -- GIVE ME JUST THOSE ITEMS THERE NAME VALUE IS NULL (CASE SENSITIVE 🥵) 1️⃣

  ✅ SELECT * FROM Employee WHERE name = NULL;  -- GIVE ME JUST THOSE ITEMS THERE NAME VALUE IS NULL (CASE SENSITIVE 🥵) 2️⃣
  
 ```
