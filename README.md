# HospitalDB
HospitalDB is database using for organize and management medical things in hospital .

## Notice
all phone numbers , patients , doctors , persons , everything in database is fake and not real things , The database administrator has no authority or power for any misuse of the database.

## SQL Schema Example

```sql

CREATE TABLE Patients(
PatientID INT PRIMARY KEY ,
FirstName VARCHAR (20)  ,
LastName VARCHAR (20) ,
DateOfBirth DATE ,
Gender VARCHAR (1) ,
ContactNumber INT (10) ,
EmergencyContactNumber INT (10) ,
Address VARCHAR (30) ,
InsurancePolicyNumber INT (10)
FOREIGN KEY (InsurancePolicyNumber) REFERENCES Insurance(PolicyNumber)
);

CREATE TABLE Physicians (
PhysicianID INT AUTO_INCREMENT PRIMARY KEY,
FirstName VARCHAR(100) NOT NULL,
LastName VARCHAR(100) NOT NULL,
Specialization VARCHAR(150),
ContactNumber VARCHAR(15),
Email VARCHAR(150)
);

CREATE TABLE Insurance (
PolicyNumber VARCHAR(50) PRIMARY KEY,
InsuranceName VARCHAR(150),
CoverageLimit DECIMAL(10, 2)
);

```

## ER Model
![ER Model](ERMODEL.png)
