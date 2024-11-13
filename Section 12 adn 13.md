## 12-1
1) It allows us to input any missing values and correct an false/null data
2) <img width="350" alt="image" src="https://github.com/user-attachments/assets/c6fafd12-c588-4099-bab3-557447439b8e">  <img width="350" alt="image" src="https://github.com/user-attachments/assets/ea237385-389e-48d3-9176-aaa009e22862">
<img width="350" alt="image" src="https://github.com/user-attachments/assets/4253afe1-93c9-45dc-9045-5ebc51c102bb">

3) <img width="350" alt="image" src="https://github.com/user-attachments/assets/2d3ae168-2429-489c-8f25-d53395b36f35">
<img width="350" alt="image" src="https://github.com/user-attachments/assets/f33283ad-53ea-4008-8f49-a43acd563d53">

The syntax seems to be fine, but the only two prompts I'm given is either that the command hasn't ended properly or I'm missing a word. I'm unsure what else to do since the previous question had the same format and worked out fine. 

4) <img width="350" alt="image" src="https://github.com/user-attachments/assets/bfb4faca-1cc8-4eeb-a1e5-0cef06444328">
Oracle was giving me the same issues as the previous question until I ran each "INSERT" command separately 

5) <img width="954" alt="image" src="https://github.com/user-attachments/assets/4b1e7e09-be76-4124-8e95-dada03054721">

6) <img width="416" alt="image" src="https://github.com/user-attachments/assets/94429367-5669-4c5f-ba87-9c3c616e2a8d">

## 12-2 
1) For this question, an UPDATE clause would be used. For example UPDATE copy_f_update_items SET price = 3.75 WHERE item_name = "Strawberry Shake"
2) An UPDATE clause would be used and a NVL clause could be used to change the function from null to 0. For example UPDATE copy_f_staffs SET overtime_pay = NVL(overtime_pay, 0) + 0.75 WHERE first_name = 'Bob' AND last_name = 'Miller
3) To insert orders, the INSERT clause would be used
4) To first check if the employee exists, a SELECT * clause can be used for the copy_f_customers table. If the employee isn't there, then an INSERT clause would be used
5) Use a UPDTE clause to match the salaries: UPDATE copy_f_staffs SET salary = (SELECT salary FROM copy_f_staffs WHERE first_name = 'Bob' AND last_name = 'Miller')  WHERE first_name = 'Sue' AND last_name = 'Doe';
6) Use an INSERT clause to add Kai's details
7) Use an UPDATE clause to reflect that Kai has the same manager as Sue and other details
8) TO delete the department use the DELETE FROM departments WHERE department_id = 60
9) To delete Kai's info the DELETE clause can also be used: DELETE FROM copy_f_staffs WHERE first_name = 'Kai' AND Last_name = 'Kim'
10) Create the table using the CREATE clause. Then to delete use DELETE FROM lesson7_emp e WHERE EXISTS (SELECT 1 FROM job_history j WHERE j.employee_id = e.employeeID)

## 12-3
1) A DEFAULT value is useful for a column to have a data point automatically entered, even if nothing is provided during the INSERT clause.
2) <img width="923" alt="image" src="https://github.com/user-attachments/assets/bbc86ec1-e6b0-4e5a-ba21-d45bc717b56f">
3) <img width="953" alt="image" src="https://github.com/user-attachments/assets/24857c7e-6e91-4b88-bc24-f1f43b2fae78">
4) <img width="581" alt="image" src="https://github.com/user-attachments/assets/3ce9d65b-a88e-4f8f-a436-4e25f10ca4c6">
<img width="583" alt="image" src="https://github.com/user-attachments/assets/9163a4c2-0f6c-451e-83bd-8d131d7daac6">
<img width="673" alt="image" src="https://github.com/user-attachments/assets/67c09b96-b37d-417e-adfc-ceaee31df864">

## 13-1 
1) FK column should have the foreign key = requirements column
2) Afer creating the foreign key, you can use the following syntax: <img width="248" alt="image" src="https://github.com/user-attachments/assets/35f49d30-dedb-4076-8fd6-7681ea7697d6">
3) <img width="467" alt="image" src="https://github.com/user-attachments/assets/1a65320d-8e27-4635-9689-9d5c059f9236">
4) <img width="214" alt="image" src="https://github.com/user-attachments/assets/fffc3180-6f93-46d2-84b4-74c1684c3b81">
5) <img width="423" alt="image" src="https://github.com/user-attachments/assets/9e81eb57-ab8b-4820-ae8f-9ef27d9f50ad"> I had to cut down the names because the max number of characters for last name was 3 and for first name was 2
6) <img width="910" alt="image" src="https://github.com/user-attachments/assets/8dcd0eeb-667a-4ce1-aa51-d830f450eabc">
<img width="946" alt="image" src="https://github.com/user-attachments/assets/f1d722ba-2b11-45be-b262-61c585f564f9">
<img width="827" alt="image" src="https://github.com/user-attachments/assets/b6fac6ab-2ba3-4cdf-a34d-59ece14a9f8a">

## 13-2

1) <img width="581" alt="image" src="https://github.com/user-attachments/assets/51c25889-1cd2-4c03-9a1e-0fc493d22bac">
<img width="722" alt="image" src="https://github.com/user-attachments/assets/62859fb5-3b67-4343-bb46-e468e3e44300"> It keeps saying there's a missing coma, but there is none. Table was created but there's no data 
<img width="566" alt="image" src="https://github.com/user-attachments/assets/1fc4385d-890e-4e8b-8e07-9c529ae40400">

2) <img width="778" alt="image" src="https://github.com/user-attachments/assets/50b4cdac-b308-4011-b570-56fa2ebb6ef0">
<img width="905" alt="image" src="https://github.com/user-attachments/assets/545bae71-0d8d-497f-b326-764f885d9d89">

3) It's important to be aware of time zones and the associated dates when a company has global offices/ international workers, booking the correct flights from foreign countries (ie. a flight stating that you're landing at 7am but the country is an hour ahead from your native country)


## 13-3 
1) <img width="803" alt="image" src="https://github.com/user-attachments/assets/70f24e7e-8948-4579-9a73-c60ef5e15653">
2) <img width="896" alt="image" src="https://github.com/user-attachments/assets/89284f2e-ebba-48f9-8cfb-34ebbc610b8b">
3) <img width="397" alt="image" src="https://github.com/user-attachments/assets/77d700e1-faa4-4dcc-a153-1ac2ff18a593">
4) <img width="317" alt="image" src="https://github.com/user-attachments/assets/b9e29ba8-9b29-48fd-8e13-2a1310b55f38">













