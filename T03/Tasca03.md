# T03 - Seveis dde Tranferència de Fitxers
## SMX 2A | Edu Gordo Cebrià

---

![Imatge](IMG/1.png)

Per fer aquesta activitat, la nostra màquina virtual utilitzara un adaptador en "Xarxa NAT" i un altre en "Adaptdor de només l'anfitrió"

---

![Imatge](IMG/2.png)

Ara si, entrem en la màquina del servidor d'Ubuntu i entrem en el fitxer del netplan per configurar els adaptadors

---

![Imatge](IMG/3.png)

Apliquem els canvid del netplan i fem "ip a" per veure la nostra direcció IP

---

![Imatge](IMG/4.png)
![Imatge](IMG/5.png)

Actualitzem el sistema a l'última versió

---

![Imatge](IMG/6.png)

Instal·lem el sistema vsftpd

---

![Imatge](IMG/7.png)

Iniciem sessió com a *root*

---

![Imatge](IMG/8.png)

Copiem l'arxiu en format **.bak*

---

![Imatge](IMG/9.png)

Ara, entrem en el fitxer i activem l'opció d'anonymous

---

![Imatge](IMG/10.png)

Reiniciem el sistema

---

![Imatge](IMG/11.png)

Confirmem l'estatus per veure que tot segueix funcionant correctament després dels canvis que hem fet

---

![Imatge](IMG/12.png)

Instal·lem **tree* per veure el sistema de fitxers

---

![Imatge](IMG/13.png)

Creem els directoris i creem un fitxer d'info a la carpeta *files* i una imatge a la carpeta *pics*
Amb el *tree* comprovem com està organitzat el sistema de carpetes dins del directori */srv/*

---

![Imatge](IMG/14.png)

Ara creem dos usuaris, *prova1* i *prova2*

---

![Imatge](IMG/15.png)

Tornem a entrar en el fitxer i han de quedar activades les 4 següents opcions
- listen_ipv6=YES
- anonymous_enable=YES
- local_enable=YES
- write_enable=YES

Ara, ja tindrem el servidor configurat, comprovem que sigui aixi reinician el sistema i veien l'estatus. Si tot segueix funcionant correctament, ja tenim el servidor

---

![Imatge](IMG/16.png)

Pasem al client, utilitzem un client Windows que també tindrà dos adaptadors, *NAT* i *Adaptador de només l'anfitrió*

---

![Imatge](IMG/17.png)

Instal·lem *FileZilla*

---

![Imatge](IMG/18.png)

Al entrar en FileZilla trobarem aquesta pantalla oon haurem de posar la IP que teniem en el servidor

---

![Imatge](IMG/19.png)

En el quadrat de l'estat ha d'apareixer un misatge com aquest indicant-nos que la connexió amb el servidor ha sigut correcte

---

![Imatge](IMG/20.png)

Entrem a la terminal de PowerShell y escribim la següent comanda:
ftp IP
Iniciarem sessió amb l'usuari del servidor que vulguem i la contrasenya assignada a aquell usuari

---

![Imatge](IMG/21.png)

Comprovem que el sistema segueix funcionan comprvant l'estatus des del servidor.

---

![Imatge](IMG/22.png)

I tambe la configuració del fitxer

---

![Imatge](IMG/24.png)

Iniciem sessió una altre cop en la terminal de PowerShell, aquesta vegada mab el usuari que hem creat de *prova1* i la contrasenya que li haguem posat

---

![Imatge](IMG/25.png)

Ara, en el fitxxer del servidor escriurem en el final de tot les següents dues linies:

---

![Imatge](IMG/26.png)

Després, guardarem la configuració, reiniciarem el servei i comprovarme l'estatus per veure que tot el servei segueix funcionant correctament

---

![Imatge](IMG/27.png)

Tornem a iniciar sessió amb l'usuari que hem creat i podem veure que funciona i troba els fitxers que hem creat anteriorment

---

![Imatge](IMG/28.png)

Ara, en el client instal·lem WireShark

---

![Imatge](IMG/29.png)

I comprovem que hi ha intercanvi de informació entre el sevidor i el client amb el protocol TCP o FTP
---

![Imatge](IMG/30.png)

Dins del servidor, com a *root*, crearem el següent directori

---

![Imatge](IMG/31.png)

I en el fitxer del servei, escriurem 6 linies més:
- ssl_sslv2=NO
- ssl_sslv3=NO
- ssl_stlsv1=NO

- force_local_data_ssl=YES
- force_local_logins_ssl=YES

I reiniciarem el sistema i comprovarem l'estat

---

![Imatge](IMG/32.png)

Ara, en el FileZilla, iniciem sessió amb la IP sel servidor i amb el nom i la contrasenya del usuari que hem cret, i podrem veure tots els seus directoris i fitxers

---

I amb aixó conclueix aquesta activitat pràctica.
