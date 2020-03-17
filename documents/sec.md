<img align="left" width="80" height="80" src="./img/../../img/sec-logo.png" alt="Security">

# Security

### Wissenstand
Im Bereich Security, habe ich verhältnissmäsig zur Verantwortung welche ich im allgemeine Berufsaltag trage noch relativ wenig gelernt. Aktuell beschränkt sich mein Wissen noch auf einfache Firewall Rules und Konfigurationen von Clients sowie Subentting.

## Firewall & Rules
Hier sieht man die erstellten Firewall Rules. Hierbei habe ich denn Zugriff per SSH nur auf meinen eigenen Client beschränkt.


<img align="center" width="" height="" src="./img/../../img/ufw_rules.PNG" alt="Firewall Rules">

## Proxy / Reverse Proxy

### Proxy
Ein Proxy ins eine Kommunikationsschnittstelle in einem Netzwerk. Er arbeitet als Vermittler, der auf einer Seite Anfragen aufnimmt, um dann über eine eigene Adresse eine Verbindung zur gewünschten Seite herzustellen.

### Reverse Proxy
Der Reverse-Proxy holt Ressourcen für einen Client aus dem Netzwerk. Dabei wird die wahre Adresse des internet systems dem externen System nicht zugänglich gemacht.

#### Konfiguration 
<img align="center" width="" height="" src="./img/../../img/apache2_status.PNG" alt="apache2_status">

## Benutzer & Rechte

Linux besitzt unterschiedliche Arten von Benutzer, dabei muss man UNterscheiden zwischen dennen, welche einer richtigen Person zugeweisen sind und diese die einem Dienst gehören.

| Benutzername  | Funktion                                             |
| ------------- | ---------------------------------------------------- | 
| `root`        | Der Systemadministrator unter Linux                  |
| `nobody`      | Wird von Prozessen als Benutzererkennung verwendet, wenn nur ein Minimum an Rechten vergeben werden soll  |
| `cupsys`      | Benutzer des Druckdienstes CUPS                      |
| `www-data`    | Benutzer des Webservers Apache                       |

Die Benutzer kann man in der Datei `/etc/passwd` finden. zusätzlich werden die Passwörter in der Datei `/etc/shadow` gespeichert.

Der Systemadministrator hat kein Passwort daher ist eine Anmeldung mit diesem Account auch nicht möglich. Falls root berechtigungen für das Ausführen eines befehls nötig sind, so können diese mit dem zusatz von "sudo" genutzt werden.

Alle Befehle, welche erhöhte Berechtigungen eines Benutzers benötigen, sollten mit `sudo` ausgeführt werden.
> sudo apt-get install apache2
> sudo service apache2 start

Es ist auch möglich das gesammte Terminal in den "sudo-modus" zu versetzen, dazu muss man im Terminal einfach `sudo su` eingeben.




## SSH-Tunnel

### Testing
Die nachfolgenden Tests, wurden durch Frau Schönenberger durchgeführt, wobei Sie kein vorwissen über die Funktionalität un die Architektur meiner vorliegenden Umgebung hatte.

<img align="center" width="" height="" src="./img/../../img/testprotokoll.PNG" alt="Testprotokol">

[Go back to main Document](https://github.com/Daddey69/Modul_300/blob/master/README.md)
