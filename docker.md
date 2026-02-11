# :memo: Notes
## DOCKER
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [Docker](https://www.docker.com/)
- [Docker Hub](https://hub.docker.com/)
- [Docker Docs](https://docs.docker.com/)
- [Docker Reference documentation](https://docs.docker.com/reference/)
- [Docker Engine overview](https://docs.docker.com/engine/)
### Terms and concepts
- Docker Hub Service (Repositories for storing and sharing images)
* Image (Similar to template, class)
  - Files
  - File tree
  - Settings
  * Layers set (read-only)
    - id
    - files
* Container (Similar to instance, object.  It must contain everything needed to run an application)
  - Operative System
  - Dependencies
  - Configuration
  - Scripts
  - Binaries
  - Application
  - etc
  * States
    - Running
    - Stoped
- Network
- Volume
- Docker CLI
- Docker compose
* Docker desktop
  - Docker CLI
  - Docker compose
- Port mapping
* Dockerfile
  - Docker build
- Docker network
* Docker volumes
  - Anonymous
  - Named
  - Host
* Dockerignore

* Dockerize
  - Dockerfile
  - .dockerignore
  - docker-compose.yml

### Installation
- Docker Hub (account)
- Docker Engine
- Docker Compose
- Docker Desktop (optional)

Verify
```
$ docker --version
$ docker -v
$ docker compose version
$ sudo docker run hello-world
```
### Image
Basic commands
```
$ docker search <image>
$ docker pull <image>
$ docker images
$ docker rm image <image>
$ docker build <parameter> <name_image> <path_context>
```
### Container
Basic commands
```
$ docker run <parameter (optional)> <image> <command (optional)>
$ docker exec <parameter (optional)> <container> <command>
$ docker ps <parameter (optional)>
$ docker stop <container>
$ docker start <container>
$ docker rm <container_name_or_id>
$ docker rm <parameter (optional)> <container_name_or_id>
$ docker logs <container id or container name>
```
Create own container
```
$ docker pull <image base>
$ docker container create <image base> or docker create <image base>
$ docker start <container id>
```
or
```
$ docker run -d <image base>
```
or Dockerfile
### Network
Basic commands
```
$ docker network ls
$ docker network create <name>
$ docker network rm <network>
$ docker run --network <network>
$ docker run --port <host_port:container_port>
$ docker run --p <host_port:container_port>
```
Create own network
```
$ docker network create <name>
```
### Volume
Basic commands
```
$ docker volume ls
$ docker volume create <name>
```
### Common commands
Basic
```
$ docker -v
$ docker logs
```
Get docker container including size:
```
$ docker ps -s
```
Get docker container disk utilization:
```
$ docker system df
```
Stop all running containers
```
$ docker stop $(docker ps -aq)
```
Delete all containers
```
$ docker rm $(docker ps -aq)
```
Delete all containers including its volumes use
```
$ docker rm -vf $(docker ps -aq)
```
Delete all the images
```
$ docker rmi -f $(docker images -aq)
```
Delete everything - Remove all unused containers, volumes, networks and images
```
$ docker system prune -a --volumes
```
Reset docker
```
$ docker stop $(docker ps -aq)
$ docker system prune --all --force
```
Disable docker container autostart
```
$ docker inspect <container>
$ docker update --restart=no <container>
```
#### Dockerfile
Basic Setup
```
$ vi Dockerfile
```
Dockerfile
```
FROM <image base>
RUN mkdir -p <absolute_path into container>
WORKDIR <absolute_path into container>
COPY <path_context (relative path) (source code)> <path_image (absolute or relative path) (destination)>
RUN <command>
EXPOSE <port>
CMD <default_command>
```
.dockerignore
```
<directories and/or name files>
```
Create image
```
$ docker build -t <image name> .
```
Run docker container
```
$ docker run <image name>
$ docker run -p 4201:4200 <image name>
```
#### Docker compose
Basic Setup
```
$ vi docker-compose.yaml
```
docker-compose.yaml
```
version: <docker compose version>
services:
  <container image name>
      <options>
  <container name>
    <options>
  <container name>
    build:
    ports:
    links:
  <container name>
    image: <image name>
    ports:
    environment:
    volumes:
      - example-data: <path>
  ...
networks:
  <options>
volumes:
  <options>
  example-data:
```
Basic commands
```
$ docker-compose --version
$ docker-compose build
$ docker-compose up <parameters (optionals)> <services (optionals)>
$ docker-compose stop <services (optionals)>
$ docker-compose down
$ docker-compose run <parameters (optionals)> <services> <command (optional)>
$ docker-compose logs <parameters (optionals)> <services (optionals)>
```
###### Examples
Share image
```
$ docker build -t <username/image_name> .
$ docker login
$ docker push <username/image_name>
```
or
```
$ docker tag <id> <new_name>
$ docker push <name>
```
Create network
```
$ docker network create <name> ...
```
Run
```
$ docker run -it --network create <name> ...
$ docker run -dp 3000:3000 ...
```
Setup container image with dockerfile
```
$ vi Dockerfile
```
Dockerfile
```
FROM <repo_name>:<version> (e.g. alpine, slim-buster)
```
Build container image
```
$ docker build  -t <name> .
```
View images
```
$ docker images
```
Delete image
```
$ docker image rm <id>
```
Run the application (when run container image, it create a new container, a new process)
```
$ docker run -it <id_image>
$ docker run -it -p 80:80 <id_image>
```
Stop container
```
$ docker stop
```
View all containers
```
$ docker ps -a
```
Delete all inactive containers
```
$ docker system prune
```
Setup container image with dockerfile
```
$ vi Dockerfile
```
Dockerfile
```
FROM ...
WORKDIR ...
COPY . .
RUN <command>
CMD [...]
ENTRYPOINT <command>
```
Build container image
```
$ docker build  -t <name> .
```
Run the application
```
$ docker run <name>
$ docker run -p 3000:3000 <name>
$ docker run -dp 3000:3000 <name>
$ docker run -d -v <path> -p 3000:3000 <name>
```
Stop image
```
$ docker stop <container_name_or_id>
$ docker stop $(docker ps -q)
$ docker kill $(docker ps -q)
```
Re-Build image
```
$ docker build  -t <repo_name>:<version> .
```
###### Example
PostgreSQL

```
$ docker --version
$ docker info
$ docker run -d \
    --name project_name_postgres \
    -e POSTGRES_DB=project_name \
    -e POSTGRES_USER=postgres \
    -e POSTGRES_PASSWORD=postgres \
    -p 5432:5432 \
    -v op_postgres_data:/var/lib/postgresql/data \
    postgres:16
$ docker ps
$ docker exec -it project_name_postgres psql -U postgres -d project_name
$ project_name=#
  SELECT version();
  \q
```

Start the existing container
```
$ docker ps -a --filter "name=project_name_postgres"
$ docker start project_name_postgres
```

Remove the old container and create a new one
```
$ docker rm -f project_name_postgres
$ docker run -d --name project_name_postgres \
  -e POSTGRES_DB=project_name \
  -e POSTGRES_USER=postgres \
  -e POSTGRES_PASSWORD=postgres \
  -p 5432:5432 \
  postgres:16
```
## Software Developer
Built by [JAVI](https://github.com/javi0b01/) :copyright: 2020 - 2026  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).
