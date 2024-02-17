docker pull mysql                                                       // pulling image
docker run --name mysql-server -e MYSQL_ROOT_PASSWORD=13777731 -d       // start db in server
mysql server is up
for connecting to this server:
docker exec -it container_name bash
mysql -u root -p                                                        // -u use for username, our account for connecting is root, -p use for the accounts password, password is 13777731

we are connected now.

create database test1                                                   // creating database
show databases                                                          // show us our databases

use test1                                                               // I selected a db named test1
we are on test1 and we can make some changes on this db
create table users(name varchar(250), phone_number varchar(11), is_active bool); // () stores list of columns

 our table is ready now
 show tables 



 desc users    // show us details of specifed tabel  

insert query be used for add row to our tables, for example add new user to users  , its create from CRUD
insert into users (name, phone_number, is_active) values ("Hadi", 09138888888, true),
 
so we created our user and we want to see it(read from CRUD)
select * from users;    // * means all columns
select name from users; // just return users name
select name,is_active from users;
select * from users where name="sara";                  // conditional states
select * from users where name="sara" or name="ali";
select * from users where name in ("sara", "ali");

we can delete tables by drop, delete from CRUD
drop table users;
show tables;
 we have no table here

create table scores(name varchar(250), score float);
insert into scores (name,scores) values ("amir",12), ("sara",15), ("saeed",19);
select * from scores where score>15; 
select * from scores where score between 10 and 17;

update scores set score=15 where name=amir;    // update from CRUD
delete scores set score=15 where name=amir;    // delete from CRUD

primary key:
create table scores(name varchar(250), score float, id int, PRIMARY KEY(id));   // id is our primary key
add to our queries:
insert into scores (name,scores) values ("amir",12,1), ("sara",15,2), ("saeed",19,3);

for ordering autoamatically:
create table scores(name varchar(250), score float, id int auto_increment, PRIMARY KEY(id));

we use database server for managing requests from program server, when we create a query, db server puts the response in a list and send back it to us, for example list of signed in users, it may be large but mostly we need limited data for example users that signed in last week,

every time we have sorted list, we can find out nearest number to our desired number
we want the row of our tables by 10-20 indexes, instead of checking all data, we know this numbers is sorted, so we use binary search and it gives us 10-20 more easily
btree or balance tree is the structure in mysql that save sorted data.
we can use it and use indexes for easy access to data and improve performance.

every time we use index, an extra table be created for sorting which its reduce writting and deleting.
in this way we have a full database and sorted table that be created after using database, in quering at first query goes to this sorted table then goes to DB.




