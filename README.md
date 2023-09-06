# 🔑 keycloak-herokuDeploy Keycloak to Heroku by just one click.
```shell
mvn clean install
docker compose up --build
```
```shell
mvn clean install
docker compose -f docker-compose.heroku.yml up --build
```
h2：

```shell
mvn clean install
docker compose -f docker-compose.local.yml up --build
open http://localhost:8080/
```

PostgreSQL
```shell
docker compose -f docker-compose.local-postgres.yml up --build
open http://localhost:8080/
```
[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

This repository deploys the [Keycloak](https://www.keycloak.org) Identity and Access Management Solution
to Heroku. It is based of Keycloak's official docker image with some slight modifications to use the
Heroku variable for `PORT` and `DATABASE_URL` properly.

The deployment will be made with a single Free dyno (although it won't run very well in smaller dynos
due to Java's memory hunger, it can be used as testing purpose without issues) with a free Postgres database attached.
