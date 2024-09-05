# SQL: Database Foundations: Sections 1, 2, 3, 4 : Intro, Modeling, Data Modeler
## Section 1-2
Q1) Data that would need to be collected for student registration: student's full name, DOB, area of residence, 
parent/guardian, transcripts of previous schools

Q2) Data for library management system: book title, author name, author ID, genre, customer library number, customer name, check-in and check-out dates, availability of the book

## Section 1-3
Q1) a- hierarchal model, b- network model, c- object-orient model, d- relational model, e- flat file model

## Section 1-4
Q1) 
- Business Rule: Members will pay membership fees. Students are free. 
- Constraints: Members can belong to corporate, student, or individual. Memberships can be changed only if the justification provided is approved 

Q2) 
- Business Rule: Doctor's ID are assigned with 'DC'. Patient's ID are assigned with 'PT'
- Constraint: Doctors must have worked at the hospital for at least 7 years. Patients must register upon their first visit

## Section 2-1
Q1) Relational Database Table and Associated Fields:
- Books: Title, ISBN, year, price
- Author: name, address, URL, associated book
- Publisher: name, address, phone number, URL, associated book
- Warehouse: code, address, phone number, book inventory
- Bookstore: customer name, customer ID, customer address
- Website: customer shopping cart ID, account number, customer transaction information

Q2) Relational Database Table and Associated Fields: 
- Customers: order number, item request, quantity of item, invoice, payment/account balance
- ABC Warehouse: inventory of each item, product details, reorder level, preferred supplier

## Section 2-2
Q1) A conceptual model: addresses the current needs of the business, captures functional and informational needs, may reflect future needs, portrays the 'client's dream', helps see the overall concept of how entities may relate to each other

Q2) Ex 1: A database is needed for beauty products in a store. The conceptual model will identify the different entities such as product, vendor, and customer. The physical table simplifies it by turning the entities into tables. Ex 2: The conceptual model will identify the relationship between the customers and the product. The physical model will simplify this by adding foreign keys like CUSTOMER_PK(Customer_id) 
## Section 2-3
Q1) Entities: School, Student, Course, Academic Session, Department, Exam

Q2) 
- Course: name, course ID
- Department: faculty, department name
- Student: full name, DOB, contact information
- Faculty: individual name, contact information, courses taught
- Academic Session: start and end date, course information
- Parent Information: parent name, contact information, relation to student
- Exam: associated course, grade threshold 

## Section 2-4
Q1) A unique identifier could be the title of the song

Q2) Studnet ID number 

Q3) Student- ID number, Movie- Title, Locker- Number

Q4) A Unique identifier for the Academic Database ERD could be the Studnet ID number. The candidate's unique identifiers could be student email

## Section 2-5
Q1) b

Q2) Rules: 
- A person must be born in one and only one town. A town may be the birthplace of one or more person
- A person must be living in one and only one town. A town may be the hometown of one or more person
- A person may visit one or more towns. A town must be visited by one and only one person
- A person may be the mayor of one or more towns. The town may be governed by one or more persons

Q3) Rules:
- An exam must be assigned to one and only one student. A student may be assigned to one or more exams
- A student must be assigned to one and only one academic session. An academic session may be assigned to one or more students
- Parent information may be connected to one or more students. A student must be connected to one and only one set of parent information
- Faculty may be working under one or more departments. The department may contain one or more faculty 

## Section 2-6
Q1) Entites: Supervisor, Employee, Department, Project. Attributes: employee ID number, unique project number, supervisor name

Q2) A HAIRSTYLIST may see one or more clients (optional). A CLIENT may see one or more HAIRSTYLIST (optional). Hairstylist attributes: full name, SS number, phone number, salary, address. Client attributes: full name, phone number

Q3) 
- A TEACHER may teach one or more COURSES (optional). A COURSE may be assigned to one or more TEACHERS (optional).
- A TEACHER may teach one or more CLASS (optional). A CLASS must be taught by one and only one TEACHER (mandatory).
- Attributes: teacher full name, teacher contact info, course code, class name, class location, class time

## Section 3-1
Q1) Relationship between COURSE and STUDNET could be TEACHER

Q2) Relationship between FACTULY and COURSE could be DEPARTMENT

Q3) Relationship between STUDNET, EXAM, and COURSE could be DEPARTMENT

Q4) A STUDNET must be assigned to one and only one EXAM RESULT. The EXAM RESULT must be assigned to one and only one STUDNET

Q5) Supertype: Faculty Subtype: Teacher, Principal, Custodian, Nurse, Secretary

Q6) Course is the supertype and ONLINE and SEATED are the subtype in the arc

Q7) Hierarchy: Hotel (UID: name) --> floors (UID: floor number) --> Suites (UID: suite number) --> Rooms (UID: room number)

Q8) Hierarchical Structure: Company --> Sales Regions --> Districts --> Sales Directors--> Territories --> Sales Manager--> Areas --> Salesperson 

Recursive Structure: A salesperson may be managed by one and only one sales manager. A sales manager may be the manager of one or more salespersons

Q9) Supertype: Rental Company  Subtypes: Rental offices, vehicles, customers  

## Section 3-2
Q1) The Grade Retake History would be the relationship between Student and Course

Q2) The UID of assignment is the start time since no other class or exam should be starting at the same time. Three constraints would be that there must be one time for the exam, one time for the class, and the start time must be unique for each date. 

## Section 3-3
Q1) TO bring the table to first normal form, the colors would need to have different Item ID and Unit price

Q2) To bring the table to second normal form, the location should be moved to Store ID

Q3) To bring the table to third normal form, the Category Description should be moved to a separate entity 

Q3) For student, you can move out the number working days and days off to a separate entity which would be third normal form


## Section 3-4
Q1) 1-a, 2-f, 3-c, 4-e, 5-d, 6-b, 7-g

Q2) pk- primary key, fk- foreign key, uk- unique key, *- mandatory column, o- optional column

Q3) Authors- autr, Publishers- pblr, Customers- cstmr

Q4) Song attribute: title, release date, first name, last name, type 

Event Attribute: title, description, venue, phone number, email address

Customer: first name, last name, phone number, email address 
