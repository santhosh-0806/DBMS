#DBMS
1. Create MY_EMPLOYEE table with the following structure
   CREATE DATABASE EXPERIMENT2;
   USE EXPERIMENT2;
   CREATE TABLE MY_EMPLOYEE(
     ID INTEGER(4) NOT NULL,
     Last_name VARCHAR(25),
     First_name VARCHAR(25),
     Userid VARCHAR(25),
     SALARY DECIMAL(9,2)
     );

<img width="507" height="185" alt="image" src="https://github.com/user-attachments/assets/9998f832-be6a-4802-a6db-b0f6bf4b8c21" />



2.Add the first and second rows data to MY_EMPLOYEE table from the following sample
data.

  INSERT INTO MY_EMPLOYEE (ID, Last_name,First_name,Userid,SALARY) VALUES
     (1,"PATEL","RALPH","rpatel",895),
     (2,"DANCS","BETTY","bdancs",860),
     (3,"BIRI","BEN","bbiri",1100),
     (4,"NEWMAN","CHAD","Cnewman",750),
     (5,"ROPEBUR","AUDREY","aropebur",1550);

<img width="432" height="188" alt="image" src="https://github.com/user-attachments/assets/94b83b9b-e393-468b-bcb3-ed8b4cc1a093" />



3.Display the table with values.
  SELECT * FROM MY_EMPLOYEE;

<img width="432" height="188" alt="image" src="https://github.com/user-attachments/assets/889e2e89-cfe9-4aa6-98f0-3671ee00b1df" />



4.Populate the next two rows of data from the sample data. Concatenate the first letter of the
first_name with the first seven characters of the last_name to produce Userid.
  UPDATE MY_EMPLOYEE
     SET Userid = CONCAT(
     LEFT(First_name,1),
     LEFT(Last_name,7)
     )
     WHERE ID IN(1,2,3,4,5);

<img width="428" height="164" alt="image" src="https://github.com/user-attachments/assets/30c30a64-30d4-42f2-b505-928445cad675" />



5. Make the data additions permanent.
COMMIT;

<img width="292" height="56" alt="image" src="https://github.com/user-attachments/assets/54e8a877-eac8-40e3-b7f3-826bc142a50e" />



6.Change the last name of employee 3 to Drexler.
  UPDATE MY_EMPLOYEE
     SET Last_name = " Drexler"
     WHERE ID = 3;

<img width="431" height="169" alt="image" src="https://github.com/user-attachments/assets/b57d4d06-4967-45c7-a44b-13ddfaa97089" />



 UPDATE MY_EMPLOYEE
         SET Userid = CONCAT(
         LEFT(First_name,1),
         LEFT(Last_name,7)
         )
         WHERE ID IN(3);

<img width="422" height="168" alt="image" src="https://github.com/user-attachments/assets/d2d0e2ce-ceda-41ff-8ba8-8564017dd28f" />



7.Change the salary to 1000 for all the employees with a salary less than 900.
 UPDATE MY_EMPLOYEE
          SET SALARY = 1000
          WHERE SALARY<900;

<img width="423" height="161" alt="image" src="https://github.com/user-attachments/assets/f4b31be6-f3b4-49a8-b992-15e91ff28f35" />



8.Delete Betty dancs from MY _EMPLOYEE table.
DELETE FROM MY_EMPLOYEE
          WHERE ID = 2;

<img width="421" height="151" alt="image" src="https://github.com/user-attachments/assets/4b1b1696-d03c-46ef-af59-4cec1b0ee49d" />



9.Empty the fourth row of the emp table.
DELETE FROM MY_EMPLOYEE
     ORDER BY ID DESC
     LIMIT 1;

<img width="423" height="132" alt="image" src="https://github.com/user-attachments/assets/bf5bb53b-fff0-4036-acba-7e2dec67fc30" />


