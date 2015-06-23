# rest-example

Simple REST example that to show how Github API works and all documentation about can be find on the https://developer.github.com/v3

This really simple example just explain how REST API works and we can contextualize some ROA (Resource Oriented Architecture) concepts.

        addressability
        connectedness
        uniform interface
        statelessness
        Safety 
        Idempotence

1 - Showing a user and user projects (using the GET HTTP method). We can see that they are just "resources"
    
    https://api.github.com/users/tuliolucas
    https://api.github.com/users/tuliolucas/repos
    
2 - Updating some user informations (this case GitHub API requires authentication and I choose the "Auth2 token" and so my property token will be sent as a parameter. My profile token is "94a7a447f7f8f4aa8c529ecc35d89125513c0154") and we are changing just my GitHub name.

    {
      "name":"Túlio Cruz"
    }
    
    https://api.github.com/user?access_token=94a7a447f7f8f4aa8c529ecc35d89125513c0154

* For this presentation we are using Advanced REST client, the web developers helper program to create and test custom HTTP requests.
