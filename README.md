# Docker_Links_Commands


docker run hello-word

docker run busybox echo hi

docker run busybox ls

docker run busybox ping google.com

docker run = docker create <image_name> + docker start <container_id>

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

docker log <container-id or (docker create hello-word)>

# stop the container 

docker stop/kill <container-id>

----------------------------------------------------------------------------------------------------------

# multiple command mean multiple commandline windows

docker exec  -it or -i -t  <container-id or (docker ps)> <command>

example:

docker run redis

docker ps

docker exec  -it  <container-id> redis-cli
 
==============================================
# type multiple command  - start typin inside cmd in comtainer

docker exec  -it  <container-id> sh/zsh/bash

example

docker exec -it <container-id>  sh

----------------------------------------------------------------------------------------------------------

# Creating Container 

create a file with name "Dockerfile" withoutany filetype

then below line enter:
++++++++++++++++++++++++++++++++++++++++++++++++++++++++

# Use an existing docker image as a base i.e "tagging the image"

FROM alpine

# Download and install a dependency
RUN apk add --update redis
RUN apk add --update gcc

# Tell the image what to do when it starts as a container
CMD ["redis-server"]

+++++++++++++++++++++++++++++++++++++++++++++++++++++

then run the follwing command:

docker build .
then 
docker run <docker id from the "docker build ." command>

or

docker build -t <your Docker ID / (Respo or projectname) : version>

example: docker build -t rahulbagal/redi_server:latest . 

----------------------------------------------------------------------------------------------------------

# creating a new image from CLI same as above and not recommended this steps:

Use terminal 1:

docker run -it alpine sh

then install redis

#apk add --update redis

Use terminal 2:

docker ps

docker commit -c 'CMD["redis-server"]' <Docker_ID>

docker run <use the id from the above command >










----------------------------------------------------------------------------------------------------------

