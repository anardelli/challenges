# Desafio de programção

Criar uma [API Rest](https://pt.wikipedia.org/wiki/REST) para gerenciamento de Pokemon.

## Pré-requisitos

* Usar o [Node.js](https://nodejs.org/en/) para construção da API.
* Usar o [Express](https://expressjs.com/pt-br/) para construção das rotas.

## Rotas

A API deverá fornecer as seguintes rotas:

### POST /pokemon: Criar um novo Pokémon

#### Especificações

* Requisição
  * Método: `POST`
  * Rota: `/pokemon`
  * Corpo: Objeto JSON com os dados do Pokémon
* Resposta
  * _Status_: 200
  * Corpo: Objeto JSON com os dados do Pokémon inserido

#### Corpo da requisição

Objeto do tipo JSON com os dados do Pokémon. Exemplo:

```json
{
  "number": 47,
  "name": "Parasect",
  "photo": "https://cdn.bulbagarden.net/upload/thumb/8/80/047Parasect.png/250px-047Parasect.png",
  "types": ["Bug", "Grass"]
}
```

#### Corpo da resposta

O objeto de saída deve ser igual ao objeto de entrada:

```json
{
  "number": 47,
  "name": "Parasect",
  "photo": "https://cdn.bulbagarden.net/upload/thumb/8/80/047Parasect.png/250px-047Parasect.png",
  "types": ["Bug", "Grass"]
}
```

### GET /pokemon/{{number}}: Obter um Pokémon

* Requisição
  * Método: `GET`
  * Rota: `/pokemon/{{number}}`
  * Corpo: _Vazio_
* Resposta
  * Quando o Pokémon foi encontrado
    * _Status_: 200
    * Corpo: Objeto JSON com os dados do Pokémon encontrado
  * Quando o Pokémon não foi encontrado
    * _Status_: 404
    * Corpo: Objeto de erro

#### Corpo da resposta (200)

O objeto de saída deve ser o Pokémon encontrado. Por exemplo, ao procurar o Pokémon 47, deve retornar o seguinte objeto:

```json
{
  "number": 47,
  "name": "Parasect",
  "photo": "https://cdn.bulbagarden.net/upload/thumb/8/80/047Parasect.png/250px-047Parasect.png",
  "types": ["Bug", "Grass"]
}
```

#### Corpo da resposta (404)

Caso o Pokémon procurado não exista, deves-se retornar o seguinte corpo como resposta da requisição.

```json
{
  "statusCode": 404,
  "message": "Pokémon not found",
  "error": "Not Found"
}
```
