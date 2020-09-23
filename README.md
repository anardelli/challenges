# Desafio de programção

Criar uma [API Rest](https://pt.wikipedia.org/wiki/REST) para gerenciamento de Pokemon.

## Pré-requisitos

* Usar o [Node.js](https://nodejs.org/en/) para construção da API.
* Usar o [Express](https://expressjs.com/pt-br/) para construção das rotas.

## Rotas

A API deverá fornecer as seguintes rotas:

### POST /pokemon: Criar um novo Pokemon

#### Especificações

* Método: `POST`
* Rota: `/pokemon`
* Entrada: Objeto JSON com os dados do Pokemon
* _Status_ da resposta: 200
* Corpo da resposta: Objeto JSON com os dados do Pokemon inserido

#### Objeto de entrada

Objeto do tipo JSON com os dados do Pokemon. Exemplo:

```json
{
  "number": 47,
  "name": "Parasect",
  "photo": "https://cdn.bulbagarden.net/upload/thumb/8/80/047Parasect.png/250px-047Parasect.png",
  "types": ["Bug", "Grass"]
}
```

#### Objeto de saída

O objeto de saída deve ser igual ao objeto de entrada:

```json
{
  "number": 47,
  "name": "Parasect",
  "photo": "https://cdn.bulbagarden.net/upload/thumb/8/80/047Parasect.png/250px-047Parasect.png",
  "types": ["Bug", "Grass"]
}
```
