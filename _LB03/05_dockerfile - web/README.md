<img align="left" width="80" height="80" src="../img/../../img/5686.jpg" alt="Apache2 Logo">

# Webserver mit Apache2
Im folgenden dockerfile können Sie meine installation eines Apache2 Webservers sehen, diesen habe ich gebührend auf seine Funktionalität getestet. Dabei habe ich mich jedoch an die standart http und https ports gehalten, das ich kein Problem mit meiner Firewall erhalten würde.

> FROM ubuntu:18.04
> 
> MAINTAINER Somebody
> 
> RUN apt-get update && apt-get install -y apache2
> 
> ENV APACHE_RUN_USER www-data  
> ENV APACHE_RUN_GROUP www-data  
> ENV APACHE_LOG_DIR /var/log/apache2  
> ENV APACHE_RUN_DIR /var/www/html  
> 
> EXPOSE 80
>
> CMD ["/usr/sbin/apache2", "-D", "FOREGROUND"]

[Go back to main Document](https://github.com/Daddey69/Modul_300/blob/master/README.md)