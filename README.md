<h1 align="center">
  <img alt="Burguer Kenzie" title="BurguerKenzie" src="https://kenzie.com.br/images/logoblue.svg" width="100px" />
</h1>

<h1 align="center">
  Burguer Kenzie - API
</h1>

<p align = "center">
Este é o backend da aplicação Burguer Kenzie - A hamburgueria número 1 entre kenzinhos! O objetivo dessa aplicação é deixar a disposição uma API de qualidade para aqueles que desejarem usar no futuro e quem sabe dar aquela "fomezinha" também! ♥
</p>

<blockquote align="center">“A fome não é exigente: basta contentá-la; como, não importa. - Sêneca”</blockquote>

<p align="center">
  <a href="#endpoints">Endpoints</a>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</p>

## Rotas que não precisam de autenticação

<h2 align ='center'> Listagem de produtos </h2>

Nessa aplicação o usuário sem fazer login ou se cadastrar pode ver os produtos disponíveis na loja e adicioná-los ao carrinho e ver o custo total da possível compra.

`GET /products - FORMATO DE RESPOSTA - STATUS 200`

```json
[
  {
    "name": "Hamburguer",
    "category": "Sanduíches",
    "price": "14.00",
    "img": "https://i.ibb.co/fpVHnZL/hamburguer.png"
  },
  {
    "name": "X-Burguer",
    "category": "Sanduíches",
    "price": "16.00",
    "img": "https://i.ibb.co/djbw6LV/x-burgue.png"
  },
  {
    "name": "Big-Kenzie",
    "category": "Sanduíches",
    "price": "18.00",
    "img": "https://i.ibb.co/cCjqmPM/fanta-guarana.png"
  },
  {
    "name": "Fanta Guaraná",
    "category": "Bebida",
    "price": "5.00",
    "img": "https://i.ibb.co/fpVHnZL/hamburguer.png"
  },
  {
    "name": "Coca-cola",
    "category": "Bebidas",
    "price": "4.99",
    "img": "https://i.ibb.co/fxCGP7k/coca-cola.png"
  },
  {
    "name": "Fanta Laranja",
    "category": "Bebidas",
    "price": "4.99",
    "img": "https://i.ibb.co/QNb3DJJ/milkshake-ovomaltine.png"
  }
]
```

<h2 align="center"> Criação de usuário </h2>

`POST /users - FORMATO DA REQUISIÇÃO`

```json
{
  "email": "johndoe@mail.com",
  "password": "123456",
  "name": "John Doe",
  "age": "22"
}
```

Caso dê tudo certo a resposta será assim:

`POST /users - FORMATO DA RESPOSTA - STATUS 201`

```json
{
  "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImpvaG5kb2VAbWFpbC5jb20iLCJpYXQiOjE2MzU5MDA4MDMsImV4cCI6MTYzNTkwNDQwMywic3ViIjoiNCJ9.s-RD3MuShGlbLWn2ZwGxLCyt2i03n7hCtTDKmo06MFA",
  "user": {
    "email": "johndoe@mail.com",
    "name": "John Doe",
    "age": "22",
    "id": 4
  }
}
```

## Rotas que precisam de autenticação

<h2 align="center">Histórico de compras<h2>

`GET /purchases - FORMATO DA RESPOSTA - STATUS 200`

```json
[
  {
    "name": "Hamburguer",
    "category": "Sanduíches",
    "price": "14.00",
    "img": "https://i.ibb.co/fpVHnZL/hamburguer.png"
  },
  {
    "name": "X-Burguer",
    "category": "Sanduíches",
    "price": "16.00",
    "img": "https://i.ibb.co/djbw6LV/x-burgue.png"
  },
  {
    "name": "Big-Kenzie",
    "category": "Sanduíches",
    "price": "18.00",
    "img": "https://i.ibb.co/cCjqmPM/fanta-guarana.png"
  },
  {
    "name": "Fanta Guaraná",
    "category": "Bebida",
    "price": "5.00",
    "img": "https://i.ibb.co/fpVHnZL/hamburguer.png"
  },
  {
    "name": "Coca-cola",
    "category": "Bebidas",
    "price": "4.99",
    "img": "https://i.ibb.co/fxCGP7k/coca-cola.png"
  },
  {
    "name": "Fanta Laranja",
    "category": "Bebidas",
    "price": "4.99",
    "img": "https://i.ibb.co/QNb3DJJ/milkshake-ovomaltine.png"
  }
]
```

Feito na base do desespero ♥ by Nafly :wave:
