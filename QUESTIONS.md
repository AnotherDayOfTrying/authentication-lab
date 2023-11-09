# CMPUT 404 Lab 8

## Question 1: What authentication scheme is used by default in Django Rest Framework's browse-able API? How is this managed?

Basic and Session Authentication. Managed in settings.py file in `REST_FRAMEWORK.DEFAULT_AUTHENTICATION_CLASSES`.


## Question 2: What authentication scheme is used by httpie when querying with the -a or --auth option flag?

Uses basic authentication

## Question 3: What is the difference between Session Authentication and Token Authentication? How is Token Authentication an improvement over Basic Authentication?

Difference:
    - Session requires the server to store the session (requires state)

Token:
    Advantages
    - fine-grained access
    - expiry date
    - revocation
    - stateless
    
    Disadvantages
    - complicated

Session:
    Advantages
    - server tracks session id
    - do not need to manually send token on each request, session is stored as a cookie in browser

    Disadvantages
    - session tracking can get complicated (e.g. on distributed servers need to share session w/ servers)
    stateful



## Question 4: Provide a high level summary of what happens during an OAuth2 authentication flow. For instance: bitbucket.org > Log In > Log in with Google. What happens when I click "Log in with Google"?

Authenticate a service using a another service.

photo.com -> Log In -> Redirect to Log In w/ Google > Enter credentials > Client gets shared authorization ID w/ photo.com > client uses authentication ID to get an authentication token > authentication token verifies user is authenticated with photo.com

## Question 5: Please provide a link to your code.

https://github.com/AnotherDayOfTrying/authentication-lab