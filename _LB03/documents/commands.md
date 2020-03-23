<img align="left" width="80" height="80" src="./img/../../../img/docker-logo1.png" alt="Docker Logo">

# Befehle
Bei den Befehlen muss man immer UNterscheiden zwischen diesen, welche in ein Dockercompose File und in das Terminal passen.

## Terminal
* docker start + (Docker-ID)
* docker run + (Image)
* Docker run -it + (Image)
* Docker run --net Test –ip 192.168.2.22 -it ubuntu bash 
* Docker container run –name XXX –p 8080:80 
* Docker stop 
* Docker kill
* Docker exec –it + (Docker-ID) (bash/sh) 
* Docker rm $(docker ps –a -q) 
* Docker ps  
* Docker ps -a 
* Docker build -t (Name des Image) . 
* Docker image ls