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


----------------------------------------------------------------------------------------------------------










