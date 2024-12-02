### 14-1 Intro to Constraints; NOT NULL and UNIQUE Constraints
1) Constraints are database rules that are maintained whenever a row is inserted, updated, or deleted from a table.
2) The constraints need to be clearly defined and listed separately. The column constraints need to be defined before listing table-level constraints.
3)  Since system-generated names are not easy to recognize, giving the constraints meaningful names is important.
4)  Id: NUMBER(10), name: VARCHAR2(100), date_opened: DATE, address: VARCHAR2(200), city: VARCHAR2(100), zip/postal code: VARCHAR2(10), phone: VARCHAR2(15), email: VARCHAR2(100), manager_id: NUMBER(10), Emergency contact: VARCHAR2(15)
5)  manager_id  and Emergency contact
6)  CREATE TABLE global_locations (
    id NUMBER(10) PRIMARY KEY,
    name VARCHAR2(100) NOT NULL,
    date_opened DATE NOT NULL,
    address VARCHAR2(200) NOT NULL,
    city VARCHAR2(100) NOT NULL,
    zip_postal_code VARCHAR2(10) NOT NULL,
    phone VARCHAR2(15) NOT NULL,
    email VARCHAR2(100) UNIQUE NOT NULL,
    manager_id NUMBER(10),
    emergency_contact VARCHAR2(15))
7) <img width="940" alt="image" src="https://github.com/user-attachments/assets/78736041-4171-45a6-b6e7-02f00490b35a">
8) <img width="930" alt="image" src="https://github.com/user-attachments/assets/c0807c61-a004-432a-b4bf-9a35fab7e015">
9) CREATE TABLE global_locations (
    id NUMBER(10) PRIMARY KEY,
    name VARCHAR2(100) NOT NULL,
    date_opened DATE NOT NULL,
    address VARCHAR2(200) NOT NULL,
    city VARCHAR2(100) NOT NULL,
    zip_postal_code VARCHAR2(10) NOT NULL,
    phone VARCHAR2(15) NOT NULL,
    email VARCHAR2(100) NOT NULL,
    manager_id NUMBER(10),
    emergency_contact VARCHAR2(15),
    CONSTRAINT unique_email UNIQUE (email)
);

### 14-2 PRIMARY KEY, FOREIGN KEY, and CHECK Constraints

1)
   - Primary key: Uniquely identifies each record in a table
   - Foreign Key: Enforces referential integrity between two tables
   - Check Constraints: Ensures that values in a column satisfy a specific condition or rule
2) Primary Key: animal_id
Unique Constraint: license_tag_number
NOT NULL Constraints: admit_date, vaccination_date
3) <img width="942" alt="image" src="https://github.com/user-attachments/assets/6dd88c16-ec8d-4b4d-9245-2d887e9fc7d9">
4) <img width="959" alt="image" src="https://github.com/user-attachments/assets/68970ed5-40fe-478a-af67-49ab7df14d16">
5) Column Level: CREATE TABLE animals (
    animal_id NUMBER(6),
    name VARCHAR2(25),
    license_tag_number NUMBER(10),
    admit_date DATE NOT NULL,
    adoption_id NUMBER(5),
    vaccination_date DATE NOT NULL,
    CONSTRAINT fk_adoption_id FOREIGN KEY (adoption_id) REFERENCES adoptions(adoption_id)); 

Table level: CREATE TABLE animals (
    animal_id NUMBER(6),
    name VARCHAR2(25),
    license_tag_number NUMBER(10),
    admit_date DATE NOT NULL,
    adoption_id NUMBER(5),
    vaccination_date DATE NOT NULL,
    CONSTRAINT pk_animal_id PRIMARY KEY (animal_id),
    CONSTRAINT unique_license_tag UNIQUE (license_tag_number),
    CONSTRAINT fk_adoption_id FOREIGN KEY (adoption_id) REFERENCES adoptions(adoption_id)
);


6) ON DELETE CASCADE: Automatically deletes the rows in the child table
ON DELETE SET NULL: Sets the foreign key value in the child table

7) The CHECK constraint explicitly defines a condition that must be met

### 14-3 Managing Constraints
1) The ALTER statement can add a constraint, modify a constraint, disable a constraint, and drop a constraint
2) ALTER TABLE copy_d_clients
ADD CONSTRAINT copy_d_clients_pk PRIMARY KEY (client_number);

3) ALTER TABLE copy_d_events
ADD CONSTRAINT copy_d_events_fk FOREIGN KEY (client_number)
REFERENCES copy_d_clients (client_number);

4) The primary key is COPY_D_CLIENTS_PK and the foreign key is COPY_D_EVENTS_FK
5) ALTER TABLE copy_d_clients DROP CONSTRAINT copy_d_clients_pk;
6) The foreign key references a client number in copy_d_clients and the referential integrity is enforced by the copy_d_events_fk constraint
7) DIsabling the primary key allows duplicate or null values in the client number column
8) Error on Oracle Apex. Need to fix the foreign key before using the INSERT command
9) ALTER TABLE copy_d_clients ENABLE CONSTRAINT copy_d_clients_pk;
10) ALTER TABLE copy_d_events ENABLE CONSTRAINT copy_d_events_fk;
11) Constraints may need to be disabled or re-enabled when there is data migration or testing
12) C= Check Constraint, U= Unique Constraint, R= Foreign Key, P= Primary Key
<img width="470" alt="image" src="https://github.com/user-attachments/assets/6d912e1f-5aec-4ac2-8ee1-02fcbeefd6f5">

### 15-1 Creating Views
1) Three uses are data abstraction, security, and integrity
2) <img width="465" alt="image" src="https://github.com/user-attachments/assets/a5b6e91d-9869-46ee-bdb2-8775274b0a0b">
3) <img width="461" alt="image" src="https://github.com/user-attachments/assets/99cc57b3-a6f4-43b1-b9cb-c57b1cb5ec4e">
4) <img width="428" alt="image" src="https://github.com/user-attachments/assets/24a70e1c-7a42-4b95-9452-44c27889b711">
5) <img width="468" alt="image" src="https://github.com/user-attachments/assets/fded662d-e833-4a6e-a130-32ec1cd305df">
6) <img width="455" alt="image" src="https://github.com/user-attachments/assets/36128fc9-4e01-404a-8e19-6c86a1f3a01a">

### 15-2 DML Operations and Views
1) <img width="467" alt="image" src="https://github.com/user-attachments/assets/d6a44028-8174-46ba-ba1d-020eb6912b65">
2) <img width="452" alt="image" src="https://github.com/user-attachments/assets/8b2ed59b-d3b1-4acb-af2a-459fc466d5fd">
3) <img width="467" alt="image" src="https://github.com/user-attachments/assets/1b0d4d3f-1e3e-4f84-ac86-0e664d67e005">
4) <img width="467" alt="image" src="https://github.com/user-attachments/assets/98e3eb10-8f09-47b2-b566-2023b0f8a935">
5) <img width="460" alt="image" src="https://github.com/user-attachments/assets/2c268096-a54b-4204-ac4b-100900277da1">
6) <img width="463" alt="image" src="https://github.com/user-attachments/assets/6de07d71-e266-4433-9e57-048cef0e2388">
7) <img width="416" alt="image" src="https://github.com/user-attachments/assets/0e517de2-da7d-4355-9079-59250a6e671a">
8) <img width="362" alt="image" src="https://github.com/user-attachments/assets/68ec9a78-e551-4a31-818f-c09b41145d6c">
9) <img width="467" alt="image" src="https://github.com/user-attachments/assets/39a5caad-0b40-4666-866e-9db4e5e10997">
10) <img width="466" alt="image" src="https://github.com/user-attachments/assets/ab47f7e3-3860-45d2-be77-c8d11d14a596">
11) Restrictions on modifying data through a view include the READ ONLY option, CHECK option, and non-updatable views.
12) Moore's law predicts that the number of transistors on a microchip doubles about every two years, resulting in an exponential growth. According to Google, AI doubles their computational power every six months which is much faster than technology following Moore's law. Moore's law lifespan seems to be dependent on technological advancements.  
13) Singularity is the hypotehtical future point where AI surpasses human intelligence. 

### 15-3 Managing Views
1) <img width="461" alt="image" src="https://github.com/user-attachments/assets/3d65caca-84a3-4d49-8d63-a3e70b3483da">
2) <img width="469" alt="image" src="https://github.com/user-attachments/assets/5bfb7b4b-1fbc-4a93-9f86-928c0fddbbe9">
3) <img width="467" alt="image" src="https://github.com/user-attachments/assets/58608390-82eb-4ee7-a0b6-5f0481429c5f">
4) <img width="465" alt="image" src="https://github.com/user-attachments/assets/695669e6-244b-4d41-b9b3-b63da607b22e">
5) <img width="470" alt="image" src="https://github.com/user-attachments/assets/92466612-fad3-4c97-a540-36ea4bb3684e">

### 16-1 Working With Sequences
1) <img width="470" alt="image" src="https://github.com/user-attachments/assets/05c66d82-985a-4324-85e4-8d2049bec0e8">
2) <img width="437" alt="image" src="https://github.com/user-attachments/assets/0a255217-61e8-4232-9500-7335d36b8992">
3) <img width="467" alt="image" src="https://github.com/user-attachments/assets/088d7341-732b-48bd-aeca-5e8280f7e68e">
4) <img width="470" alt="image" src="https://github.com/user-attachments/assets/935d53b2-885c-45e9-b471-140564e0c943">
5) <img width="412" alt="image" src="https://github.com/user-attachments/assets/0aae0e7a-06ba-4051-8483-5ac7d21966ff">
6) Three benefits to using SEQUENCES: automatic number generation, management of unique values, and customization of sequence behavior
7) Advantages of caching sequence values: reduces the number of operations required to get sequence values and provides a pool of squence values

### 16-2 Indexes and Synonyms
1) An index is a database object that can speed up the retrieval of rows by using a pointer
2) ROWID is a base 64 string representation of the row address containing block identifier, row location in the block, and the database file identifier
3) Indexes are created automatically when a primary key or unique constraint is defined on the table
4) <img width="454" alt="image" src="https://github.com/user-attachments/assets/1da09b0c-5f4b-46b9-a4bf-beab7fafac21">
5) <img width="457" alt="image" src="https://github.com/user-attachments/assets/5e1ca245-e648-4c7a-8a3b-2e124b9d8f8f">
6) <img width="470" alt="image" src="https://github.com/user-attachments/assets/e562f4fa-b16d-4875-be9d-3a13888e1fb2">
7) <img width="368" alt="image" src="https://github.com/user-attachments/assets/2603b4dc-eb1c-482e-aa98-db2d76f4a4b0">
8) <img width="469" alt="image" src="https://github.com/user-attachments/assets/169c9855-4af1-4f5f-a81e-fd9779d92428">
9) <img width="467" alt="image" src="https://github.com/user-attachments/assets/24ca356f-c6ab-46ea-ad93-f5b95d4d5ff7">
10) <img width="460" alt="image" src="https://github.com/user-attachments/assets/dcb0cc77-fe1f-4e85-8249-e20633ddb571">

### 17-1 Controlling User Access
1) The ability to create or remove users, remove tables, or backup tables
2) The level of security covers access and use of the database objects and the actions users can have on those objects
3) Object privileges
4) CREATE USER scott IDENTIFIED BY tiger;
GRANT CREATE SESSION TO scott;
5) GRANT SELECT, UPDATE ON d_clients TO scott;
6) GRANT SELECT ON d_songs TO PUBLIC;
7) SELECT grantee, privilege, table_name 
FROM user_tab_privs
WHERE grantee = USER;
8) GRANT CREATE TABLE TO username;
9) GRANT SELECT ON your_table TO other_user;
10) GRANT SELECT ON copy_employees TO other_user;

### 17-2 Creating and Revoking Object Privileges
1) A role is a named group of related privileges that can be granted to a user
2) The DBA can use the GRANT function to assing the role to users and assign privileges to the role
3) GRANT SELECT ON your_table TO other_user WITH GRANT OPTION;
4) Create a ROLE and grant privileges to the role
5) 
   - CREATE ROLE manager; GRANT SELECT, INSERT, UPDATE, DELETE ON employees TO manager;
   - CREATE ROLE clerk; GRANT SELECT, INSERT ON employees TO clerk;
   - GRANT manager TO scott;
   - REVOKE DELETE ON employees FROM manager;

6) A database link is used to enable communication and data sharing between two Oracle databases.

### 17-3 Regular Expressions
1) <img width="956" alt="image" src="https://github.com/user-attachments/assets/f3e27b15-9eb3-495a-b882-ef2986c7de97">
2) <img width="599" alt="image" src="https://github.com/user-attachments/assets/5098a7c5-d027-43c2-b1f5-b27abc5b2739">
