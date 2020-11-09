# Databas-SurvivalGuide

## Docker
Connect to docker-container:
```sh
docker exec -it *docker-container-name* /bin/bash
```
Start docker with docker-compose.yml file:
```sh
docker-compose up
```
Docker-compose.yml file example:
```yml
version: "3"

services:
  db:
    image: mysql:latest
    container_name: "MySQL_DB"
    ports:
      - "33006:3306"
    cap_add:
      - SYS_NICE
    environment:
      MYSQL_ROOT_PASSWORD: password
      MYSQL_DATABASE: carparts
```
