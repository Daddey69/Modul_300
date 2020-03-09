<img align="left" width="80" height="80" src="./img/../../img/vagrant-logo.png" alt="Vagrant Logo">

# Vagrant

Vagrant ist eine Software, welche für das automatisierte erstellen von WMs genutzt wird. Vagrantfile lassen sich Konfigurationen an den VMs und Informationen für die Hypervisoren anpassen. Über das CMD, kann vagrant angesprochen werden und somit auch die VMs

Mehr Informationen können unter [Vagrant](https://www.vagrantup.com/) gefunden werden.

## Befehle
* vagrant Init --> Erstellt VM
* vagrant up --> Startet VM
* vagrant ssh --> Verbindet sich per SSH zur VM
* vagrant status --> Zeigt Status der VM an
* vagrant port --> Zeigt weitergeleitete Ports der VM an.
* vagrant halt --> stoppt die VM
* vagrant destroy --> Zerstört / löscht die VM 

## Wissenstand
Im Bereich von Vagrant hatte ich bis zu diesem Modul kein Vorwissen. Ich habe mich im Büro schon mit autoamtisierung von VMs auseinandergesetzt, jedoch habe ich dies hauptsächlich auf Kubernetis und Docker gemacht, da diese hauptsächlich im Windows Bereich verwendet werden.

## Vagrant VM einrichten
1. zuerst muss ein Ordner erstellt werden.
> mkdir newProject
> cd NewProject
2. Nun muss ein neues Vagrantfile erstellt werden.
> vagrant init ubuntu/xenial64
3. Im Vagrant File müssen folgende Zeilen hinzugefügt werden.
> config.vm.provision "shell", inline: <<-SHELL
> sudo apt-get update
>
> sudo apt-get install libapache2-mod-proxy-html
> 
> sudo apt-get install libxm12-dev -y
> 
> sudo a2enmod proxy
> 
> sudo a2enmod proxy_html
> 
> sudo a2enmod proxy_http
> 
> sudo service apache2 restart
> 
> SHELL


1. Augestartet wird die VM mit dem folgenden Befehl:
> vagrant up --provider virtualbox
5. Nun läuft die VM diese kann auch über Virtualbox geöffnet werden.
6. Um die VM zu terminieren wird folgender Befehl genutzt.
> vagrant destroy -f

<img align="center" width="" height="" src="./img/../../img/apache_code1.PNG" alt="Apache Code">

## Funktionstest
Die Funktionalitäten unser VMs können wir testen, indem wir die gehostete Website unseres Apache Webservers aufrufen. Dazu erstellen wir zuerst eine VM.

1. Zuerst nehmen wir das forgefertigte Image aus dem /web Ordner
2. Dieses starten wir auf
> vagrant up
3. Danach öffnen wir den Browser auf unserem Client und schauen ob wir über die ip und den port des Dienstes, die Website aufrufen können.
<img align="center" width="" height="" src="./img/../../img/websrv-test.png" alt="Webserver Test">


### Netzwerkplan
<img align="center" width="" height="" src="./img/../../img/Netzplan-Websrv1.jpg" alt="Netzplan">




[Go back to main Document](https://github.com/Daddey69/Modul_300/blob/master/README.md)