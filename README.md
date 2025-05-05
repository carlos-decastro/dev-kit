🇧🇷 - [Português](#documentação-do-ambiente-de-desenvolvimento)
🇺🇸 - [English](#development-environment-documentation)

# Documentação do Ambiente de Desenvolvimento

## Índice

- [Documentação do Ambiente de Desenvolvimento](#documentação-do-ambiente-de-desenvolvimento)
  - [Índice](#índice)
  - [Introdução](#introdução)
  - [Objetivo do Projeto](#objetivo-do-projeto)
  - [Estrutura do Projeto](#estrutura-do-projeto)
  - [Execução](#execução)
    - [Observação](#observação)
  - [Conexões](#conexões)
    - [PostgreSQL](#postgresql)
    - [Oracle XE](#oracle-xe)
    - [Redis](#redis)
    - [Kafka](#kafka)
    - [MongoDB](#mongodb)
    - [RabbitMQ](#rabbitmq)
    - [Elasticsearch](#elasticsearch)
  - [Interfaces](#interfaces)
    - [KafkaUI](#kafkaui)
    - [RedisInsight](#redisinsight)
    - [MongoExpress](#mongoexpress)
    - [RabbitMQ Management](#rabbitmq-management)
    - [Kibana](#kibana)
  - [Configurações Adicionais](#configurações-adicionais)
    - [Limitar Uso de Memória no Docker Desktop WSL2](#limitar-uso-de-memória-no-docker-desktop-wsl2)
    - [Configuração de Conexão do Redis pelo RedisInsight](#configuração-de-conexão-do-redis-pelo-redisinsight)
  - [Contribuição](#contribuição)
  - [Licença](#licença)

---

## Introdução

Este projeto fornece um ambiente de desenvolvimento completo e isolado para desenvolvedores, utilizando containers Docker para serviços como bancos de dados, filas de mensagens e cache. Ele é projetado para facilitar o desenvolvimento e os testes locais, garantindo que cada desenvolvedor tenha um ambiente independente.

---

## Objetivo do Projeto

O objetivo é criar um ambiente de desenvolvimento isolado para evitar interferências entre desenvolvedores, problemas de compatibilidade e corrupção de dados em ambientes de homologação e produção.

---

## Estrutura do Projeto

A estrutura do projeto é organizada por serviços, cada um com seus próprios arquivos de configuração `docker-compose.yml`. Aqui está a estrutura principal:

```
elasticsearch/
kafka_stack/
mongodb/
oracle/
postgresql/
rabbitmq/
redis/
```

Cada diretório contém os arquivos necessários para configurar e executar os serviços correspondentes.

---

## Execução

Para iniciar o ambiente de desenvolvimento, execute o seguinte comando no diretório do serviço que você deseja executar:

```shell
docker-compose up --build -d
```

Este comando irá construir as imagens e iniciar os containers em segundo plano.

### Observação

Você pode comentar os serviços que não deseja executar no arquivo `docker-compose.yml` ou pausar containers específicos. Os serviços são independentes entre si.

---

## Conexões

### PostgreSQL

- **HOST:** localhost  
- **PORT:** 5432  
- **USER:** postgres  
- **PASSWORD:** admin  

### Oracle XE

- **HOST:** localhost  
- **PORT:** 1521  
- **SID:** XE  
- **USER:** SYSTEM  
- **PASSWORD:** 123456  

### Redis

- **HOST:** localhost  
- **PORT:** 6379  

### Kafka

- **HOST:** localhost  
- **PORT:** 9091  

### MongoDB

- **HOST:** localhost  
- **PORT:** 27017  
- **USER:** root  
- **PASSWORD:** 123456  

### RabbitMQ

- **HOST:** localhost  
- **PORT:** 5672  
- **USER:** guest  
- **PASSWORD:** guest

### Elasticsearch

- **HOST:** localhost  
- **PORT:** 9200

---

## Interfaces

### KafkaUI

- URL: [http://localhost:9000/](http://localhost:9000/)

### RedisInsight

- URL: [http://localhost:8001](http://localhost:8001)

### MongoExpress

- URL: [http://localhost:8089/](http://localhost:8089/)

### RabbitMQ Management

- URL: [http://localhost:15672/](http://localhost:15672/)

### Kibana

- URL: [http://localhost:5601/](http://localhost:5601/)

---

## Configurações Adicionais

### Limitar Uso de Memória no Docker Desktop WSL2

Para limitar o uso de memória no Docker Desktop em modo WSL2, siga as instruções no artigo:  
[How to Limit Memory Usage on Docker Desktop WSL2 Mode](https://medium.com/geekculture/how-to-limit-memory-usage-on-docker-desktop-wsl-2-mode-2a4a719f05fd)

### Configuração de Conexão do Redis pelo RedisInsight

`redis://redis:6379`

---

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests para melhorias.

---

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

---

# Development Environment Documentation

## Index

- [Development Environment Documentation](#development-environment-documentation)
  - [Index](#index)
  - [Introduction](#introduction)
  - [Project Objective](#project-objective)
  - [Project Structure](#project-structure)
  - [Execution](#execution)
    - [Note](#note)
  - [Connections](#connections)
    - [PostgreSQL](#postgresql)
    - [Oracle XE](#oracle-xe)
    - [Redis](#redis)
    - [Kafka](#kafka)
    - [MongoDB](#mongodb)
    - [RabbitMQ](#rabbitmq)
    - [Elasticsearch](#elasticsearch)
  - [Interfaces](#interfaces)
    - [KafkaUI](#kafkaui)
    - [RedisInsight](#redisinsight)
    - [MongoExpress](#mongoexpress)
    - [RabbitMQ Management](#rabbitmq-management)
    - [Kibana](#kibana)
  - [Additional Configurations](#additional-configurations)
    - [Limit Memory Usage on Docker Desktop WSL2](#limit-memory-usage-on-docker-desktop-wsl2)
    - [RedisInsight Connection Configuration](#redisinsight-connection-configuration)
  - [Contribution](#contribution)
  - [License](#license)

---

## Introduction

This project provides a complete and isolated development environment for developers, using Docker containers for services such as databases, message queues, and cache. It is designed to facilitate local development and testing, ensuring that each developer has an independent environment.

---

## Project Objective

The objective is to create an isolated development environment to avoid interference between developers, compatibility issues, and data corruption in staging and production environments.

---

## Project Structure

The project structure is organized by services, each with its own `docker-compose.yml` configuration files. Here is the main structure:

```
elasticsearch/
kafka_stack/
mongodb/
oracle/
postgresql/
rabbitmq/
redis/
```

Each directory contains the necessary files to configure and run the corresponding services.

---

## Execution

To start the development environment, run the following command in the directory of the service you want to run:

```shell
docker-compose up --build -d
```

This command will build the images and start the containers in the background.

### Note

You can comment out the services you do not want to run in the `docker-compose.yml` file or pause specific containers. The services are independent of each other.

---

## Connections

### PostgreSQL

- **HOST:** localhost
- **PORT:** 5432
- **USER:** postgres
- **PASSWORD:** admin

### Oracle XE

- **HOST:** localhost
- **PORT:** 1521
- **SID:** XE
- **USER:** SYSTEM
- **PASSWORD:** 123456

### Redis

- **HOST:** localhost
- **PORT:** 6379

### Kafka

- **HOST:** localhost
- **PORT:** 9091

### MongoDB

- **HOST:** localhost
- **PORT:** 27017
- **USER:** root
- **PASSWORD:** 123456

### RabbitMQ

- **HOST:** localhost
- **PORT:** 5672
- **USER:** guest
- **PASSWORD:** guest

### Elasticsearch

- **HOST:** localhost
- **PORT:** 9200

---

## Interfaces

### KafkaUI

- URL: [http://localhost:9000/](http://localhost:9000/)

### RedisInsight

- URL: [http://localhost:8001](http://localhost:8001)

### MongoExpress

- URL: [http://localhost:8089/](http://localhost:8089/)

### RabbitMQ Management

- URL: [http://localhost:15672/](http://localhost:15672/)

### Kibana

- URL: [http://localhost:5601/](http://localhost:5601/)

---

## Additional Configurations

### Limit Memory Usage on Docker Desktop WSL2

To limit memory usage on Docker Desktop in WSL2 mode, follow the instructions in the article:  
[How to Limit Memory Usage on Docker Desktop WSL2 Mode](https://medium.com/geekculture/how-to-limit-memory-usage-on-docker-desktop-wsl-2-mode-2a4a719f05fd)

### RedisInsight Connection Configuration

`redis://redis:6379`

---

## Contribution

Contributions are welcome! Feel free to open issues or pull requests for improvements.

---

## License

This project is licensed under the [MIT License](LICENSE).

