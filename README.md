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
- MSSQL (sa/Pass@word)

... and waiting for your contribute.

### Available environment variables

1. Postgres
 
| Variable name      | Default value |
| ------------------ | ------------- |
| POSTGRES_DB        | ``postgres``  |
| POSTGRES_USER      | ``postgres``  |
| POSTGRES_PASSWORD  | ``postgres``  |

2. Microsoft SQL Server

| Variable name      | Default value |
| ------------------ | ------------- |
| MSSQL_SA_PASSWORD  | ``Pass@word``  |

3. Redis

| Variable name             | Default value             |
| ------------------------- | ------------------------- |
| ALLOW_EMPTY_PASSWORD      | ``yes``                   |
| REDIS_DISABLE_COMMANDS    | ``FLUSHDB,FLUSHALL``      |