# Desplegament d’Aplicacions Web <br>Servei DNS en Sistema Linux

**Fet Per:** Jhonny Claure

**Data:** 31/03/2025

**Exercici 1 – Instal∙lació del servei**

En una màquina Ubuntu Server 24.04, segueix els següents passos per a instal∙lar i configurar el servei de DNS:
**a. Instal∙la Ubuntu Server 24.**
<img src="file:///home/vandalieu06/.config/marktext/images/2025-03-31-12-43-11-image.png" title="" alt="" data-align="center">

**b. Suposant que la IP de la teva xarxa Red NAT és la 10.20.30.0/24, posa‐li la següent IP estàtica al servidor →10.20.30.10**

- **Configura‐li com a DNS el servidor de Google →8.8.8.8**

<img src="file:///home/vandalieu06/.config/marktext/images/2025-03-31-12-47-44-image.png" title="" alt="" data-align="center">

**c. Comprova que la teva màquina pot fer ping a www.jviladoms.cat**
<img src="file:///home/vandalieu06/.config/marktext/images/2025-03-31-12-49-45-image.png" title="" alt="" data-align="center">

**d. Actualitza els repositoris: sudo apt update**
<img src="file:///home/vandalieu06/.config/marktext/images/2025-03-31-12-50-38-image.png" title="" alt="" data-align="center">

**e. Instal∙la el servidor DNS anomenat bind9: sudo apt install bind9 bind9‐utils ‐y**
<img src="file:///home/vandalieu06/.config/marktext/images/2025-03-31-12-52-43-image.png" title="" alt="" data-align="center">

**f. Mira l’estatus del servei: sudo systemctl status bind**

- Recorda que pots parar/iniciar/reiniciar: sudo systemctl stop/start/restart bind

<img src="file:///home/vandalieu06/.config/marktext/images/2025-03-31-12-54-46-image.png" title="" alt="" data-align="center">

**g. Per a què s’iniciï el servei DNS al iniciar el sistema, executa: sudo systemctl enable bind9**

<img src="file:///home/vandalieu06/.config/marktext/images/2025-03-31-13-04-10-image.png" title="" alt="" data-align="center">**h. Explica què és un forwarder**
Un reenviador DNS és un servidor DNS configurat per a reexpedir les consultes que no poden resoldre's localment a un altre servidor DNS, normalment un extern.

**i. Explica què podem trobar en el fitxer/etc/bind/named.conf.options**
Aquest fitxer normalment conté opcions globals per al servidor DNS, com els forwards, ports que escolta, directory del fitxers temproals, logs, etc.

**j. Explica què podem trobar en el fitxer/etc/bind/named.conf.local**

Conté la configuració del servidor DNS local, i aquí és on es declaren les zones associades al domini.

**Exercici 3 – Editar el fitxer named.conf.local**

Edita el fitxer/etc/bind/named.conf.locali afegeix‐li les següents línies que permetran crear les zones de búsqueda directa i inversa:

```shell
zone "cognom.daw" {
    type master;
    file "/etc/bind/zones/db.cognom.daw";
};shell
```

```shell
zone "30.20.10.in‐addr.arpa" {
    type master;
    file "/etc/bind/zones/db.30.20.10";
};
```

<img src="file:///home/vandalieu06/.config/marktext/images/2025-03-31-13-23-48-image.png" title="" alt="" data-align="center">

**Exercici 4 – Creació de les zones DNS**

**a. Executa la següent comanda per a crear la carpeta de zones: sudo mkdir ‐p /etc/bind/zones**

**b. Crea el fitxer /etc/bind/zones/db.cognom.dawi posa‐li la següent definició de la zona directa**

```shell
$TTL 86400
@ IN SOA servidor.cognom.daw. root.cognom.daw. (
    2025032101 ; Serial
    3600 ; Refresh
    1800 ; Retry
    604800 ; Expire
    86400 ) ; Minimum TTL
@ IN NS servidor.cognom.daw.
servidor IN A 10.20.30.
pcwin IN A 10.20.30.
pclinux IN A 10.20.30.
printer IN A 10.20.30.
www IN CNAME servidor.cognom.daw.
server IN CNAME servidor.cognom.daw.
```

**c. Crea el fitxer/etc/bind/zones/db.30.20.10i posa‐li la següent definiciió de la zona inversa**

```shell
$TTL 86400
@ IN SOA servidor.cognom.daw. root.cognom.daw. (
    20250312101 ; Serial
    3600 ; Refresh
    1800 ; Retry
    604800 ; Expire
    86400 ) ; Minimum TTL
@ IN NS servidor.cognom.daw.
10 IN PTR servidor.cognom.daw.
20 IN PTR pcwin.cognom.daw.
30 IN PTR pclinux.cognom.daw.
40 IN PTR printer.cognom.daw.
```

**Exercici 5 – Configuració general del servidor**

Per acabar de configurar el servidor correctament:

```
a. Edita el fitxer/etc/bind/named.conf.optionsi revisa que aparegui la següent
configuració en la secció → options
```

```
options {
directory "/var/cache/bind";
recursion yes;
allow‐query { any; };
forwarders {
8.8.8.8;
8.8.4.4;
};
dnssec‐validation auto;
};
```

```
b. Si tot és correcte, podem reiniciar el servei →sudo systemctl restart bind
c. Finalment podem comprovar l’estat →sudo systemctl status bind
```

**Exercici 7 – Comprovació funcionament client Linux**

Des d’una màquina client Linux com Ubuntu Desktop o Lubuntu, segueix els següents passos
per a comprovar el funcionament:
a. Posa la màquina client en la mateixa xarxa Red NAT que el servidor DNS
b. Edita els paràmetres de xarxa del client i posa‐li com a servidor DNS la IP de la teva
màquina servidor DNS →10.20.30.
c. Comprova que el servidor DNS funciona correctament, executant des del client:
nslookup servidor.cognom.daw
nslookup [http://www.cognom.daw](http://www.cognom.daw)
nslookup pcwin.cognom.daw

**Exercici 8 – Comprovació funcionament client Windows**

Torna a provar de fer les comprovacions però ara a partir d’un client Windows 10

DAW 3
