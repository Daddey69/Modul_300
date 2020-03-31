<img align="left" width="80" height="80" src="./img/../../../img/docker-logo1.png" alt="Docker Logo">

# Images
Im folgenden Ordner habe ich jegliche Images abgelegt, welche ich für dieses Modul sedlber erstellt habe. Dies habe ich hauptsächlich aus Gründen der Sicherheit so gemacht. Dafür habe ich eigenen Dockerfiles erstellt. Diese habe ich basierend auf bestehenden gemacht, danach jedoch noch eigenen Befehle eingefügt und Programme wie net-tools und oing installiert, welche zu testzwecken noch sehr nützlich sind.

Hier eine Auflistung meiner Images und deren Funktionen.
> httpd_egy
> ubuntu_egy

Diese Images musste ich zuerst auf meinem Intel NUC in .tar Dateien umwandeln und dann hier importieren. Dafür habe ich mich zuerst ins richtige Verzeichniss eingewählt

> /test/docker docker images
> /test/docker docker save httpd_egy -o httpd.tar
> /test/docker docker save ubuntu_egy -o ubuntu.tar

Danach konnte ich diese auf meinem Laptop mit folgendem Befehl wieder entpacken.
> docker load -i httpd.tar
> docker laod -i ubuntu.tar

Übrigens können die Images mti dem Befehl `docker pull` aus meinem repository heruntergeladen werden.


[Go back to main Document](https://github.com/Daddey69/Modul_300/blob/master/README.md)
