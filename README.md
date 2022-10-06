# Local infrastructure with docker

A simple code for setup a local environment for development.

## Prerequisite

Just ensure that you have docker installed on your computer.

## How to run

To start all services:
`docker-compose up -d`

To start specific services relevant to your tech stack:
`docker-compose up -d postgres`

## How to custom your own configurations

Create a `.env` in the root folder and override your custom value. See [available variables below](#available-environment-variables).

## Available infrastructure

- Postgres (postgres/postgres)      | `docker-compose up -d postgres-plv8`
- Redis                             | `docker-compose up -d redis`
- MSSQL (sa/Pass@word)              | `docker-compose up -d mssql`
- Mysql (root/Pass@word) | Adminer  | `docker-compose up -d mysql mysql-adminer`
- Mailhog                           | `docker-compose up -d mailhog`
- RabbitMq                          | `docker-compose up -d rabbitmq rabbitmq_management`

... and waiting for your contribute.

### Available environment variables

1. Postgres
 - Ports
   + Default: 5432

| Variable name      | Default value |
| ------------------ | ------------- |
| POSTGRES_DB        | ``postgres``  |
| POSTGRES_USER      | ``postgres``  |
| POSTGRES_PASSWORD  | ``password1``  |

2. Microsoft SQL Server
- Ports
  + Default: 1433

| Variable name      | Default value |
| ------------------ | ------------- |
| MSSQL_SA_PASSWORD  | ``Pass@word``  |

3. Redis
- Ports
  + Default: 6379

| Variable name             | Default value             |
| ------------------------- | ------------------------- |
| ALLOW_EMPTY_PASSWORD      | ``yes``                   |
| REDIS_DISABLE_COMMANDS    | ``FLUSHDB,FLUSHALL``      |

4. Mysql
- Ports
  + DB Server: 3306
  + Adminer: 8080

| Variable name      | Default value |
| ------------------ | ------------- |
| MYSQL_ROOT_PASSWORD  | ``Pass@word``  |

5. MailHog

- Ports
  
  + Web UI: 8025
  + SMTP: 465

1. RabitMq

- Ports
  + Server: 5672
  + Management tool: 15672
