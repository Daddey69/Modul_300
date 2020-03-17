<img align="left" width="80" height="80" src="../img/../../img/5686.jpg" alt="Apache2 Logo">

# ReverseProxy & Proxy mit Apache2
Im folgenden Vagrant-File können Sie meine installation eines Apache2 Servers sehen, diesen habe ich mit weiteren Paketen zu einem Funkionsfähigen ReverseProxy umgebaut. Leider ist mir jedoch kein konkreter Testfall dazu in den Sinn gekommen, da ich keine Zeit hatte um mich tiefer mit dieser Thematik auseinander zu setzten.

### Terminal
```
$ sudo apt-get update

$ sudo apt-get install libapache2-mod-proxy-html
$ sudo apt-get install libxm12-dev -y

$ sudo a2enmod proxy
$ sudo a2enmod proxy_html
$ sudo a2enmod proxy_http 

$ sudo service apache2 restart
```

[Go back to main Document](https://github.com/Daddey69/Modul_300/blob/master/README.md)