# 10-1#
1) The Subquery pulls data within a subset. The command line would requre a SELECT statment embedded in anohter clause of a SELECT statement
2) The subquery pulls information that you don't know
3)<img width="711" alt="image" src="https://github.com/user-attachments/assets/463bd39c-8072-41bd-b61b-613272f99e9a">
4) <img width="763" alt="image" src="https://github.com/user-attachments/assets/7c4f9948-d8e7-4862-80d6-2b11b10371f0">
5) <img width="650" alt="image" src="https://github.com/user-attachments/assets/235712eb-43a8-4db9-8c76-be02685f7ee7">
6) <img width="499" alt="image" src="https://github.com/user-attachments/assets/92fe6fec-3350-4013-a981-5f6097634bf6">
7) <img width="617" alt="image" src="https://github.com/user-attachments/assets/cc1c73ff-663a-44e7-913e-5855a0b6d86f">
8) <img width="595" alt="image" src="https://github.com/user-attachments/assets/2dd67b4c-5c5f-44a3-807f-47981d6adf51">
9) <img width="665" alt="image" src="https://github.com/user-attachments/assets/34418ed7-a2b5-4b89-9ce1-ad46cff0f8ab">
10) <img width="650" alt="image" src="https://github.com/user-attachments/assets/60228bd5-44ee-4ab3-bb03-ec912044e006">
11) a:T b:F c: T

# 10-2
1) <img width="583" alt="image" src="https://github.com/user-attachments/assets/1bee8772-7126-4785-9195-30fef64f61b4">
2) <img width="502" alt="image" src="https://github.com/user-attachments/assets/97bed383-7c31-4560-a89d-1b85878357e5">
3) <img width="662" alt="image" src="https://github.com/user-attachments/assets/23b0ef88-cd8b-4de4-bc87-da20f4305878">
4) <img width="659" alt="image" src="https://github.com/user-attachments/assets/ec017c51-9342-4299-9767-42fd803c9b1a">
5) <img width="458" alt="image" src="https://github.com/user-attachments/assets/493dfc04-a15c-4a89-ad41-817f78dca797">

# 10-3
1) If the subquery returns a null, then nothing else will be returned
2) <img width="434" alt="image" src="https://github.com/user-attachments/assets/88e81a04-7304-4a25-9bfb-8c28103bde2a">
3) <img width="403" alt="image" src="https://github.com/user-attachments/assets/d0511f83-15c1-4287-b9ad-368715eb1c19">
4) <img width="536" alt="image" src="https://github.com/user-attachments/assets/1bd0069c-d99c-47d7-8816-145db241bd7e">
5) 
   - SELECT year FROM d_cds WHERE title = 'Carpe Diem'
   - (SELECT salary FROM employees WHERE department_id = (SELECT department_id FROM departments WHERE department_name = 'IT') AND job_id = 'Programmer')
   - (SELECT year FROM d_cds WHERE title IN ('Party Music for All Occasions', 'Carpe Diem'))
   - (SELECT duration FROM d_songs WHERE type_code = 77)
  
6) a:T b:F c:T d:T e: F
7) The min salary needs to use the HAVNG clause and GROUP BY needs to be included as well
8) a:F b: T c:F d:F
9) SELECT last_name, first_name, department_id, manager_id
FROM employees e
WHERE (e.department_id, e.manager_id) = (
    SELECT department_id, manager_id
    FROM employees
    WHERE employee_id = 141
)
AND e.employee_id != 141;

10)  SELECT last_name, first_name, department_id, manager_id
FROM employees
WHERE department_id = (
    SELECT department_id
    FROM employees
    WHERE employee_id = 141
)
AND manager_id = (
    SELECT manager_id
    FROM employees
    WHERE employee_id = 141
)
AND employee_id != 141;

# 10-4 

1) Correlated subquery: refers to columns from the outer query. Non-corrleated: independent of the outer query
2) SELECT last_name, department_id, salary
FROM employees e
WHERE salary = (
    SELECT MAX(salary)
    FROM employees
    WHERE department_id = e.department_id)

3) SELECT e.last_name, e.department_id, e.salary
FROM employees e
WHERE 'x' IN (
    SELECT 'x'
    FROM employees e2
    WHERE e2.manager_id = e.employee_id
)
ORDER BY e.department_id;

4) <img width="849" alt="image" src="https://github.com/user-attachments/assets/ad745714-5be5-4260-b0ae-5ee1d825d950">

# 11-1

No questions in this section. Summary of lesson was on how to create and modify a query to produce specified data 


   















