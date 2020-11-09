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
## Alembic
Initialise Alembic:
```sh
alembic init migrations
```
Create a new revision with description:
```sh
alembic revision -m 'description'
```
Run revisions:
```sh
alembic upgrade head
```
Downgrade to given revision Id:
```bash
alembic downgrade *revisionId*
```
Check revision history:
```sh
alembic history
```
