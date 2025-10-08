Find the Solution for the following:

1. Add a table-level PRIMARY KEY constraint to the EMP table on the ID column.The
constraint should be named at creation. Name the constraint my_emp_id_pk.

USE EXPERIMENT3;
Database changed

CREATE TABLE EMP(
     EMP_ID INTEGER(6) NOT NULL,
     FIRST_NAME VARCHAR(25),
     LAST_NAME VARCHAR(25) NOT NULL,
     SALARY INTEGER(8),
     COMMISSION_PCT INTEGER(4)
     );
Query OK, 0 rows affected, 3 warnings (0.85 sec)

ALTER TABLE EMP
ADD CONSTRAINT my_emp_id_pk PRIMARY KEY EMP(EMP_ID);
Query OK, 0 rows affected (0.77 sec)
Records: 0  Duplicates: 0  Warnings: 0


![EXP 3 1](https://github.com/user-attachments/assets/d629bdfb-64bf-47bc-815e-522446208554)


2. Create a PRIMAY KEY constraint to the DEPT table using the ID colum. The constraint
should be named at creation. Name the constraint my_dept_id_pk.

CREATE TABLE DEPT(
     DEPT_ID INTEGER(6),
     DEPT_NAME VARCHAR(20),
     LOCATION VARCHAR(20),
     CONSTRAINT my_dept_id_pk PRIMARY KEY (DEPT_ID)
     );
Query OK, 0 rows affected, 1 warning (0.21 sec)


![EXP 3 2](https://github.com/user-attachments/assets/9d76dfe0-064a-4b8e-a315-38fce81c438e)


3. Add a column DEPT_ID to the EMP table. Add a foreign key reference on the EMP table
that ensures that the employee is not assigned to nonexistent deparment. Name the constraint
my_emp_dept_id_fk.

ALTER TABLE EMP
ADD COLUMN DEPT_ID INTEGER(6);
Query OK, 0 rows affected, 1 warning (0.66 sec)
Records: 0  Duplicates: 0  Warnings: 1

ALTER TABLE EMP
ADD CONSTRAINT my_emp_dept_id_fk FOREIGN KEY EMP(DEPT_ID) REFERENCES DEPT(DEPT_ID);
Query OK, 0 rows affected (0.75 sec)
Records: 0  Duplicates: 0  Warnings: 0


![EXP 3 3](https://github.com/user-attachments/assets/ad74cc71-26ae-4d6e-9b20-f5b08d50f104)


4. Modify the EMP table. Add a COMMISSION column of NUMBER data type, precision 2,
scale 2. Add a constraint to the commission column that ensures that a commission value is greater
than zero.

ALTER TABLE EMP
ADD COLUMN COMMISSION NUMERIC(2,2);
Query OK, 0 rows affected (0.68 sec)
Records: 0  Duplicates: 0  Warnings: 0

ALTER TABLE EMP
ADD CONSTRAINT com_ck CHECK (COMMISSION>0);
Query OK, 0 rows affected (0.55 sec)
Records: 0  Duplicates: 0  Warnings: 0

![EXP3 4](https://github.com/user-attachments/assets/58cf31ef-1a9a-40d8-ae97-b72065b77103)

