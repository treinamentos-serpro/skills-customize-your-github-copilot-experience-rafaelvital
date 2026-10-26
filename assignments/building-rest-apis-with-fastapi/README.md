# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Construa uma API REST para gerenciar um catálogo de livros usando FastAPI. Ao longo das tarefas, você praticará a criação de rotas, operações CRUD, validação de dados e testes de endpoints HTTP.

## 📝 Tasks

### 🛠️ Criar a API e consultar livros

#### Descrição
Crie uma aplicação FastAPI para um catálogo de livros. Comece com uma rota de verificação da API e implemente consultas para listar livros e buscar um livro pelo identificador. Use uma lista em memória como armazenamento inicial.

#### Requisitos
O programa concluído deve:

- Criar a aplicação FastAPI e disponibilizar uma rota `GET /health` que retorne `{"status": "ok"}`
- Implementar `GET /books` para retornar a lista de livros, inicialmente vazia
- Implementar `GET /books/{book_id}` para retornar um livro pelo identificador
- Retornar o status HTTP `404` quando o identificador solicitado não existir
- Incluir instruções para instalar o FastAPI e executar a aplicação com Uvicorn

### 🛠️ Implementar operações CRUD

#### Descrição
Expanda a API para permitir criar, atualizar e remover livros. Cada livro deve ter um identificador, título, autor e ano de publicação. Mantenha os dados em memória; eles não precisam persistir após a aplicação ser encerrada.

#### Requisitos
O programa concluído deve:

- Implementar `POST /books` para criar um livro e retornar o livro criado com status HTTP `201`
- Implementar `PUT /books/{book_id}` para atualizar um livro existente
- Implementar `DELETE /books/{book_id}` para remover um livro existente
- Retornar o status HTTP `404` ao tentar atualizar ou remover um livro inexistente
- Permitir verificar as operações usando a documentação interativa disponível em `/docs`

### 🛠️ Validar entradas e testar endpoints

#### Descrição
Defina modelos Pydantic para as informações de entrada e saída dos livros e acrescente testes automatizados para os principais comportamentos da API.

#### Requisitos
O programa concluído deve:

- Validar que título e autor não sejam vazios e que o ano de publicação seja um número positivo
- Retornar um erro de validação HTTP `422` para dados de entrada inválidos
- Criar testes com o cliente de testes do FastAPI para as rotas de consulta e criação
- Testar pelo menos um caso de recurso inexistente (`404`) e um caso de entrada inválida (`422`)
- Incluir instruções para executar os testes
