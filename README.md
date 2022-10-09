## Projeto Albulnz - Backend

![pizza](https://user-images.githubusercontent.com/104647493/194761446-690f12cc-1bc8-4069-bc72-7c9c53f94bad.gif)

<h1 align="center"> :pizza: Projeto Ambulnz - Turma Alves - Labenu  :pizza: </h1>

##  Índice 

* [Descrição](#descrição)
* [Funcionalidades](#funcionalidades)
* [Instruções](#instruções)
* [Link do Projeto](#link-do-projeto)
* [Programas utilizados](#programas-utilizados)
* [Tecnologias utilizadas](#tecnologias-utilizadas)


💬
## Descrição 

<div align='justify'>O projeto consiste na elaboração de um cardápio de pizzas com valores e ingredientes, com pussibilidade de pedidos pelo usuário através de um carrinho de compras. 
<div/>


## Entidades (TypeScript)

### Pizzas
<div align='justify'>
Representa as pizzas do cardápio, com três tabelas criadas no banco de dados, sendo uma de pizzas, uma de ingredientes e uma com a integração entre elas:

- Tabela de Pizzas:
-   `name (string) e chave primária`
-   `price (number)`

- Tabela de Ingredientes:
-   `name (string) e chave primária`

- Tabela de Pizzas com Ingredientes:
-   `pizza_name (string) e chave primária, referência à tabela de pizzas(name)`
-   `ingredient_name (string), referência à tabela de ingredientes(name) `

<div/>

### Pedidos
<div align='justify'>
Representa os pedidos de pizzas feitos pelos usuários, com duas tabelas, sendo uma para o pedido e uma para os itens do pedido.

- Tabela de Pedidos:
-   `id (string) gerado pela aplicação`

- Tabela de Itens do pedido:
-   `id (string) gerado pela aplicação`
-   `order_id (string), referência à tabela de pedidos(id)`
-   `pizza_name (string), referência à tabela de pizzas(name)`
-   `quantity (number)`


<div/>


## Instruções

### Instalando as dependências:

-   `npm install`:
    Instala todas as dependências listadas no `package.json`.

### Criando o arquivo .env:

Criar o arquivo `.env` e configurar com as informações de seu banco de dados.

```
PORT: 3003
DB_HOST = host
DB_USER = usuario
DB_PASSWORD = senha
DB_NAME = nome-do-banco-de-dados
JWT_KEY = "minha-senha-segura"
JWT_EXPIRES_IN = "24h"
BCRYPT_SALT_ROUNDS = 12
```

### Populando a tabela:
-   `npm run migrations`
    Cria e popula as tabelas com dados _mockados_ de usuários e shows.
    -   _Esse script deve ser executado apenas uma única vez_
    -   _Se executado uma segunda vez, ele dropa as tabelas e reseta os dados mockados_
    
    ### Executar o projeto:

-   `npm run dev:`
    Estabelece a conexão com o banco de dados e reinicia automaticamente o servidor `localhost` toda a vez que o projeto for alterado e salvo.

---
### Funcionalidades

#### 1. Busca de todos as pizzas

-   **Método:** `GET`
-   **Caminho:** `/api/pizzas`
-   **Entrada:** `nenhuma`
-   **Saída:** `array de pizzas com ingredientes`

#### 2. Criação de pedido
-   **Método:** `POST`
-   **Caminho:** `/api/orders`
-   **Entrada:** `pizza_name, quantity`
-   **Saída:** `id do pedido, mensagem de pedido feito com sucesso`
#### 3. Busca de pedidos

-   **Método:** `GET`
-   **Caminho:** `/api/orders`
-   **Entrada:** `nenhuma`
-   **Saída:** `array de pedidos do usuário`
-----

### Referência da case:
* `git clone git@github.com:AmbulnzLLC/fullstack-challenge.git && cd fullstack-challenge`

### Tecnologias utilizadas

-   NodeJS
-   TypeScript
-   MySQL
-   Knex
-   Express
-   Cors
-   JWT
-   UUID
-   BcryptJS
-   Markdown
-   Jest

----------

### Programas utilizados

-   Git
-   VSCode
-   Extensão REST Client

### Link do projeto
