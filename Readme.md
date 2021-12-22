# 1. Create tables for the above list given
CREATE TABLE guvi(users varchar(45),codekata integer,attendance integer,topics integer,tasks integer,company_drives integer,mentors varchar(45), students_activated_courses integer,courses varchar(45));

# 2.insert at least 5 rows of values in each table
INSERT INTO guvi (users,codekata,attendance,topics,tasks,company_drives,mentors,students_activated_courses,courses) VALUES ("Somu.S",55,35,40,42,5,"Ragav",1,"Fullstack Developer"), ("Sundar.D",10,33,34,19,2,"Mariappan.S",3,"Data Scientist"), ("Goblu.K",54,34,20,65,4,"Lavish",1,"Artificial Inteligence"), ("Joe.D",200,30,30,15,0,"SaiMohan",1,"Fullstack Developer"), ("Raja.D",44,30,30,15,0,"Karthik",1,"Ethical Hacking");
![image](https://user-images.githubusercontent.com/91074732/147105265-de609bd5-cff0-4584-94ac-9e5ce0c92a32.png)

# 3. get number problems solved in codekata by combining the users
SELECT sum(codekata) as Total_solved_codekata FROM guvi
![image](https://user-images.githubusercontent.com/91074732/147105565-b42952c2-20f6-4107-ab01-54849dba6f66.png)

# 4.display the no of company drives attended by a user
select users,company_drives FROM guvi
![image](https://user-images.githubusercontent.com/91074732/147105748-2efd9543-4d07-4ae2-a453-98f5d72f901f.png)

# 5.combine and display students_activated_courses and courses for a specific user groping them based on the course
select courses,count(courses) as users,students_activated_courses from guvi group by courses order by courses desc
![image](https://user-images.githubusercontent.com/91074732/147106102-77e0d308-f7ac-4572-8a2a-0a38aab442a1.png)

# 6. list all the mentors
SELECT mentors FROM guvi
![image](https://user-images.githubusercontent.com/91074732/147106299-5871f9a6-9c0d-4578-9127-ee58eb285aae.png)

# 7. list the number of students that are assigned for a mentor
select mentors,count(users) as students from guvi group by mentors order by students
![image](https://user-images.githubusercontent.com/91074732/147106522-7c0ba143-03de-41a8-8cf8-7d804491fe1c.png)
