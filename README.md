# rest-example

Simple REST example that to show how Github API works and all documentation about can be find on the https://developer.github.com/v3

This really simple example just explain how REST API works and we can contextualize some ROA (Resource Oriented Architecture) concepts.

1 - Show a user and user projects resource (using the GET HTTP method)
    
    https://api.github.com/users/tuliolucas
    https://api.github.com/users/tuliolucas/repos
    
      addressability
      connectedness
      uniform interface
    
2 - Updating (using the PATCH HTTP method) some user informations and this application requires authentication and I choose the "Auth2 token" and so my property token will be sent as a parameter. My profile token is "94a7a447f7f8f4aa8c529ecc35d89125513c0154"

  We will change my name in Github account 
    {
      "name":"Túlio Cruz"
    }
    
    
    https://api.github.com/user?access_token=94a7a447f7f8f4aa8c529ecc35d89125513c0154
    
    statelessness
    Safety 
    Idempotence
    
    
    https://developer.github.com/v3/auth/#basic-authentication
    https://developer.github.com/v3/users/
    
* For this presentation we are using Advanced REST client, the web developers helper program to create and test custom HTTP requests.
