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
- Postgres (postgres/postgres)
- Redis
- MSSQL (sa/Pass@word)
- Mysql (root/Pass@word)
- Mailhog

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

| Variable name      | Default value |
| ------------------ | ------------- |
| MYSQL_ROOT_PASSWORD  | ``Pass@word``  |

5. MailHog
- Ports
  + Web UI: 8025
  + SMTP: 465
