-- create database exp5_db;
-- use  exp5_db;

-- CREATE TABLE Students(
--  id int unique NOT NULL,
--  Name Varchar(50) NOT NULL,
--  Email Varchar(50) ,
--  MobNO Varchar(20)
-- );

-- Insert Into Students VALUES(1 , "Prem Dogra", "premdogra@gmail.com", "7890786766"),
-- (2 , "Shivansh", "shivansh@gmail.com", "7890786766"),
-- (4 , "Om Gupta", "omgupta@gmail.com", "7890786766"),
-- (3 , "pawan Kumar" ,"pawankumar@gmail.com", "7890786766"),
-- (5 , "Anush Kumar" ,"anushkumar@gmail.com", "7890786766"),
-- (6 , "Bhupinder Mangotra" ,",mangotra@gmail.com", "7890786766"),
-- (7 , "Shagun Kattal" ,"shagun@gmail.com", "7890786766"),
-- (8 , "Amit badyal" ,"premdogra@gmail.com", "7890786766"),
-- (9 , "Akshit Mehra", "premdogra@gmail.com", "7890786766"),
-- (10 , "Rahil Sharma", "rahil@gmail.com", "7890786766");

-- CREATE TABLE Students_backup(
--  id int unique NOT NULL,
--  Name Varchar(50) NOT NULL,
--  Email Varchar(50) ,
--  MobNO Varchar(20)
-- );

-- select * from Students;
-- select * from Students_backup;

-- DELIMITER $$

-- CREATE TRIGGER T1
-- BEFORE DELETE ON Students
-- FOR EACH ROW
-- BEGIN
--     INSERT INTO Students_backup (id, Name, Email, MobNo)
--     VALUES (OLD.id, OLD.Name, OLD.Email, OLD.MobNo);
-- END $$

-- DELIMITER ;

delete from Students where id = 2;
select * from Students_backup;
