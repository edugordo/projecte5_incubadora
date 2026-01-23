---
![Imatge](IMG/1.png)

Creem una "snapshot" de la maquina virtual per si alguna caso surt malament i per recuperarla en cas que no puguem treure el virus

---
![Imatge](IMG/2.png)

Obrim la màquina, entrem a Microsoft Edge i anem a la configuració del navegador

---
![Imatge](IMG/3.png)

Entrem en l'apartat de "Privacitat, cerca y serveis"

---
![Imatge](IMG/4.png)

A "seguretat" desactivem l'opció de "SmartScreen de Micrisift Defender" i la de "Bloquear aplicaciones potencialmente no deseadas"

---
![Imatge](IMG/5.png)

Entrem a la pàgina de "EICAR", pero abans de descarregar-nos el fitxer hem de fer unes coses

---
![Imatge](IMG/6.png)

Entrem a la configuració de la "seguretat de Windows" de la màquina

---
![Imatge](IMG/7.png)

Anem a "protecció antivirus y contra amenàçes"

---
![Imatge](IMG/8.png)

Desactivem dues opcions; 1. Proteccion en tiempo real, 2. Proteccion basada en la nube

---
![Imatge](IMG/9.png)

Ara si que podem descarregar el fitxer en format .zip

---
![Imatge](IMG/10.png)

Com podem veure, al desactivar la protecció antivirus de Windows, les descarregas es bloqueijen automàticament, el que hem de fer es anar a les opcions de la descarrega i sel·leccionar l'opció de "Baixa igualment". Aixi, el fitxer es continuarà baixant sense cap tipus de bloqueij.

---
![Imatge](IMG/11.png)

Quan ja tinguem el fitxer descarregat, entrem en l'explorador d'arxius i intentem entrar en la carpeta

---
![Imatge](IMG/12.png)

Ens sortirà aquesta alerta on no ens deixa entrar en la carpeta ni accedir a cap fitxer perque el sistema l'enten com a fitxer malintecionat o que conte alguna cosa persillosa per el sistema

---
![Imatge](IMG/13.png)

Ara ens descarregarem WinRAR des de qualsevol navegador

---
![Imatge](IMG/14.png)

Quan el tinguem descarregat, l'instal·larem

---
![Imatge](IMG/15.png)
![Imatge](IMG/16.png)

I quan ja el tinguem instal·lat, sel·leccionarem la carpeta de EICAR i en les opcions la comprimirem en format ZIP i en format 7s

---

![Imatge](IMG/17.png)

Quan intentem entrar en qualsevol d'aquests dos fitxers comprimits ens sortirà aquesta alerta de que el arxiu esta danyat o que té un format desconegut

---

Sistemes protecció Windows 11
1. Quines proteccions incorporar Windows 11 a la seccció de "Protección antivirus y contra amenazas"?
El mètode de protecció que implementa windows 11 és el Microsoft Defender, que a través d'escanejos i un historial d'amenaçes protejeix el equip en temps real ccontra malware i virus

2. Quines opcions tenim a "Control de aplicaciones y navegador"?
Es dedica a la protecció contra webs i aplicacions perillosses a base de aplicacións com SmartScreen, Smart App Control i el bloqueig d'aplicacions no desitjades

3. Investigueu quines opcions específiques hi ha per la protecció contra ransomware a Windows 11.
Windows 11 no xifra els fitxers gràcies a l'accés controlat de carpetes i permet la recuperació de dades a través de copies de seguretat a OneDrive

---

![Imatge](IMG/18.png)

Entrem en el GitHub "https://github.com/JoelGMSec/PSRansom i ens descarreguem el fitxer de LICENSE

---
![Imatge](IMG/19.png)

Ara obrim la terminal de PowerShell de Windows i posem les següents comandes:

Set-ExecutionPolicy -ExecutionPolicy Unrestricted

---
![Imatge](IMG/20.png)

I després, escriurem: 

./PSRansom.ps1 -e C:\Users\nomdelamaquina\Documents -s 127.0.0.1 -p

---
![Imatge](IMG/22.png)

Afegim 3 documents en format .txt a la carpeta de documents

---
![Imatge](IMG/23.png)

Desxifrem el fitxer de readme per veure la informació que conté dintre el fitxer. Dins trobarem una clau que haurem d'utilitzar seguidament en la terminal

---
![Imatge](IMG/24.png)

Haurem de posar una altre comanda en la terminal:

./PSRansom.ps1 -e C:\Users\nomdelamaquina\Documents -k "I la clau que ens doni el readme"

---
![Imatge](IMG/25.png)

Ara, comprovem que els fitxers no estan xifrats com anteriorment ho deia el fitxer de readme

---
![Imatge](IMG/26.png)

Ara descarreguem uns quants fitxers en diferents formats: .PNG, .JPG, .docx, .pdf

---
![Imatge](IMG/27.png)

Ara tornem a entrar en WinRAR i seleccionarem tots els fitxer que ens acabem de descarregar i els comprimirem en una carpeta en format .zip. Farem dues carpetes iguales, pero una li establirem una contrasenya i l'altre no li posarem res.

---
![Imatge](IMG/28.png)

info
---
![Imatge](IMG/29.png)

info
---

## Atacs de Ransomware: WannaCry

1. Llegiu la informació sobre WannaCry
https://www.avg.com/es/signal/wannacry-ransomware-what-you-need-to-know
i busqueu informació als enllaços dels projectes antiransomware per
contestar les preguntes següents:

2. Expliqueu quins són els factors que fan que WannaCry es propagui tan ràpid.
Expliqueu què vol dir.

WannaCry s'expandeix aprofitant equips sense actualitzar i es capaç d'infectar xarxes en molt poc temps  sense que l'usuari no pugui fer res al respecte

3. Quina vulnerabilitat en concret es fa servir? Busqueu el CVE associat. És
molt greu?

WannaCry utilitza la vulnerabilitat CVE‐2017‐0144, explotada per l’eina
EternalBlue. És una vulnerabilitat crítica, perquè permet execució remota de
codi i control total del sistema.

4. S'ha de pagar el rescat demanat? Per què? Busqueu per internet a veure si
trobeu alguna empresa negociadora de rescats i com funciona. Això s'està
fent, tot i que no se sol recomanar...

No s’ha de pagar perquè no garanteix recuperar les dades i incentiva més
atacs. Empreses com Coveware negocien rescats, però és una pràctica
desaconsellada per experts i autoritats.

5. Quines mesures podem aplicar si volem PREVENIR un atac de Ransomware
abans que passi?

Cal actualitzar Windows i aplicar pedaços de seguretat com el d’EternalBlue.
També és essencial tenir antivirus actualitzat, còpies de seguretat i evitar
arxius sospitosos.

6. Quines mesures aplicarem si JA HEM SOFERT un atac de WannaCry i no
hem aplicat les mesures de prevenció o ho hem fet parcialment?

Desconnectar l’equip de la xarxa i intentar recuperar dades de còpies de seguretat. Eliminar
el malware, no pagar, i reinstal·lar/actualitzar el sistema per evitar reinfeccions.

## Prova pràctica de WannaCry
