# MySQL-Lab2 :heavy_check_mark:

### Try to create the following Queries:

   #### :small_blue_diamond: 1. Display all the employees Data.
      
	      SELECT * from employee;
		
   #### :small_blue_diamond: 2. Display the employee First name, last name, Salary and Department number.
    
        SELECT Fname, Lname, Salary, DNO from employee;
           
   #### :small_blue_diamond: 3. If you know that the company policy is to pay an annual commission for each employee with specific percent equals 10% of              his/her annual salary .Display each employee full name and his annual commission in an ANNUAL COMM column (alias).
    
           
           SELECT CONCAT(Fname,Lname)AS FullName, Salary*12*0.10 AS ANNUALCOMM
           FROM employee;

   #### :small_blue_diamond: 4. Display the employees Id, name who earns more than 1000 LE monthly.

           SELECT CONCAT(Fname,Lname)AS FullName, SSN 
           FROM employee 
           WHERE Salary > 1000;

   #### :small_blue_diamond: 5. Display the employees Id, name who earns more than 10000 LE annually.
    
          SELECT CONCAT(Fname,Lname)AS FullName, SSN 
          FROM employee
          WHERE Salary*12 > 10000;

   #### :small_blue_diamond: 6. Display the names and salaries of the female employees 
    
        select CONCAT(Fname,Lname)AS FullName, Salary 
        from employee 
        WHERE Gender = 'F';
		
   #### :small_blue_diamond: b7. Display each department id, name which managed by a manager with id equals 968574.

          select Dnum, Dname from departments	
          where MGRSSN = 968574;
       	
   #### :small_blue_diamond: 8. Dispaly the ids, names and locations of  the pojects which controled with department 10.

          SELECT Pnumber, Pname, Plocation from project 
          WHERE Dnum = 10;
