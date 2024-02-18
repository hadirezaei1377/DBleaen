we want to access the students that graduared from our university whithin last 50 years.

table students
id           primary key
university   varchar
is_graduate  bool
name         varchar

select * returns all users, its not efficient
we should have index:
index(university) and index(is-graduate)

select * from students where university=x
select * from students where university=x and is-graduate=true

now mysql keeps all student by same university in a table
when we query and tell it we want the students of Sharif, it has more easliy access.
furtheremore it keeps graduated students in another seperated table
but we want a combine query, 
ALTER table students
ADD INDEX idx_uni_grad(university,is_graduate) , this composite query says sort based on university initially then sort based on graduation



