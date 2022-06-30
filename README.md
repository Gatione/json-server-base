# json-server-base

Esse é um repositório teste

## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

### Cadastro

```POST /register``` <br/>
```POST /signup``` <br/>
```POST /users```

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são os de email e password.
A resposta será um objeto contendo o "acessToken" que contêm um token para o usuário ter acesso as ferramentas que necessitam de autorização, e "user" que contêm as informações de email, name, age e id do usuário.

### Login

```POST /login``` <br/>
```POST /signin```

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"
A resposta será um objeto contendo o "acessToken" que contêm um token para o usuário ter acesso as ferramentas que necessitam de autorização, e "user" que contêm as informações de email, name, age e id do usuário.

### Ver Posts

```GET /posts```

Esta rota pode ser utilizada para retornar um array com os posts.

### Mensagem Para Usuários Logados

```GET /welcome```

Esta rota necessita de autorização utilizando o token de acesso dado quando o usuário realiza o login. No header: <br>
```Authorization: Bearer "acessToken"```
