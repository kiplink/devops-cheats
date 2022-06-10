####### DOCKER COMMANDLINE #######

# list images

docker images

# menjalankan container

docker run -d --name <some name> [OPTIONS] <some image>

OPTIONS:
-p <external port>:<internal port>
-e <some environment>
-v <local path>:<container path>

example:
docker run -d --name postgresql -p 5433:5432 -e POSTGRES_PASSWORD=Passw0rd -v /home/kiplink/volumes/postgre:/var/lib/postgresql/data postgres

# list container yang running

docker ps

# list semua container

docker ps -a

# masuk kedalam container

docker exec -it <nama/id container> <bash/sh>

# logs container

docker logs <nama/ID container>

# melihat detail container

docker inspect <nama/ID container>

# build image docker

docker build -t <username>/<image name>:<version> -f <specify a Dockerfile>

example:
docker build -t kiplink/ubuntu:1.0 -f Dockerfile

# push/publish image to docker hub

docker push kiplink/ubuntu:1.0

# create docker network

docker network create -d bridge local-network

# list docker network

docker network ls

REFERENCE:
https://docs.docker.com/engine/reference/commandline/docker/

####### DOCKER COMPOSE ########

# 1. create folder

# 2. create file docker-compose.yaml

# create and start container

docker-compose up -d

# stop container

docker-compose stop

# start container

docker-compose start

# masuk ke dalam container

docker-compose exec <nama container> <bash/sh>

# stop and remove container

docker-compose down

REFERENCE:
https://docs.docker.com/engine/reference/commandline/compose/
