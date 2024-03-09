group requests for getting into use less resources and process more requests per second.
we use some services between clients and db services, these services manage requests and provide reach to hot db.

in fact this middle service classify the requests, compine that and try to send that to db services in ordered.
this is combined usage like upsert .