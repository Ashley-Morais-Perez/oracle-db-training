# Oracle HW Sections 5 and 6 #

## Section 5-1 and 5-2 ## 

I had issues with completing the logical and regional models in Oracle SLQ because there's an issue with my authenticator account. I've submitted the help ticket, so hopefully this doesn't happen in the future. 

<img width="715" alt="image" src="https://github.com/user-attachments/assets/2eed8b0b-48ec-42f3-b40c-5a2c5b766a3d">


## Section 6-1 and 6-2 ##

The task was to read about Oracle APEX. Since my Oracle Cloud isn't working, I just read what was available online. In general, it seems that APEX uses AI to aid with app developemnt. 

## Sectopm 6-3 ##

For this section, using the APEX I should have been able to create tables. I tried formatting some of the syntax used in the slides here:

- ALTER Table Academic Database ADD (Parent Information [first name], Parent Information [last name], Parent Information [ID#])
  
- ALTER Table Academic Database ADD (Student [ID#], Student [First Name], Student [Last Name], Student [Registration Year], Student [Email])
  
- ALTER Table Academic Database ADD (Studen Attendance [Working Days], Student Attendance [Days Off], Student Attendance [Eligibility for Exam])
  
- ALTER Table Academic Database ADD (Student Course Detail [Grade])
  
- ALTER Table Academic Database ADD (Academic Session [#ID], Academic Session [Name])
  
- ALTER Table Academic Database ADD (Department [#ID], Department [Name], Department [Head])
  
- ALTER Table Academic Database ADD (Exam Result [Grade])
  
- ALTER Table Academic Database ADD (Exam Type [#Type], Exam Type [Name], Exam Type [Description])
  
- ALTER Table Academic Database ADD (Faculty [#ID], Factuly [First Name], Faculty [Last Name])

## Section 6-4 ##

For this section, the practice involved inserting rows into the tables created using more DDL syntax

- INSERT INTO Academic Database Student (ID#, First name, Last name, Registration Year, Email) VALUES (720, Jack, Smith, 01-Jan-2012, Jsmith@school.edu)
  
- INSERT INTO Academic Database Exam Type (#type, Name, Description) VALUES (MCE, Multiple Choice Exams, Choose More Than One Answer)

- INSERT INTO Academic Database Faculty (#ID, First Name, Last Name) VALUES (800, Jill, Miller)

- Insert INTO ACADEMIC DATABASE Student Attendance (Working Days, Days Off, Eligibility for Exam) VALUE (180, 11, Y)

## Section 6-5 ##

1) Yes, the new email field would still be there since there was a savepoint created
2) Everything up to being deleted would remain on the table. If there's a rollback to UPDATE_DONE then it would remove the DELETE_DONE savepoint

## Section 6-6 ##

1) SELECT Studnet #ID, Studnet First name FROM Academic Database
2) SELECT Exam Result, Exam Studnet #ID FROM Academic Database
3) DESCRIBE Faculty
4) SELECT Studnet Attendance, Eligibility for Exam (Y) FROM Academic Database

