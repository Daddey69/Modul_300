<img align="left" width="80" height="80" src="./img/../../img/docker-logo1.png" alt="Docker Logo">

# Container / Docker
Docker ist eine Form von Paas (Platform as a Service) welche OS-Level virtualisierung verwendet, zur Bereitstellung sogennanter Contaier. Diese sind grundsätzlich von einander isoliert, konnen jedoch durch das öffnen von Ports und daserstellen von Netzwerken zusammengeschlossen werden. Durch den Zusammenschluss können mehrere Mikroservices zusammen einen grösseren Dienst zur Verfung zu stellen.

Mehr Informationen können unter [Docker Hub](https://hub.docker.com/) gefunden werden.

## Installation der Umgebung
Meine Umgebung habe ich auf meinem INtel NUC installiert, dafür habe ich Ubuntu 16.04 genutzt. Der Vorteil dieser Lösung ist, dass alles remote gespeichert ist und ein Absturz meines Rechners keine schlimmeren Folgen mit sich bringen würde.

Die Installation konnte ich danach mit `docker run hello-world` prüfen.

## Unterschied zu herkömlichem VMs
<img align="center" width="" height="" src="https://github.com/nickegli/Modul_300/blob/master/img/unterschiede.png" alt="Unterschied Container vs. Virtuelle Machine">

Container bringen viele Vorteile mit sich, zum einen sind diese sehr Ressourcensparend, wie man aus der oberen Grafik auslessen kann. Zudem sind sie sehr effizient, da sie nur einen Dienst hosten und somit darauf optimiert sein können.

## Befehle
[Upload]https://github.com/nickegli/Modul_300/blob/master/_LB03/documents/commands.md

## ContainerImage erstellen
Das Image kann mit dem Befehl `docker image build -t websrv-egli .` erstellt werden. Dabei wird das Dockerfile aus dem lokalen Verzeichniss genommen und für die Erstellung des Images verwendet.

Nun ist das Image lokal auf meinem Client abgelegt. Da ich dieses auch auf anderen Geräten verwenden möchte, pusche ich dieses noch mit dem Befehl:  
`docker push websrv-egli`  
Mit diesem Befehl, pusche ich das Image auf meinen Dockerhub Account. Hierzu ist jedoch eine Anmeldung mit dem DOcker Account nötig, dies mit dem Befehl:  
`Docker login`  
Danach kann man sich auf der Dockerhub Webseite anmelden.

## Starten der Umgebung

## Anweisungen Dockerfile
* `FROM`
  * definiert welches Image für den Container verwendet werden sollte.
* `ADD`
  * Ermöglicht das Hinzufügen externer Inhalte.
* `CMD`
  * Nach dem Aufstarten des Containers, werden die folgenden Befehle in einem CMD ausgeführt. Dabei ist jedoch wichtig, dass der `sudo` Befehl nicht verwendet wird, da man sowieso schon mit erhöhten Berechtigungen arbeitet.
* `ENV`
  * Diese Anweisung ermöglicht es Variabeln zu deffinieren, welche im weiteren Verlauf der Installation genutzt werden können.

##  Netzwerk

MySQL Container permanent an Host Port 3306 weiterleiten:

```
$ docker run --rm -d -p 3306:3306 mysql
```

MySQL Container mit nächsten freien Port verbinden:

```
$ docker run --rm -d -P mysql
```






[Go back to main Document](https://github.com/Daddey69/Modul_300/blob/master/README.md)