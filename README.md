# Docker_Links_Commands


docker run hello-word

docker run busybox echo hi

docker run busybox ls

docker run busybox ping google.com

------------------------------------------------------------------------------------------------
docker ps

docker ps --all

# delete all the containers that was created previously 
docker system prune

-------------------------------------------------------------------------------------------------
docker create hello-word

docker start -a <id from "docker create hello-word">

docker start -a <id from "docker ps --all">

# getting logs of the particular container

docker log <container-id>

# stop the container 

docker stop/kill <container-id>

----------------------------------------------------------------------------------------------------------

# multiple command 

docker exec  -it or -i -t  <container-id> <command>

example

docker run redis

docker ps

docker exec  -it  <container-id> redis-cli
 
==============================================
# type multiple command 

docker exec  -it  <container-id> sh/zsh/bash

example

docker exec -it busybox sh

----------------------------------------------------------------------------------------------------------

# Creating Container

create a file with name "Dockerfile" withoutany filetype

then below line enter:
++++++++++++++++++++++++++++++++++++++++++++++++++++++++

# Use an existing docker image as a base

FROM alpine

# Download and install a dependency
RUN apk add --update redis
RUN apk add --update gcc

# Tell the image what to do when it starts as a container
CMD ["redis-server"]

+++++++++++++++++++++++++++++++++++++++++++++++++++++

then run the follwing command:

docker build .



----------------------------------------------------------------------------------------------------------






