# Task Manager API

API REST para gerenciamento de tarefas, desenvolvida em Java com Spring Boot.

## Sobre o projeto

O Task Manager API é um projeto backend desenvolvido para praticar e demonstrar conceitos de desenvolvimento de APIs REST utilizando Java e Spring Boot.

A aplicação permite realizar operações de CRUD (Create, Read, Update e Delete) sobre tarefas, utilizando persistência de dados com Spring Data JPA e banco de dados H2.

O projeto também possui validação de dados e tratamento global de exceções.

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
- Tratamento global de exceções
- Retorno de erro HTTP 404 para tarefas não encontradas

## Estrutura do projeto

```text
src
└── main
    ├── java
    │   └── com.marcelo.taskmanager
    │       ├── controller
    │       ├── entity
    │       ├── exception
    │       ├── repository
    │       └── service
    └── resources
        └── application.properties
```

## Endpoints

| Método | Endpoint | Descrição |
|---|---|---|
| POST | `/tasks` | Criar tarefa |
| GET | `/tasks` | Listar todas as tarefas |
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
```

### Resposta

```json
{
    "id": 1,
    "title": "Estudar Spring Boot",
    "description": "Aprender a criar uma API REST",
    "completed": false
}
```

## Tratamento de erros

A aplicação possui um tratamento global para tarefas não encontradas.

Exemplo:

### GET `/tasks/999`

```json
{
    "status": 404,
    "message": "Tarefa não encontrada com o ID: 999"
}
```

## Banco de dados

O projeto utiliza o **H2 Database em memória**, facilitando a execução e os testes da aplicação sem necessidade de configurar um banco de dados externo.

## Como executar

### 1. Clonar o projeto

```bash
git clone https://github.com/marcelogsouza1/taskmanager.git
```

### 2. Entrar na pasta

```bash
cd taskmanager
```

### 3. Executar com Maven

```bash
mvn spring-boot:run
```

A API estará disponível em:

```text
http://localhost:8080
```

## Testes realizados

Durante o desenvolvimento foram testadas as principais operações da API:

- POST `/tasks`
- GET `/tasks`
- GET `/tasks/{id}`
- PUT `/tasks/{id}`
- DELETE `/tasks/{id}`
- Validação de dados
- Tratamento de erro HTTP 404

## Autor

**Marcelo Souza**

GitHub:  
https://github.com/marcelogsouza1

LinkedIn:  
https://www.linkedin.com/in/marcelogsouza/