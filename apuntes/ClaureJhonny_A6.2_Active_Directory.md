# Sistemes Informàtics Operatius <br>Usuaris, grups i carpetes compartides

**Fet Per:** Jhonny Claure

**Data:** 02/04/2025

---

# **Exercici 1: Creació d’usuaris**

A partir de la teva màquina de Windows Server on tens creat el controlador de
domini, executa les següents tasques relacionades amb la creació d’usuaris:
**a. Crea una Unitat Organitzativa (OU) anomenada Activitat‐2**

> Les següents operacions les hauràs de fer sempre dins aquesta OU.

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-24-29-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-25-17-image.png" title="" alt="" data-align="center">

**b. Crea un usuari anomenat _lectura1_ amb password _JVjv2025_**

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-27-10-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-27-49-image.png" title="" alt="" data-align="center">

<img title="" src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-28-37-image.png" alt="" data-align="center">

**c. Crea un usuari anomenat _escriptura1_ amb password _JVjv2025_**
<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-33-34-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-33-53-image.png" title="" alt="" data-align="center">

**d. Crea una carpeta compartida anomenada C:\DAW1DADES**

> Fes que _lectura1_ tingui permisos de lectura sobre aquesta carpeta i _escriptura_
> tingui permisos de control total sobre aquesta carpeta.
> Posa‐hi 2 fitxers qualsevols en aquesta carpeta.

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-40-27-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-41-33-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-42-01-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-42-42-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-42-56-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-44-08-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-44-24-image.png" title="" alt="" data-align="center">

**e. Des d’un client Windows 10, comprova que els 2 usuaris poden iniciar sessió, i que _lectura1_ només pot llegir els fitxers de la carpeta compartida i en canvi
_escriptura1_ pot llegir, escriure, crear carpetes, eliminar fitxers...**

![](C:\Users\Jhonny\AppData\Roaming\marktext\images\2025-04-02-17-55-11-image.png)<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-53-04-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-53-39-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-54-14-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-17-57-26-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-18-01-40-image.png" title="" alt="" data-align="center">

**f. Elimina els privilegis dels usuaris lectura1 i escriptura1 sobre la carpeta
anterior.**

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-18-02-10-image.png" title="" alt="" data-align="center">

## **Exercici 2: Creació de grups i assignació d’usuaris a grups**

A partir de la teva màquina de Windows Server on tens creat el controlador de domini, entra a la OU Activitat‐2 i executa les següents operacions:
**a. Crea un grup anomenat _gLectura_**
<img title="" src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-18-09-40-image.png" alt="" data-align="center">

**b. Crea un grup anomenat _gEscriptura_**
<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-18-10-11-image.png" title="" alt="" data-align="center">

**c. Dóna privilegis de lectura al grup _gLectura_ sobre la carpeta compartida C:\DAW1DADES , i privilegis de control total al grup _gEscriptura_.**
<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-18-11-39-image.png" title="" alt="" data-align="center">

**d. Crea 2 usuaris anomenats _lectura2_ i _lectura3_ i afegeix‐los al grup _gLectura,_ recorda també afegir l’usuarilectura1 què has creat abans.**
<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-18-14-36-image.png" title="" alt="" data-align="center">

**e. Crea 2 usuaris anomenats _escriptura2_ i _escriptura3_ i afegeix‐los al grup _gEscriptura,_ recorda també afegir l’usuari escriptura1 què has creat abans.**
![](C:\Users\Jhonny\AppData\Roaming\marktext\images\2025-04-02-18-16-20-image.png)

**f. Fes sessió des d’un client Windows 10 amb els usuaris anteriors i comprova que els usuaris de _gLectura_ només poden llegir i els usuaris de _gEscriptura_ poden llegir, escriure, crear carpetes, copiar fitxers...**

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-18-20-49-image.png" title="" alt="" data-align="center">

## **Exercici 3: Control dels passwords d’usuari**

> **Dins de la OU Activitat‐2:**

**a. Crea un usuari anomenat _Usuari1_ i fes que hagi de canviar el password el primer cop que iniciï sessió.**

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-18-43-10-image.png" title="" alt="" data-align="center">

**b. Crea un usuari anomeant _Usuari2_ i fes que l’usuari no pugui canviar mai el password.**

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-18-43-42-image.png" title="" alt="" data-align="center">

**c. Crea un usuari anomenat _Usuari3_ i fes que el seu password no expiri mai.**

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-18-44-46-image.png" title="" alt="" data-align="center">

**d. Crea un usuari anomenat _Usuari4_ i fes que per defecte estigui deshabilitat.**

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-18-45-41-image.png" title="" alt="" data-align="center">

> Des d’una màquina client, demostra cada un dels apartats anteriors fent sessió amb cada un dels usuaris creats.

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-18-45-56-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-18-48-10-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-19-02-07-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-19-06-35-image.png" title="" alt="" data-align="center">

![](C:\Users\Jhonny\AppData\Roaming\marktext\images\2025-04-02-19-09-16-image.png)

## **Exercici 4: Restriccions sobre els usuaris**

Els següents passos els hauràs de fer dins la OU Activitat‐2:

1. **Crea un usuari anomenat UsuariRestringit**    

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-19-10-14-image.png" title="" alt="" data-align="center">

2. **Un cop creat l’usuari, ves a les seves propietats i acaba de completar les seves dades:**

**a. En la pestanya General introdueix els teus cognoms en el camp Apellidos**

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-19-12-17-image.png" title="" alt="" data-align="center">

**b. En la pestanya Dirección introdueix les dades de l’adreça de l’escola:
 Carrer Dr Almera 33, Sabadell, Codi Postal: 08206...**

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-19-13-26-image.png" title="" alt="" data-align="center">

**c. Fes que només pugui entrar al sistema de 15h a 20h de la tarda. Recorda  que per fer això hauràs d’entrar a la pestanya *Cuenta* y clicar en el botó *Horas de inicio de session.***

> Demostra que aquest usuari ara no pot fer sessió des d’una màquina client perquè encara no són les 15h de la tarda.

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-19-14-12-image.png" title="" alt="" data-align="center">

<img src="file:///C:/Users/Jhonny/AppData/Roaming/marktext/images/2025-04-02-19-14-59-image.png" title="" alt="" data-align="center">
