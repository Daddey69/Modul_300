<img align="left" width="80" height="80" src="./img/../../img/firewall-logo.jpg" alt="UFW Logo">

# Uncomplicated Firewall auf Ubuntu Xenial
Im folgenden Vagrant-File können Sie meine installation einer Ubuntu/Xenial64 VM, diese habe ich mit dem zusätzlichen UFW Paket zu einer Firewall umgebaut. Um die Funktionalität dieser zu prüfen, habe ich zwei einfache Rules erstellt und diese getestet, dabei war es öglich für mich auf die UFW über den Port 22 zuzugreifen.

### Terminal
```
$ sudo apt-get update

$ sudo apt-get install ufw -y
  
$ sudo ufw all 80/tcp
$ sudo ufw allow from any to any port 22

$ sudo ufw enable
```

[Go back to main Document](https://github.com/Daddey69/Modul_300/blob/master/README.md)