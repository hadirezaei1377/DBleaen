Classification of databases based on usage:

1- Databases that should give us access to data as soon as possible...
This type of database is also called cache or fast access databases.
like redis or memcached.
This type of database stores data in RAM.
Accessing data that is stored in the storage, such as videos, photos, etc., of any device, is slower than accessing data from RAM, such as variables that are stored in the application.
Caches store data in RAM, so accessing them is fast.
Storage memory has more space for data storage than RAM.
The data stored in RAM is temporary and will be lost.

2-general purpose databases:

SQL and NOSQL

SQL:
has releation, based ACID rules, has tables, data is related together

NOSQL:
has more readability than SQLs 

3-elasticsearch:

Database for searching.
This database has special data structures that help to categorize data.
It allows us to divide the data on different servers and deal with less data when searching data on different servers and increase the performance of our work.

many databases by different usage may use one mysql server

we consider each application as a database and each usage of it as a table.

each rows that we add to our database has a key as primary key

Talking about the journey of a query when it is created inside a server with any programming language and sent to the mysql server, it is executed and returned.

b3 or balance tree used for sorted data in mysql, for example users which added to our tables from 2000-2010.




