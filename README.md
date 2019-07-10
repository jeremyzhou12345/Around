# Around

Apply our servers on GAE(on cloud servers which can avoid local machine and balance load). Install ElasticSearch on GCE(virtual machine).

Use BigTable to store non-relational data(User,Location), while use dataflow and BigQuery to deal with relational data. Store unstructured data(file,images) to Google Cloud Storage

Use Machine Learning to analyse data. 

app.yaml: 
to tell google that your program is a go program and use go compiler to run it.
When running on Google App Engine, flexible environment automatically balance the load

Add Token-Based Authentication when users post and search posts: 
use jwt to protect post and search endpoints (reject if without auth token)

How it works: Once login credentials(username+password) is verified, a signed token is returned to the client. Subsequent requests include this token to the servers, servers decodes the JWT and if token is correct, it then process the requests.

Implement signup http requests:
Given a User json data, if user information format is valid, and there is no this user, save the user into index of ElasticSearch

Implement login http requests:
Given a User json data, if user exists and password matches, Set token claims and sign the token with secret key. Finally return the token back so that we can use token to pass authentication

