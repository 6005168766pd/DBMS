-- create database exp_6;
-- use exp_6;
-- create TABLE xyz(
-- Emp_d int NOT NUll Unique,
-- Empname varchar(50),
-- Salary int 
-- );
-- select * from xyz where Emp_d=1;
-- Insert into xyz values(
--   3,"Om", 65000
--  );

-- DELIMITER //

-- CREATE PROCEDURE fetch_Employee(IN eid INT)
-- proc: BEGIN
--     DECLARE ename VARCHAR(200);
--     DECLARE esalary FLOAT;
--     DECLARE emp_count INT;

--     SELECT COUNT(*) INTO emp_count 
--     FROM xyz 
--     WHERE Emp_d = eid;

--     IF emp_count = 0 THEN
--         SELECT 'Error: Employee ID not found in database' AS Message;
--         LEAVE proc;
--     END IF;

--     SELECT Empname, salary 
--     INTO ename, esalary
--     FROM xyz 
--     WHERE Emp_d = eid;

--     SELECT ename AS Name, esalary AS Salary;

-- END //

-- DELIMITER ;

 CALL fetch_Employee(5);
