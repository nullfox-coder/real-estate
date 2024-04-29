## DockerFile - make sure to provide environment for application to run
## entrypoint - helps to connect to database
## start - start scripts ensure that our models are migrated and django server runs
## docker-compose - tool used for defining and running multi-container Docker applications. It uses YAML files to configure the application's sevices

- build containers
```docker compose up --build -d --remove-orphans```
- down containers
```docker compose down```