# Ex. No: 4 Creating Procedures using PL/SQL

## DATE: 24.08.2023

## AIM: To create a procedure using PL/SQL.

## Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

## Program:
```
SQL> CREATE TABLE ep4(
     empid NUMBER,
     empname VARCHAR(10),
     dept VARCHAR(10),
     salary NUMBER
    );
CREATE OR REPLACE PROCEDURE emp_data AS
    BEGIN
    INSERT INTO es(empid,empname,dept,salary)
    values(1,'Eswar','MD',10000000);
    INSERT INTO es(empid,empname,dept,salary)
    values(2,'Fareed','HR',500000);
    INSERT INTO es(empid,empname,dept,salary)
    values(3,'Divya','IT',200000);
    COMMIT;
   FOR emp_rec IN (SELECT * FROM es)LOOP
   DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||
   ',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);
   END LOOP;
   END;
  /
```
  
## Output:
![dbms_exp4_1](https://github.com/Thirukaalathessvarar-S/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/121166390/8505a54f-4abb-40d3-8d66-fb9d06e10cde)

## Result:
The procedures has been successfully created using PL\SQL
