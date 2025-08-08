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
![1](https://github.com/user-attachments/assets/bfce35cd-c883-495b-acbe-83b0132b645e)


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
![2](https://github.com/user-attachments/assets/ec4ad900-9316-4c42-b15f-35b49fab091f)


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
![3](https://github.com/user-attachments/assets/4f4ae4d7-e7e5-4257-88c4-93d3c927925c)

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
![4](https://github.com/user-attachments/assets/9eec54c9-8716-4b4b-860e-432e20f158b8)

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
![5](https://github.com/user-attachments/assets/1422e5a1-d7b5-4965-b9d4-4f72212d4059)


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
![6](https://github.com/user-attachments/assets/265924c2-da92-4b3a-b4c7-d70de5940654)
