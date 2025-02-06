# Go API com Docker

Este é um projeto simples de uma API construída em Go, utilizando o framework Gin para o gerenciamento das rotas. A API é hospedada em Docker e utiliza um banco de dados para armazenar informações de produtos. Está hospedada no DockerHub e conta com os arquivos `Dockerfile` e `docker-compose.yml` para facilitar a construção e execução do ambiente.

## Funcionalidades

A API possui 3 rotas principais:

1. **GET /ping**
   - Retorna uma mensagem de ping para verificar se o servidor está ativo.
   - Resposta: `{"message": "pong"}`

2. **GET /products**
   - Retorna todos os produtos cadastrados no banco de dados.
   - Resposta: Lista de produtos com seus respectivos detalhes.

3. **POST /product**
   - Cria um novo produto no banco de dados.
   - Corpo da requisição:
     ```json
     {
       "product_name": "Nome do Produto",
       "price": 99.99
     }
     ```

4. **GET /product/:productId**
   - Retorna um produto específico baseado no ID.
   - Resposta: Detalhes do produto solicitado.

## Como Rodar

### Pré-requisitos

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

### Passos

1. Clone o repositório:

   ```bash
   git clone https://github.com/seu-usuario/go-api-docker.git
   cd go-api-docker
2. Construa a imagem Docker:
   ```bash
   docker build -t go-api .

3. Suba os containers com Docker Compose:
   ```bash
   docker compose up
