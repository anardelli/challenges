# Web Scraping

A coleta de dados web, ou raspagem web, é uma forma de mineração que permite a extração de dados de sites da web convertendo-os em informação estruturada para posterior análise. [Wikipédia](https://pt.wikipedia.org/wiki/Coleta_de_dados_web)

## Desafio

O desafio consiste em criar um _script_ ou conjunto de _scripts_ em JavaScript para realizar a raspagem de dados do site [VGMusic.com](http://www.vgmusic.com/).

O site **VGMusic.com** possui uma coletânea das trilhas sonoras dos jogos de vídeo game.

Como resultado final, o _script_ deve gerar um arquivo no formato [JSON](https://www.json.org/json-en.html) com as informações da trilha sonora do jogo **Chrono Trigger**, do Super Nintendo. O documento JSON deve ter o seguinte formato:

```json
[
  {
    "title": "A Premonition",
    "fileSize": 3432,
    "sequencedBy": "Jon Berney",
    "comments": 0
  },
  {
    "title": "A Premonition (2)",
    "fileSize": 4613,
    "sequencedBy": null,
    "comments": 0
  },
  {
    "title": "A Premonition & \"Chrono Trigger\"",
    "fileSize": 22205,
    "sequencedBy": "Masashi Ito",
    "comments": 0
  }
]
```

Se uma informação estiver vazia no site, como por exemplo a coluna **Sequenced by**, então a informação deve receber o valor `null` no documento JSON. Para as colunas **File size** e **Comments** deve-se extrair somente a parte numérica do conteúdo.

Todas as informações sobre a trilha sonora do jogo **Chrono Trigger** podem ser obtidas neste endereço: http://www.vgmusic.com/music/console/nintendo/snes/

## Dicas e tutoriais

### Node.js

Antes de começar é necessário obter e instalar o Node.js. A última versão do Node.js pode ser obtida no site oficial do Node.js: https://nodejs.org/en/

### NPM

o NPM (_Node Package Manager_) é o gerenciador de pacotes oficial do Node.js.

Este artigo mostra como iniciar um novo projeto Node.js e como instalar alguns pacotes: [Set Up and Run a Simple Node Server Project](https://levelup.gitconnected.com/set-up-and-run-a-simple-node-server-project-38b403a3dc09)

O NPM possui um [repositório](https://www.npmjs.com/) repleto de pacotes para executar as mais diversas tarefas.

### Informações úteis

Para a execução deste desafio, sugere-se o uso dos seguintes pacotes:

#### `Got`

O [Got](https://github.com/sindresorhus/got) permite realizar requisições HTTP/HTTPS. Com auxílio desta biblioteca é possível obter o conteúdo de uma página web.

#### `jsdom`

O [jsdom](https://github.com/jsdom/jsdom) permite manipular um documento HTML. Usando os [seletores](https://www.w3schools.com/jsref/met_document_queryselector.asp) é possível extrair as informações desejadas da página HTML.

#### Expressões regulares

Se o `jsdom` não for o suficiente para realizar a tarefa, ainda é possível recorrer às expressões regulares: [Expressões Regulares](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Regular_Expressions).

#### Outras soluções e bibliotecas

As bibliotecas aqui apresentadas são apenas uma sugestão. No entanto, um mesmo problema pode ser resolvido de diferentes formas. Portanto, sinta-se à vontade para usar outras bibliotecas se assim desejar.

## O que deve ser entregue

Deve-se entregar um arquivo `zip` com os arquivos do projeto, incluindo o arquivo `package.json`. Deve-se também incluir um arquivo `README.md` contendo as instruções sobre como executar o projeto. O arquivo **não deve incluir** a pasta `node_modules`.
