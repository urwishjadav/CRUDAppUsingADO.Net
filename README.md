# CRUDAppUsingADO.Net
Its a dotnet core project where I build CRUD (Create ,Read ,Update ,Delete) functionality using ADO .Net with use of Storeded Procedure.I mentioned stored procedure for all the logic below it is for your reference.

create database CrudADOdb;

create table Employees
(
Id int primary key identity,
name varchar(50) not null,
gender varchar(50) not null,
age int not null,
designation varchar(50) not null,
city varchar(50) not null
);

Go
CREATE PROCEDURE spAddEmployee
(
@name varchar(50),
@gender varchar(50),
@age int,
@designation varchar(50),
@city varchar(50)
)
as
Begin
	Insert into Employees (name,gender,age,designation,city)
	values(@name,@gender,@age,@designation,@city)
End

Go
CREATE PROCEDURE spUpdateEmployee
(
@Id int,
@name varchar(50),
@gender varchar(50),
@age int,
@designation varchar(50),
@city varchar(50)
)
as
Begin
	Update Employees set name = @name, gender = @gender,
	age = @age, designation = @designation, city = @city
	where id = @Id
End

Go
CREATE PROCEDURE spDeleteEmployee
(
@Id int
)
as
Begin
	Delete from Employees where id = @Id
End

Go
CREATE PROCEDURE spGetAllEmployee
as
Begin
	select * from Employees order by id
End


-----------------------------------------------------------------------
#DotNetDeveloper
#CRUDApplication
#ADONET
#DotNetProjects
#DatabaseManagement
#SoftwareDevelopment
#CodeQuality
#SQL
#StoredProcedure
#MVC
#CRUD
#FullStackDevelopment
#BackendDevelopment
#DataAccessLayer
#CodeRepository
#GitHubProjects
#EnterpriseApplication
#TechCommunity
#CodingBestPractices
