# DBMS
Experiment No: 1
1. Create the DEPT table based on the DEPARTMENT following the table instance chart
below. Confirm that the table is created.
CREATE TABLE DEPARTMENT(
     DEPT_ID INTEGER(6) NOT NULL,
     DEPT_NAME VARCHAR(20) NOT NULL,
     MANAGER_ID INTEGER(6),
     LOCATION INTEGER(4)
     );
ALTER TABLE DEPARTMENT
MODIFY DEPT_ID INTEGER(7);

ALTER TABLE DEPARTMENT
MODIFY DEPT_NAME VARCHAR(25);

+------------+-------------+------+-----+---------+-------+
| Field      | Type        | Null | Key | Default | Extra |
+------------+-------------+------+-----+---------+-------+
| DEPT_ID    | int         | NO   | PRI | NULL    |       |
| DEPT_NAME  | varchar(25) | YES  |     | NULL    |       |
| MANAGER_ID | int         | YES  |     | NULL    |       |
| LOCATION   | int         | YES  |     | NULL    |       |
+------------+-------------+------+-----+---------+-------+



2. Create the EMP table based on the following instance chart. Confirm that the table is
created.
CREATE TABLE EMP(
     ID VARCHAR(6),
     FIRST_NAME VARCHAR(20),
     LAST_NAME VARCHAR(20) NOT NULL,
     DEPT_ID VARCHAR(4)
     );
+------------+-------------+------+-----+---------+-------+
| Field      | Type        | Null | Key | Default | Extra |
+------------+-------------+------+-----+---------+-------+
| ID         | varchar(6)  | YES  |     | NULL    |       |
| FIRST_NAME | varchar(20) | YES  |     | NULL    |       |
| LAST_NAME  | varchar(20) | NO   |     | NULL    |       |
| DEPT_ID    | varchar(4)  | YES  |     | NULL    |       |
+------------+-------------+------+-----+---------+-------+

3. Modify the EMP table to allow for longer employee last names. Confirm the
modification.(Hint: Increase the size to 50)
 ALTER TABLE EMP
 MODIFY LAST_NAME VARCHAR(50);

+------------+-------------+------+-----+---------+-------+
| Field      | Type        | Null | Key | Default | Extra |
+------------+-------------+------+-----+---------+-------+
| ID         | varchar(6)  | YES  |     | NULL    |       |
| FIRST_NAME | varchar(20) | YES  |     | NULL    |       |
| LAST_NAME  | varchar(50) | YES  |     | NULL    |       |
| DEPT_ID    | varchar(4)  | YES  |     | NULL    |       |
+------------+-------------+------+-----+---------+-------+

4. Create the EMPLOYEES2 table based on the structure of EMPLOYEES table. Include
Only the Employee_id, First_name, Last_name, Salary and Dept_id coloumns. Name the columns
Id, First_name, Last_name, salary and Dept_id respectively.

CREATE TABLE EMPLOYEES2(
     ID INTEGER(6),
     FIRST_NAME VARCHAR(20),
     LAST_NAME VARCHAR(25),
     SALARY INTEGER(7),
     Dept_id VARCHAR(7)
     );
+------------+-------------+------+-----+---------+-------+
| Field      | Type        | Null | Key | Default | Extra |
+------------+-------------+------+-----+---------+-------+
| ID         | int         | YES  |     | NULL    |       |
| FIRST_NAME | varchar(20) | YES  |     | NULL    |       |
| LAST_NAME  | varchar(25) | YES  |     | NULL    |       |
| SALARY     | int         | YES  |     | NULL    |       |
| Dept_id    | varchar(7)  | YES  |     | NULL    |       |
+------------+-------------+------+-----+---------+-------+

5. Drop the EMP table.
DROP TABLE EMP;

ERROR 1146 (42S02): Table 'ltd.emp' doesn't exist

6. Rename the EMPLOYEES2 table as EMP.
RENAME EMPLOYEES2 TO EMP;

+------------+-------------+------+-----+---------+-------+
| Field      | Type        | Null | Key | Default | Extra |
+------------+-------------+------+-----+---------+-------+
| ID         | int         | YES  |     | NULL    |       |
| FIRST_NAME | varchar(20) | YES  |     | NULL    |       |
| LAST_NAME  | varchar(25) | YES  |     | NULL    |       |
| SALARY     | int         | YES  |     | NULL    |       |
| Dept_id    | varchar(7)  | YES  |     | NULL    |       |
+------------+-------------+------+-----+---------+-------+

7. Drop the First_name column from the EMP table and confirm it.
ALTER TABLE EMP
DROP ID;
+------------+-------------+------+-----+---------+-------+
| Field      | Type        | Null | Key | Default | Extra |
+------------+-------------+------+-----+---------+-------+
| FIRST_NAME | varchar(20) | YES  |     | NULL    |       |
| LAST_NAME  | varchar(25) | YES  |     | NULL    |       |
| SALARY     | int         | YES  |     | NULL    |       |
| Dept_id    | varchar(7)  | YES  |     | NULL    |       |
+------------+-------------+------+-----+---------+-------+
