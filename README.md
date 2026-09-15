# Task Manager API

API REST para gerenciamento de tarefas, desenvolvida em Java com Spring Boot.

## Sobre o projeto

Este projeto foi desenvolvido como prática de desenvolvimento backend, aplicando conceitos de APIs REST, CRUD, persistência de dados, validação e tratamento de exceções.

A aplicação permite criar, consultar, atualizar e excluir tarefas.

## Tecnologias utilizadas

- Java 21
- Spring Boot
- Spring Web MVC
- Spring Data JPA
- Hibernate
- H2 Database
- Maven
- Git e GitHub

## Funcionalidades

- Criar uma tarefa
- Listar todas as tarefas
- Buscar uma tarefa por ID
- Atualizar uma tarefa
- Excluir uma tarefa
- Validar dados de entrada
- Tratamento de tarefa não encontrada

## Endpoints

| Método | Endpoint | Descrição |
|---|---|---|
| POST | `/tasks` | Criar tarefa |
| GET | `/tasks` | Listar tarefas |
| GET | `/tasks/{id}` | Buscar tarefa por ID |
| PUT | `/tasks/{id}` | Atualizar tarefa |
| DELETE | `/tasks/{id}` | Excluir tarefa |

## Exemplo de criação

### POST `/tasks`

```json
{
    "title": "Estudar Spring Boot",
    "description": "Aprender a criar uma API REST",
    "completed": false
}