# Pasos para crear un serivod DNS linux Ubuntu 

1. Ip statica
2. netplan apply
3. sudo apt install bind9 dnsutils
4. cd /etc/bird
5. sudo nano  ....deafault.conf
6. Al final del archivo añadir las dos zonas directa e indirecta
7. Fer les copies de les 2 zones db.local i db.127
8. --
```
sudo nano /etc/bind/naruto[nombre]..... 
```
9. sudo service bind 9 restart
9. sudo service bind 9 status