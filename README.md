# Agendador de Tarefas

API REST desenvolvida com Spring Boot para gerenciamento de tarefas agendadas. O projeto permite criar, listar, atualizar e excluir tarefas, além de controlar o status de notificações.

## Tecnologias

- Java 21
- Spring Boot 3
- Spring Web
- Spring Security
- Spring Data MongoDB
- MongoDB
- OpenFeign
- JWT
- Lombok
- MapStruct
- Gradle
- Docker

## Funcionalidades

- Cadastro de tarefas
- Listagem de tarefas do usuário
- Busca de tarefas por período
- Atualização de tarefas
- Alteração do status de notificações
- Exclusão de tarefas
- Autenticação via JWT

## Endpoints

| Método | Endpoint | Descrição |
|---------|----------|-----------|
| POST | /tarefas | Cadastra uma tarefa |
| GET | /tarefas | Lista as tarefas do usuário |
| GET | /tarefas/eventos | Busca tarefas por período |
| PUT | /tarefas?id={id} | Atualiza uma tarefa |
| PATCH | /tarefas?id={id}&status={status} | Atualiza o status |
| DELETE | /tarefas?id={id} | Remove uma tarefa |

## Como executar

### Pré-requisitos

- Java 21
- Gradle
- MongoDB

### Configuração

Configure o MongoDB em `application.properties`:

```properties
spring.data.mongodb.uri=mongodb://localhost:27017/db_agendador
```

### Executando

```bash
./gradlew bootRun
```

ou

```bash
gradlew.bat bootRun
```

A aplicação será iniciada na porta **8081**.

## Estrutura

```
src
├── controller
├── business
├── dto
├── entity
├── repository
├── security
└── mapper
```

## Autor

Desenvolvido por Guilherme Felipe.
