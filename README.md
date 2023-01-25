<h1>API DE GAMES 🎮</h1>

Documentação sobre API de Games criada no Curso de Nodejs.

<h2>Endpoints 🔌</h2>
<h4>GET /games</h4>
Esse endpoint é responsável por retornar a listagem de todos os games cadastrados no banco de dados.
<hr>
<h3>Parâmetros</h3>
Nenhum
<hr>
<h3>Respostas:</h3>

  <li><strong>Ok! 200:  Caso essa resposta aconteça você vai receber a <em><b>listagem de todos os games</b></em></strong>
    <p>Exemplo de resposta:</p>
</li>

  
  
  ```
[
    {
        "id": 23,
        "title": "Death Stranding",
        "year": 2019,
        "price": 150
    },
    {
        "id": 65,
        "title": "The Sims 4",
        "year": 2014,
        "price": 3000
    },
    {
        "id": 2,
        "title": "Minecraft",
        "year": 2012,
        "price": 20
    }
]
```
  
  
  <li><strong>Falha na autenticação! 401: Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de autenticação da requisição. Motivos: Token inválido, Token expirado.</strong>
  <p>Exemplo de resposta:</p>
</li>



```
{
    "err": "Token inválido!"
}
```


<h4>POST /auth</h4>
Esse endpoint é responsável por retornar o processo de login.
<hr>
<h3>Parâmetros</h3>
<p>email: E-mail do usuário cadastrado no sistema.</p>
<p>password: Senha do usuário cadastrado no sistema, com aquele determinado e-mail.</p>
<p>Exemplo de resposta:</p>


```
{
    "email": "emailteste@email.com",
    "password": "123456"
}
```


<hr>
<h3>Respostas:</h3>
<li><strong>OK! 200: Caso essa resposta aconteça você vai receber o token JWT para conseguir acessar endpoints protegidos na API.</strong>
  <p>Exemplo de resposta:</p>
  </li>
  
  ```
  {
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJlbWFpbHRlc3RlQGVtYWlsLmNvbSIsImlhdCI6MTY3NDYxMDQ3MCwiZXhwIjoxNjc0NzgzMjcwfQ.0IrKf_dJFMVCI1Y_padfL5cnD5fDxnpzmW2mF_tWZCw"
}
  ```
  
  
<li><strong>Falha na autenticação! 401: Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de requisição. Motivos: Senha ou e-mail incorretos.</strong>
  <p>Exemplo de resposta:</p>
</li>


```
{err: "Credenciais inválidas!"}
```


