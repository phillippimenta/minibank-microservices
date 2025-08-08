# Mini Bank – Management Microservices

Project developed to showcase my programming skills and enhance my professional portfolio. The system is based on a microservices architecture and implements banking management functionalities using Java and Spring Boot. It features asynchronous communication via RabbitMQ, service-to-service integration with Feign Client, and data persistence with Spring Data JPA, PostgreSQL, and MongoDB. Technologies such as Lombok, Bean Validation, and best architecture practices were applied to ensure code organization, readability, and scalability.

## General Architecture Diagram

![General Architecture Diagram](https://github.com/phillippimenta/minibank-microservices/blob/main/docs/ArchitectureDiagram.png)

## Subindo a infraestrutura com Docker Compose

Para iniciar a infraestrutura definida no arquivo docker-compose.yml, é necessário criar um arquivo .env na raiz do projeto com as variáveis de ambiente abaixo:

```
# Account Service DB
ACCOUNT_DB_USER=account_user
ACCOUNT_DB_PASSWORD=account_pass
ACCOUNT_DB_NAME=account_db
ACCOUNT_DB_PORT=5433

# Settlement Service DB
SETTLEMENT_DB_USER=settlement_user
SETTLEMENT_DB_PASSWORD=settlement_pass
SETTLEMENT_DB_NAME=settlement_db
SETTLEMENT_DB_PORT=5434

# Transfer Service DB (Mongo)
TRANSFER_DB_USER=transfer_user
TRANSFER_DB_PASSWORD=transfer_pass
TRANSFER_DB_PORT=27017
```

Após criar o arquivo .env, execute:

```
docker-compose up -d
```
