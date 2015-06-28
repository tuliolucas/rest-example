# rest-example

Exemplo de funcionamento de como se consome um serviço REST, utilizando a API publica do Github e toda documentação relacionada a esta API pode ser encontrada em "https://developer.github.com/v3".

Desta forma conseguiremos identificar os cinco princípios fundamentais são os seguintes:

        Dê a todas as coisas um Identificador (addressability)
        Vincule as coisas (connectedness)
        Utilize métodos padronizados (uniform interface)
        Recursos com múltiplas representações
        Comunique sem estado (statelessness)

1) Para contextualizar, iremos fazer a requisição do recurso tuliolucas, que nada mais é do que meu usuário do Github e todas as informações a respeito.

Já pela URL de acesso ao recurso "https://api.github.com/users/tuliolucas", metodo GET, podemos perceber o conceito de endereçamento, que significa que foi disponibilizado um endereço que representa somente este recurso.
 
 ```
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
Lembrando que o principio de multiplas representações não pode ser apresentado nesta API, pois ela somente retorna o formato JSON.

"...All API access is over HTTPS, and accessed from the api.github.com domain (or through yourdomain.com/api/v3/ for enterprise). All data is sent and received as JSON..."

2) O segundo exemplo iremos atualizar informações relacionadas ao recurso, tuliolucas. 

De acordo com a documentação os dados que podem ser alterados são: name, email, blog, company, location, hireable e bio.

Este tipo de solicitação de alteração de um recurso ou exibição de informações sensíveis, a API utiliza o protocolo de autenticação OAuth2. Para nosso exemplo utilizaremos o OAuth2 com a utilização de TOKEN.

    https://api.github.com/user?access_token=ed3231abe893f9c4a5c45642085722d456c62b95 (metodo PATCH)
    
    Conteúdo:
    
    ```
    {
      "name":"Túlio Cruz"
    }
    ```
    
------------------

Para os testes foram utilizados programas que criam e customizando testes requisições HTTP.
Exemplo: Paw e Advanced REST client
