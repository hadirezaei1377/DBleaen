we can determine some DB from main DB as copy and when requests grow up, use those and scale out our database .
for example instead on serving 3 request by DB we serve 9 request by 3 copy of DB.
changes in each db must be done in others,  
consistency : each requests to each DB must has same response.
for example a user requests to one of that db and see the content doesnt exist, he sends the request again and in the another DB the content exists.
it depends on the processing number in each db.
it was the definition of inconsistency.

types of consistency:

strong consistency:
for example we have a main DB for finantial and other DB read from that, it must done imadiatly on all DB .

eventual consistency:
by low pressure on system changes be update in varous times, for example thing by low importance like changing profile picture may occure 5 minutes.
no need to change instantly.
here we use queues.