  <h2><i><b>Idea behind ProjectsAdda<b></i></h2>
  <p>Any student wants to learn How projects are build and how to Work with Hardware and Software components then he or she needs some Guide or they need to know how to build    a project .</p>
<p>This platfrom provoide both.i.e projects and training</p>

<h2><i>ProjectsAdda DataBase Querys</i></h2>
<h3>CreateDataBase Query</h3>
<p>create database ProjectsAdda</p>
<h3>Use CreatedDataBase Query</h3>
  <p>use ProjectsAdda</p>

<h3><i>Table Stucture</i></h3>
<hr>
<h3><i>StudentDetails Table</i></h3>
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
<h3><i>TrainerDetails Table structure</i></h3>
  
Create Table TrainerDetails(
<br>
TrainerId int identity(1,1) primary key,
<br>
TrainerName Varchar(50) not null,
<br>
TrainerPhoneNumber varchar(10) not null,
<br>
TrainerAddress varchar(80) not null,
<br>
TrainerAvilability DateTime not null,
<br>
ExpectedDateOfComplition Date not null,
  <br>
StudentId int,
<br>
  PriceId int,
  <br>
FOREIGN KEY (StudentId) REFERENCES StudentDetails(StudentId)
<br>
  FOREIGN KEY (PriceId) REFERENCES Price(PriceId)
  <br>
);
<hr>
  
  
  <h2>Price Table</h2> 
  create table Price(
  <br>
PriceId int Identity(1,1) primary key,
    <br>
TrainerFee money,
    <br>
HardwareCost money,
    <br>
softwareCost money,
    <br>
GST money
    <br>
);
  <hr>
  <hr>

<br>
<h2>Select statement</h2>
<hr>
select * from StudentDetails;
<br>
select * from TrainerDetails;
<br>


<h2>drop statemet</h2>
drop table StudentDetails;
<br>
drop table TrainerDetails;
<br>
<br>
<h2>Insert statement</h2>
insert into StudentDetails values('Goutam','9481248849','Malavalli po:Bare tq:yellapur Uttarakanada 581337','WaterLevelDetector','When water level fall it should indicate','12/02/2022');
<br>
<br>
insert into StudentDetails values('Ganesh','9481248849','Malavalli po:Bare tq:yellapur Uttarakanada 581337','WaterLevelDetector','When water level fall it should indicate','12/02/2022');
<br><br>
insert into TrainerDetails values('Mukesh','866005699','mumbi','12/02/2333 9:20','2/03/2333',1);
<br><br>
  insert into Price values(200,200,200,200);
  <br>

<h2>Join Statement(ON StudentDetail & TrainerDetails Tables)</h2>
  

select StudentName,StudentPhoneNumber,TrainerName from StudentDetails ;
  
  <br>
  <h2>Join Three table Query</h2>
  <p>select StudentName,StudentPhoneNumber,TrainerName,Price.TrainerFee from StudentDetails 
inner join TrainerDetails ON StudentDetails.StudentId = TrainerDetails.TrainerId 
    inner join  Price ON Price.PriceId=TrainerDetails.TrainerId
inner join TrainerDetails ON StudentDetails.StudentId = TrainerDetails.TrainerId ;</p>
  <br>

<br><br>
