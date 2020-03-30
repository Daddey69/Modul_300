<img align="left" width="80" height="80" src="./img/../../img/docker-logo1.png" alt="Docker Logo">

# Docker
Docker ist eine Form von Paas (Platform as a Service) welche OS-Level virtualisierung verwendet, zur Bereitstellung sogennanter Contaier. Diese sind grundsätzlich von einander isoliert, konnen jedoch durch das öffnen von Ports und daserstellen von Netzwerken zusammengeschlossen werden. Durch den Zusammenschluss können mehrere Mikroservices zusammen einen grösseren Dienst zur Verfung zu stellen.

Mehr Informationen können unter [Docker Hub](https://hub.docker.com/) gefunden werden.

## Meine LB03
Für meine LB03 habe ich mich dazu entschieden einen Wordpress Server zu installieren, an diesen habe ich eine Datenbank angeschlossen und einen direkten Webserver, wlcher die Website von Wordpress anzeigt.

[Hier die wichtigsten Befehle](https://github.com/nickegli/Modul_300/blob/master/_LB03/documents/commands.md)

## Container erstellen
Das Dockerfile kann mit dem Befehl `docker build -t websrv-egli .` erstellt werden. Dabei wird das Dockerfile aus dem lokalen Verzeichniss genommen und für die Erstelung des Images verwendet.

## Starten der Umgebung
Meinen Container kann ich mit dem Befehl `docker run -it websrv-egli bash` aufstarten.

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

## Monitoring
Das Monitoring meiner Umgebung habe ich mit CAdvisor von Google gelöst. Diesen Container habe ich ebenfalls in meinem Docker-compose file definiert. Dieser Service sammelt alle Daten meiner Umgebung und nimmt meine Logs auf, damit ich diese dort übersichtlich einsehen kann und ich ein konstantes Monitoring meiner Mikroservices habe.

### config
<img align="center" width="" height="" src="./img/../../img/../../img/cadvisor-conf.png" alt="Monitoring">

## Security
Um die Sicherheit meienr Umgebung zu gewährleisten, habe ich einen Reverseproxy mit nginx eingerichtet. Diesen habe ich ebenfalls via Docker-compose file erstellt. Über diesen werden alle Dienste zur Verfügugn gestellt. Dies ermöglicht das alle Dienste über eine IP laufen und daher nur diese direkt angegriffen werden kann.

### config
<img align="center" width="" height="" src="./img/../../img/../../img/reverse-conf.png" alt="Security - Reverse Proxy">

## Testprotokoll
Wie für die LB02 habe ich hier ein weiteres Testprotokoll, ich habe versucht hierbei die wichtigsten Dienste zu prüfen um deren FUnktionalität sicherzustellen können.

<img align="center" width="" height="" src="./img/../../img/../../img/testprotokoll3.png" alt="<testprotokoll">

[Go back to main Document](https://github.com/Daddey69/Modul_300/blob/master/README.md)