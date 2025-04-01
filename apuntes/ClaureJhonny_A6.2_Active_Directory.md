# DAW1 – Sistemes Informàtics Operatius

# Activitat 6.2: Usuaris, grups i carpetes compartides

**Exercici 1: Creació d’usuaris**
A partir de la teva màquina de Windows Server on tens creat el controlador de
domini, executa les següents tasques relacionades amb la creació d’usuaris:
a. Crea una Unitat Organitzativa (OU) anomenada Activitat‐ 2
Les següents operacions les hauràs de fer sempre dins aquesta OU.
b. Crea un usuari anomenat _lectura1_ amb password _JVjv_
c. Crea un usuari anomenat _escriptura1_ amb password _JVjv_
d. Crea una carpeta compartida anomenada **C:\DAW1DADES**
Fes que _lectura1_ tingui permisos de lectura sobre aquesta carpeta i _escriptura_
tingui permisos de control total sobre aquesta carpeta.
Posa‐hi 2 fitxers qualsevols en aquesta carpeta.
e. Des d’un client Windows 10, comprova que els 2 usuaris poden iniciar sessió, i
que _lectura1_ només pot llegir els fitxers de la carpeta compartida i en canvi
_escriptura1_ pot llegir, escriure, crear carpetes, eliminar fitxers...
f. Elimina els privilegis dels usuaris lectura1 i escriptura1 sobre la carpeta
anterior.

**Exercici 2: Creació de grups i assignació d’usuaris a grups**
A partir de la teva màquina de Windows Server on tens creat el controlador de
domini, entra a la OU Activitat‐2 i executa les següents operacions:
a. Crea un grup anomenat _gLectura_
b. Crea un grup anomenat _gEscriptura_
c. Dóna privilegis de lectura al grup _gLectura_ sobre la carpeta compartida
**C:\DAW1DADES** , i privilegis de control total al grup _gEscriptura_.
d. Crea 2 usuaris anomenats _lectura2_ i _lectura3_ i afegeix‐los al grup _gLectura,_
recorda també afegir l’usuarilectura1què has creat abans.
e. Crea 2 usuaris anomenats _escriptura2_ i _escriptura3_ i afegeix‐los al grup
_gEscriptura,_ recorda també afegir l’usuariescriptura1què has creat abans.
f. Fes sessió des d’un client Windows 10 amb els usuaris anteriors i comprova
que els usuaris de _gLectura_ només poden llegir i els usuaris de _gEscriptura_
poden llegir, escriure, crear carpetes, copiar fitxers...


**Exercici 3: Control dels passwords d’usuari**

1. Dins de la OU Activitat‐2:
    a. Crea un usuari anomenat _Usuari1_ i fes que hagi de canviar el password el
       primer cop que iniciï sessió.
    b. Crea un usuari anomeant _Usuari2_ i fes que l’usuari no pugui canviar mai el
       password.
    c. Crea un usuari anomenat _Usuari3_ i fes que el seu password no expiri mai.
    d. Crea un usuari anomenat _Usuari4_ i fes que per defecte estigui deshabilitat.
2. Des d’una màquina client, demostra cada un dels apartats anteriors fent sessió
    amb cada un dels usuaris creats.

**Exercici 4: Restriccions sobre els usuaris**
Els següents passos els hauràs de fer dins la OU Activitat‐2:

1. Crea un usuari anomenatUsuariRestringit
2. Un cop creat l’usuari, ves a les seves propietats i acaba de completar les seves
    dades:
       a. En la pestanya _General_ introdueix els teus cognoms en el camp _Apellidos_
       b. En la pestanya _Dirección_ introdueix les dades de l’adreça de l’escola:
          _Carrer Dr Almera 33, Sabadell, Codi Postal: 08206..._
       c. Fes que només pugui entrar al sistema de 15h a 20h de la tarda. Recorda
          que per fer això hauràs d’entrar a la pestanya _Cuenta_ y clicar en el botó
          _Horas de inicio de session._
3. Demostra que aquest usuari ara no pot fer sessió des d’una màquina client
    perquè encara no són les 15h de la tarda.


