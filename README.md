

Select * from Students 
Select *from Departments 
Select * from Courses 
Select * from Enrollments 
Select * from Professors
Select*from Grades 





--1.  Retrieve all the information regarding each and every Course offered by the College
Select * from Courses 

--2. Retrieve the names of all professors in the "Professors" table.
Select Professor_Name from Professors

--3. Retrieve the location of the Biology Department on Campus 
Select department_location from Departments  where department_name = 'Biology'

- 4. Query all the students who have 'K' in their initials
Select Student_Name from Students where Student_Name like 'K%'

--5. Query all the students who have 'I' at the end of the name 
Select Student_Name from Students where Student_Name like '%I'

--6. Query all the students who have 'A'  as their initial as well as at the end of the name 
 Select Student_Name from Students where Student_Name like 'A%A'

--7. Retrieve the professor ID, name, and department name of professors who belong to the department with ID 3
 Select PRofessor_Id , professor_Name ,Department_ID  from Professors where Department_ID  = 3 

--8. Retrieve the count of the courses offered in the Department where the department Id  is '5'
 Select Count(Course_Name) as No_Of_Courses from Courses where department_Id = 5 

--9. The professor's age is the only column in the Professor Table that is missing. You are the college's administrator-head. Create a new column called "age" in the professor database and add records for it.

ALTER TABLE Professors
add  Age  int

update professors set age = 62 where professor_id = 'A1'; 
UPDATE Professors SET age = 62 WHERE professor_id = 'A2';
UPDATE Professors SET age = 47 WHERE professor_id = 'A3';
UPDATE Professors SET age = 49 WHERE professor_id = 'B4';
UPDATE Professors SET age = 65 WHERE professor_id = 'B5';
UPDATE Professors SET age = 47 WHERE professor_id = 'B6';
UPDATE Professors SET age = 54 WHERE professor_id = 'BSC7';
UPDATE Professors SET age = 45 WHERE professor_id = 'BSC8';
UPDATE Professors SET age = 45 WHERE professor_id = 'BSC9';
UPDATE Professors SET age = 47 WHERE professor_id = 'C10';
UPDATE Professors SET age = 39 WHERE professor_id = 'C11';
UPDATE Professors SET age = 45 WHERE professor_id = 'C12';
UPDATE Professors SET age = 45 WHERE professor_id = 'CS13';
UPDATE Professors SET age = 42 WHERE professor_id = 'CS14';
UPDATE Professors SET age = 43 WHERE professor_id = 'CS15';
UPDATE Professors SET age = 44 WHERE professor_id = 'D16';
UPDATE Professors SET age = 65 WHERE professor_id = 'D17';
UPDATE Professors SET age = 46 WHERE professor_id = 'D18';
UPDATE Professors SET age = 49 WHERE professor_id = 'ECO19';
UPDATE Professors SET age = 58 WHERE professor_id = 'ECO20';
UPDATE Professors SET age = 47 WHERE professor_id = 'ECO21';
UPDATE Professors SET age = 40 WHERE professor_id = 'ENG22';
UPDATE Professors SET age = 53 WHERE professor_id = 'ENG23';
UPDATE Professors SET age = 62 WHERE professor_id = 'ENG24';
UPDATE Professors SET age = 51 WHERE professor_id = 'EVS67';
UPDATE Professors SET age = 54 WHERE professor_id = 'EVS68';
UPDATE Professors SET age = 46 WHERE professor_id = 'EVS69';
UPDATE Professors SET age = 53 WHERE professor_id = 'FA28';
UPDATE Professors SET age = 39 WHERE professor_id = 'FA29';
UPDATE Professors SET age = 38 WHERE professor_id = 'FA30';
UPDATE Professors SET age = 61 WHERE professor_id = 'FS25';
UPDATE Professors SET age = 59 WHERE professor_id = 'FS26';
UPDATE Professors SET age = 61 WHERE professor_id = 'FS27';
UPDATE Professors SET age = 60 WHERE professor_id = 'G31';
UPDATE Professors SET age = 61 WHERE professor_id = 'G32';
UPDATE Professors SET age = 50 WHERE professor_id = 'G33';
UPDATE Professors SET age = 56 WHERE professor_id = 'H34';
UPDATE Professors SET age = 66 WHERE professor_id = 'H35';
UPDATE Professors SET age = 46 WHERE professor_id = 'H36';
UPDATE Professors SET age = 34 WHERE professor_id = 'J70';
UPDATE Professors SET age = 37 WHERE professor_id = 'J71';
UPDATE Professors SET age = 56 WHERE professor_id = 'J72';
UPDATE Professors SET age = 45 WHERE professor_id = 'L61';
UPDATE Professors SET age = 56 WHERE professor_id = 'L62';
UPDATE Professors SET age = 48 WHERE professor_id = 'L63';
UPDATE Professors SET age = 47 WHERE professor_id = 'M37';
UPDATE Professors SET age = 43 WHERE professor_id = 'M38';
UPDATE Professors SET age = 35 WHERE professor_id = 'M39';
UPDATE Professors SET age = 40 WHERE professor_id = 'MSC40';
UPDATE Professors SET age = 37 WHERE professor_id = 'MSC41';
UPDATE Professors SET age = 46 WHERE professor_id = 'MSC42';
UPDATE Professors SET age = 43 WHERE professor_id = 'P43';
UPDATE Professors SET age = 50 WHERE professor_id = 'P44';
UPDATE Professors SET age = 53 WHERE professor_id = 'P45';
UPDATE Professors SET age = 57 WHERE professor_id = 'PH46';
UPDATE Professors SET age = 59 WHERE professor_id = 'PH47';
UPDATE Professors SET age = 60 WHERE professor_id = 'PH48';
UPDATE Professors SET age = 45 WHERE professor_id = 'PSC49';
UPDATE Professors SET age = 47 WHERE professor_id = 'PSC50';
UPDATE Professors SET age = 56 WHERE professor_id = 'PSC51';
UPDATE Professors SET age = 47 WHERE professor_id = 'PSY52';
UPDATE Professors SET age = 49 WHERE professor_id = 'PSY53';
UPDATE Professors SET age = 48 WHERE professor_id = 'PSY54';
UPDATE Professors SET age = 58 WHERE professor_id = 'S55';
UPDATE Professors SET age = 57 WHERE professor_id = 'S56';
UPDATE Professors SET age = 47 WHERE professor_id = 'S57';
UPDATE Professors SET age = 49 WHERE professor_id = 'ST73';
UPDATE Professors SET age = 59 WHERE professor_id = 'ST74';
UPDATE Professors SET age = 57 WHERE professor_id = 'ST75';
UPDATE Professors SET age = 55 WHERE professor_id = 'SW64';
UPDATE Professors SET age = 43 WHERE professor_id = 'SW65';
UPDATE Professors SET age = 39 WHERE professor_id = 'SW66';
UPDATE Professors SET age = 54 WHERE professor_id = 'T58';
UPDATE Professors SET age = 60 WHERE professor_id = 'T59';
UPDATE Professors SET age = 62 WHERE professor_id = 'T60';

--10.  What is the age of oldest Professor in the college 
Select  MAX(Age) as Oldest_Age  from Professors 

--11.  What is the average age of all professors in the college 
Select  AVG(Age) as AVG_Age  from Professors 

--12.  What is the age of youngest Professor in the college 
Select  MIN(Age) as Youngest_Age  from Professors 

--13. What is the age gap between the oldest and youngest professor 
Select (MAx(Age) - Min(Age)) as Age_Difference  from Professors

--14. How Many of the Students enroll in the month of June
Select count(Student_id)as No_of_Students_enroll from Enrollments where month(enrollment_date) = 6

--15. How many students recieve the respective grades :O,A,B,C,D and F

Select Count(Grade) as O_Grade from Grades where grade = 'O'
Select Count(Grade) as A_Grade from Grades where grade = 'A'
Select Count(Grade)as B_Grade from Grades where grade = 'B'
Select Count(Grade) as C_Grade from Grades where grade = 'C'
Select Count(Grade)  as D_Grade from Grades where grade = 'D'
Select Count(Grade) as F_Grade from Grades where grade = 'F'


--16. Query the all information of each students who not opted Music 
Select* from Students where not  student_major = 'Music'

--17. Retrieve professor Name who are above the age of 50 
Select Professor_Name from Professors  where Age > 50 

--18. As you are the college's administrative head, and your department is having trouble sorting the names of all the students who have applied to the college this year because they all have their full names in the same column.
--Split First Name and Last Name into two separate columns and display them in the Students tables.

Select Student_Name, 
Substring(Student_Name,1,(CHARINDEX(' ',Student_Name)-1)) as First_Name,
 Substring(Student_Name,
 LEN(Substring(Student_Name,1,(CHARINDEX(' ',Student_Name)+1)))
 ,LEN(Student_Name)) as Last_Name
 from Students 

--19. Find out how many days did the college recieved application for the enrollment
Select Abs(datediff(DD,MAX(Enrollment_date),MIN(Enrollment_date))) as No_Of_Days from Enrollments

--20. Retrieve all the Professors Name with their respective Department 

Select P.professor_name , D.department_name
from Professors as p
join Departments as D  on P.department_id = D.department_id

-- 21. Query the name of Students and course taken by them in the college

Select Student_name,Course_Name
from Students  as S 
join Enrollments as E on S.student_id = E.Student_Id
join Courses as   C  on  E.Course_ID = C.Course_ID

--22. Retrieve all course data in related to each and every departments whether they belong  to it or not.Also sort them in right order

Select  D.department_id,D.department_name,C.course_id,C.course_name
from Departments as D 
left join Courses as C  on  C.department_id = D.department_id
order by D.department_id


--23.The results of the first semester's examinations and practicals are now released. Students are concerned about their exam performance. Kindly assist everyone in viewing their First Semester results.

Select S.Student_name , G.Grade
from 
Students as S 
join enrollments as E on S.student_ID = E.Student_ID
join Grades as G  on E.enrollment_id = G.enrollment_id


--24. Every email in the professors' table has a personal domain.Please substitute it to  "@MountBridge.com " (College Official Email) for their professional usage.
Select 
REPLACE(professor_email,'@example.com','@MountBridge.com') as Official_Email
from Professors


-- 25. Letting students view their results from the first semester was a terrific job that you performed. Even though the majority of Students  did very well. There were some students who failed the exam.Every piece of information
-- regarding the students who failed the first semester exams is required by the college administration department. 

Select S.*, E.enrollment_id,E.enrollment_date,C.course_id,C.course_name,C.course_credits
from Students as S 
left join enrollments as E on S.student_ID = E.Student_ID
left join Courses as C on C.course_id = E.course_id
left join Grades as G  on E.enrollment_id = G.enrollment_id
where G.Grade = 'F'




--26. College Admin Department wants to know how many students were failed in which department 

Select S.student_major,Count(S.student_name) as No_Of_Students_Failed 
from 
Students as S 
 left join enrollments as E on S.student_ID = E.Student_ID
 left join Grades as G  on E.enrollment_id = G.enrollment_id
group by S.student_major, G.Grade
having  G.Grade = 'F'  





-- 27. The college administration department neglected to include remarks on the grades they were given.Assist the college administration department to categorise students based on the grades they received.

Select S.Student_Id,S.Student_Name,S.Student_Major,G.Grade,
case 
when Grade = 'O' then 'Outstanding'
when Grade = 'A' then 'Very Good'
when Grade = 'B' then 'Good'
when Grade = 'C' then 'Above Average'
when Grade = 'D' then 'Average'
else 'Fail' 
end as Remarks
from Grades as G 
join enrollments as E on E.enrollment_id = G.enrollment_id
join Students as S on S.student_ID = E.Student_ID
 order by S.student_major




 --28. Professors have asked the college admin department for information on which students in their own teaching department failed. Please give the names of all the students to each professor who failed the first semester exams in their teaching major  

 With CTE1 as 
(Select S.student_major,S.student_name as Students_Failed 
from 
Students as S 
join enrollments as E on S.student_ID = E.Student_ID
join Grades as G  on E.enrollment_id = G.enrollment_id
where   G.Grade = 'F')
Select P.Professor_Name,C.* from Professors as P
join Departments as D on P.department_id = D.department_id
join CTE1 as C  on D.department_name = C.student_major



-- 29. 'Ravi Patel', 'Neha Kapoor', 'Vikram Malhotra', and 'Nikhil Menon' are professors who find it difficult to comprehend the data because it is populated with numerous students. Kindly assist the individual professors by ensuring that they
--only collect information from students who are enrolled in courses related to their areas of expertise.

Create view  Anthropology
As
Select * from Students where student_major = 'Anthropology' 
Select * from Anthropology

Create view  Economics
As
Select * from Students where student_major = 'Economics' 
Select * from Economics

Create view  Physics
As
Select * from Students where student_major = 'Physics' 
Select * from Physics

Create view  Political_Science
As
Select * from Students where student_major = 'Political Science' 
Select * from Political_Science



--30. The college administration department made a mistake when revising results since they reported an "O" grade rather than an "E," 
--which the college should have given and which is referred to as "Excellent." Create a procedure to replace any grades that contain "O" with "E."

Create procedure updated_result
As
Update grades 
set Grade= 'E' where Grade = 'O'
GO

Exec updated_result


--31. Calculate the average age for each professors with respective to their departments.

Select  P.professor_name, D.department_name,P.Age,
avg(Age) over (partition by department_name ) as Avg_Age 
from Professors as P 
join Departments as D 
on P.department_id = D.department_id



--32. Even though you did a fantastic job earlier, all professors now simply want information on their students only.Due to the numerous departments, creating a view can be difficult. Instead, come up with a different solution to the problem so the professor won't
--complain again and the college administration department won't be under as much stress.  

Create Procedure Student_Info @Stud varchar(50)
As
Select S.* ,C.course_id,C.course_name,G.Grade
from Students as S 
join Enrollments as E on E.student_id = S.student_id
join Grades as G on E.enrollment_id = G.enrollment_id
join Courses as C on C.course_id = E.course_id
where @stud = student_major
GO

Exec Student_Info @Stud = 'Computer Science '








