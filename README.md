# rest-example

Exemplo de consumo de um serviço REST, utilizando a API publica do Github.

Toda documentação relacionada a esta API pode ser encontrada em "https://developer.github.com/v3".

Desta forma conseguiremos identificar os princípios fundamentais do REST,  que são:

        - Dê a todas as coisas um identificador (addressability)
        - Vincule as coisas (connectedness)
        - Utilize métodos padronizados (uniform interface)
        - Comunique sem estado (statelessness)

1) Para contextualizar, iremos fazer a requisição do recurso "tuliolucas", que representa um usuário no Github e todas as informações relacionadas.

Já pela URL de acesso ao recurso "https://api.github.com/users/tuliolucas", podemos perceber o conceito de endereçamento, que significa que foi disponibilizado um endereço que representa somente este recurso.
 
 ```
 https://api.github.com/users/tuliolucas (GET)
{
  "login": "tuliolucas",
  "id": 530063,
  "avatar_url": "https://avatars.githubusercontent.com/u/530063?v=3",
  "gravatar_id": "",
  "url": "https://api.github.com/users/tuliolucas",
  "html_url": "https://github.com/tuliolucas",
  "followers_url": "https://api.github.com/users/tuliolucas/followers",
  "following_url": "https://api.github.com/users/tuliolucas/following{/other_user}",
  "gists_url": "https://api.github.com/users/tuliolucas/gists{/gist_id}",
  "starred_url": "https://api.github.com/users/tuliolucas/starred{/owner}{/repo}",
  "subscriptions_url": "https://api.github.com/users/tuliolucas/subscriptions",
  "organizations_url": "https://api.github.com/users/tuliolucas/orgs",
  "repos_url": "https://api.github.com/users/tuliolucas/repos",
  "events_url": "https://api.github.com/users/tuliolucas/events{/privacy}",
  "received_events_url": "https://api.github.com/users/tuliolucas/received_events",
  "type": "User",
  "site_admin": false,
  "name": "Túlio Cruz",
  "company": "",
  "blog": "",
  "location": "",
  "email": "tuliolucas.silva@gmail.com",
  "hireable": false,
  "bio": null,
  "public_repos": 6,
  "public_gists": 0,
  "followers": 2,
  "following": 2,
  "created_at": "2010-12-20T02:57:34Z",
  "updated_at": "2015-06-23T04:24:38Z"
} 
```

2) O segundo exemplo iremos atualizar informações relacionadas ao recurso, tuliolucas. 

De acordo com a documentação os dados, do recurso usuário, que podem ser alterados são: 

        - name 
        - email 
        - blog 
        - company 
        - location 
        - hireable (available for hire)
        - bio.

Este tipo de solicitação de alteração de um recurso ou exibição de informações sensíveis, a API utiliza o protocolo de autenticação OAuth2. Para nosso exemplo utilizaremos o OAuth2 com a utilização de TOKEN, https://github.com/settings/tokens.

    https://api.github.com/user?access_token=ed3231abe893f9c4a5c45642085722d456c62b95 (PATCH)
    
    Conteúdo

    {
      "name":"Túlio Cruz"
    }
    

------------------

Para os testes foram utilizados programas que criam e customizando testes requisições HTTP.

Exemplo: Paw e Advanced REST client
