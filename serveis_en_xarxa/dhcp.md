## DHCP (Windows) 

- Rang 200.200.8.75 a 200.200.8.125
- Reserva => pc1 - 200.200.8.200
- Domini => online.com

## PASOS CONFIGURACION DHCP

1. cd /etc/netplan
2. cp 00-... 00-...backup
3. sudo nano 00-...
4. config:

``` 
enp0s3
    addresses: [xxx.xxx.xxx.xxx]
    dhcp: false
    routes:
        - to: default 
        via: xxx.xxx.xxx.1
    nameservers:
        addresses: [xxx.xxx.xxx.xxx]  
```
5. sudo netplan apply
6. sudo install isc-dhcp-server
7. cd /etc/dhcp
8. sudo nano dhcpd.conf
```
subnet xxx.xxx.xxx.xxx netmask xxx.xxx.xxx.xxx {
    range xxx.xxx.xxx.xxx xxx.xxx.xxx.xxx;
    option domain-name-servers 8.8.8.8;
    option domain-name "example.org";
    option routers xxx.xxx.xxx.1;
    option broadcast-address xxx.xxx.xxx.255;
    default-lease-time 600;

    host namereserva{
        hardware ethernet xx:xx:xx:xx:xx:xx;
        fixed-address xxx.xxx.xxx.xxx;
    }
}
```
9. sudo service isc-dhcp-server restart
10. sudo service isc-dhcp-server status 
11. error line pc2{} 89
12. error line 90