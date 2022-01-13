<h1>Idea behind ProjectsAdda</h1>
<p>Any student wants to learn How projects are build and how to Work with Hardware and Software components then he or she needs some Guide or they need to know how to build a project .</p>
<p>This platfrom provoide both.i.e projects and training</p>

<h2>ProjectsAdda DataBase Querys</h2>
<h3>CreateDataBase Query</h3>
<p>create database ProjectsAdda</p>
<h3>Use CreatedDataBase Query</h3>
use ProjectsAdda

<h3>Table Stucture</h3>
<hr>
<h3>StudentDetails Table</h3>
create table StudentDetails(
<br>
Id int identity(1,1) primary key,
<br>
StudentName Varchar(50) not null,
<br>
StudentPhoneNumber varchar(10) not null,
<br>
StudentAddress varchar(80) not null,
<br>
ProjectTitle varchar(30) not null,
<br>
ProjectDiscription varchar(8000) not null,
<br>
ExpectedDate Date not null,
<br>


);
<hr>

<br>
<h2>Select statement</h2>
select * from StudentDetails
<br><br>
<h2>drop statemet</h2>
drop table StudentDetails
<br>
<br>
<h2>Insert statement</h2>
insert into StudentDetails values('Goutam','9481248849','Malavalli po:Bare tq:yellapur Uttarakanada 581337','WaterLevelDetector','When water level fall it should indicate','12/02/2022');
<br><br>
insert into StudentDetails values('Ganesh','9481248849','Malavalli po:Bare tq:yellapur Uttarakanada 581337','WaterLevelDetector','When water level fall it should indicate','12/02/2022');
