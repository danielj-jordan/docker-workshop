# Docker workshop

## Run the container with a local mapped directory

`docker run -d -p 8080:80 -v "$HOME/projects/docker-workshop/web":/usr/local/apache2/htdocs/ httpd:2.4`


## Build the image
The following command will build the image, assig a tag name of docker-workshop based the dockerfile in the current directory.
 
`docker build -t docker-workshop  -f dockerfile .`

## List all the images on the host

`docker images`

## Run the container
Create a container based on the docker-workshop image and map port 8080 on the host to port 80 in the container.

`docker run -d --rm -p 8080:80 docker-workshop`

## List all the containers

`docker ps -a`

## Get a shell in the container
Create a container based on the docker-workshop image and map port 8080 on the host to port 80 in the container.

`docker exec -it docker-workshop `  

## Stop a container

`docker stop <image id from the list of all containers>`  

Exammple `docker stop 0d778a2bd94c`

## Remove a container
If the container has already exited, it may still be on the list of containers.

`docker rm <image id from the list of all containers>`  

## Docker Cheat Sheet
[quick reference](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=11&cad=rja&uact=8&ved=2ahUKEwi-yrHS4_bhAhXWJDQIHXtbB-oQFjAKegQIARAC&url=https%3A%2F%2Fwww.docker.com%2Fsites%2Fdefault%2Ffiles%2FDocker_CheatSheet_08.09.2016_0.pdf&usg=AOvVaw3np6TWDRoQMtDv09rCnRHF)