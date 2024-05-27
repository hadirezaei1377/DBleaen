some times our task doesnt implement by one query and we need to submit several queries.

for example moving money from an account to another account, first of all we need to 1- check amount in first account 2-pick up from first account and 3-save the money in second account.

in each steps may have error and operation be stoped.
transactions help us to solve this problem.

start transaction ---> start transaction (as a query)
for example less a number from a table, 
if we enter a query we see no change in each table (atomic property)
if we enter commit, changes be done in both tables.
and by rolleback we could send the changes back