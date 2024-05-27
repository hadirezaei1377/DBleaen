Migration refers to the changes that we want to apply to the database.
Generally, relational databases need to have specific tables before starting.
Sometimes we want to add or define a schema, for example, create or edit table values
Sometimes it is necessary to seed the database.
For example, we have defined a table called users for the database, and now we want this table to contain 100 unique users.
Add data to tables = seed 
Maybe we want to migrate the data, for example, we have an old table and we want to split its data between two new tables.
ORMs help us in migration.
For example, in Go, gorm helps us to migrate.

ORM:
We must apply the business logic layer in software design.
For example, maybe the product owner will tell us that in order to register users, I need to get the users' phone numbers and confirm them.
This layer needs storage for data processing, which usually uses a database for storage.
Changing the database can disrupt the business logic of the project.
ORMs said we add an abstraction layer to the database that includes functions and methods. You add business logic to these functions and based on that I decide what database to call and how to connect to it.
Mostly used for relational databases.
It is better to use pattern repository instead of ORMs.

GORM:
In the application, for each request or any work we want to do, we must send a query from the server to the database and get the answer and process it.
In the first step, we need to create a query based on the desired table fields, in this step we need to know the table fields.
The second step is to create a connection between the application and the database.
The database has its own language and we have to talk to it based on that language.
The third step is parsing the database answer.

It is suggested to use ready-made packages for the second step.
We can do steps 1 and 3 with ready-made packages like GORM, It lowers performance.

According to this standard, we have one struct for each table.
