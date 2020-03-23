<img align="left" width="80" height="80" src="./img/../../img/docker-logo1.png" alt="Docker Logo">

# Container / Docker
Docker ist eine Form von Paas (Platform as a Service) welche OS-Level virtualisierung verwendet, zur Bereitstellung sogennanter Contaier. Diese sind grundsätzlich von einander isoliert, konnen jedoch durch das öffnen von Ports und daserstellen von Netzwerken zusammengeschlossen werden. Durch den Zusammenschluss können mehrere Mikroservices zusammen einen grösseren Dienst zur Verfung zu stellen.

Mehr Informationen können unter [Docker Hub](https://hub.docker.com/) gefunden werden.

## Befehle
Bei den Befehlen muss man immer UNterscheiden zwischen diesen, welche in ein Dockercompose File und in das Terminal passen.

### Terminal
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

### Dockerfile
<-------------------------------------------------> 
> FROM ubuntu:18.04 
> 
> MAINTAINER Yanick Egli-Rohr 
> 
> RUN sudo apt-get update  \ 
> && sudo apt-get install apache2 –Y 
> 
> ENV APACHE_RUN_USER www-data 
> ENV APACHE_RUN_GROUP www-data 
> ENV APACHE_LOG_DIR /var/log/apache2 
> ENV APACHE_RUN_DIR /var/www/html 
> 
> EXPOSE 80 
>
> CMD ["usr/sbin/apache2", "-D", "FOREGROUND"] 
> 
<-------------------------------------------------> 

## Docker Container einrichten

[Go back to main Document](https://github.com/Daddey69/Modul_300/blob/master/README.md)