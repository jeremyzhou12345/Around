# Around

/************   July 7th         **********/

Add Token-Based Authentication when users post and search posts: 
use jwt to protect post and search endpoints (reject if without auth token)

How it works: Once login credentials(username+password) is verified, a signed token is returned to the client. Subsequent requests include this token to the servers, servers decodes the JWT and if token is correct, it then process the requests.

Implement signup http requests:
Given a User json data, if user information format is valid, and there is no this user, save the user into index of ElasticSearch

Implement login http requests:
Given a User json data, if user exists and password matches, Set token claims and sign the token with secret key. Finally return the token back so that we can use token to pass authentication

