# Day 2 MYSQL RELATIONSHIPS (MANY-TO-MANY)
## Daily Journal
Read Dotnet WebAPI's > Relationships, and answer the following questions
## What is the difference between a primary key and a foreign key
    The primary key is a unique piece of information used to identify records on a table. A Forgein Key or FK for short is a key on a second table on a different table thant the first that references the table, usually the pk on the first table and the fk on the second table are the same.
## What is an Alias?
 An Alias is used to reference either a table or property on a table to change the name. Usually used when joining two tables to uniquely identify which id is present on a table. It also is used so the id's aren't blowing each other away.
## Demonstrate how you would query a join statement that would get all of a doctors patients from the following collections:

CREATE TABLE doctors (
  id INT NOT NULL AUTO_INCREMENT,
  -- CODE OMITTED
  PRIMARY KEY (id)
)

CREATE TABLE patients (
  id INT NOT NULL AUTO_INCREMENT,
  -- CODE OMITTED
  PRIMARY KEY (id)
)
### Table name changed by me(original name was doctors)
CREATE TABLE doctor_patients (
  id INT NOT NULL AUTO_INCREMENT,
  doctorId INT NOT NULL,
  patientId INT NOT NULL,

  FOREIGN KEY (doctorId)
    REFERENCES doctors(id),
  FOREIGN KEY (patientId)
    REFERENCES patients(id),
)
** ANSWER **
    First off the code wouldn't work because you have two tables named the same. But if the tables were named appropriately then this is what I would do.
    SELECT
    d.*,
    p.*,
    dp.id as doctorpatientId,
    dp.doctorId as doctorId,
    wp.patientId as patientId,
    FROM
    doctor_patients dp
    JOIN doctors d ON d.id = dp.doctorId
    JOIN patients p ON p.id = dp.patientId
    WHERE
    dp.doctorId = @id

## Afternoon Challenge
  https://github.com/kpohiostyle/contracted