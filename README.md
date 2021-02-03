# API de Games 
Essa API é utilizada para tal e tal....
## Endpoints
### GET /games
Esse endpoint é responsável por retornar a listagem de todos os games cadastrados no banco de dados. 
### Parametros
Nenhum
### Respostas
##### OK! 200
Caso essa resposta aconteça, você vai receber a listagem de todos os games.

Exemplo de resposta:

```
[
        {
            id: 23,
            title: "call of duty MW",
            year: 2019,
            price: 60
        },
        {
            id: 65,
            title: "Sea of thieves",
            year: 2018,
            price: 40
        },
             
         {
            id: 2,
            title: "Minecraft",
            year: 2012,
            price: 20
        }
    ]

```
##### Falha de autenticação! 401.
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de autenticação da requisição. Motivos: Token inválido, token expirado.

```
{
  "err": "Token inválido!"
}
```


### POST /auth
Esse endpoint é responsável por fazer processo de login. 
### Parametros
email: E-mail do usuário cadastrado no sistema.

password: Senha do usuário cadastrado no sistema, com aquele determinado e-mail.

Exemplo:
```
{
  "email": "diego.acta@gmail.com",
  "password": "maradona",
}
```
### Respostas
##### OK! 200
Caso essa resposta aconteça, você vai receber o token JWT para conseguir acessar endpoints protegidos na API.

Exemplo de resposta:

```
  "token":
  "fjlsjgljgldjsglsjglsjgflsjflsktççrfçidpkj95845rrririlsssssssssssssssssssssssssfkwwwwwwwwçgkjpeigpeigpkjgpejtgpejitpejtpowjpowjrpowjrpowjrowjrowjrowjrowjrowjrowjrowjrowjrowjrowjrowjrowjrowjrowjrowjrowrjowrjowrjowjrowjrowjrowjrowrjowtu9w3hb4hkih9iwrpoqjoqre"

```
##### Falha de autenticação! 401.
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de autenticação da requisição. Motivos: Senha e e-mail incorretos.

```
{
  "err": "Credenciais inválidas!"
}
```

