# 🖥️ T06: Configuració del domini

## 📌 Breu descripció
Un cop creat el domini, el següent pas és **desplegar-lo**, és a dir, crear i organitzar els diferents objectes que el formaran: **unitats organitzatives (OU), grups, usuaris i equips**.  
En aquesta pràctica es treballa la importància d’una **estructura ordenada i escalable** dins d’un entorn de domini.

---

## 📖 Introducció
La correcta configuració del domini permet una **administració eficient** dels recursos i usuaris.  
Mitjançant l’ús d’**Unitats Organitzatives (OU)**, podem aplicar polítiques, permisos i configuracions de manera estructurada i flexible.

---

## ⚙️ Procediment pràctic

### 🗂️ 1. Crear l’estructura d’Unitats Organitzatives (OU)
Crear una estructura d’OU adequada per organitzar usuaris, grups i equips del domini.

---

### 👥 2. Definir l’estructura de grups
Crear els següents grups de seguretat:

- **gestio**
- **magatzem**
- **gerencia**
- **personal**  
  > 🔹 *Aquest grup ha de contenir com a membres tots els grups anteriors.*

---

### 🧑‍💼 3. Crear plantilles d’usuari
Crear una plantilla d’usuari per a cadascun dels grups següents:

- **Gestio**
- **Magatzem**
- **Gerencia**

Cada plantilla ha de tenir:
- ✅ Pertinença al grup corresponent  
- 📁 Carpeta personal creada automàticament

---

### 👤 4. Crear usuaris de prova
Definir **un usuari de prova** per a cadascuna de les plantilles creades anteriorment.

---

### 💻 5. Aprovisionar un equip
- Crear una OU anomenada **equips**
- Aprovisionar un equip amb el nom **PC1** dins d’aquesta OU

---

### 🪟 6. Crear una màquina virtual client
Crear una **VM amb Windows 11** amb les següents característiques:
- 💾 **4 GB de RAM**
- 📀 **Disc amb espai suficient**
- 🌐 **Xarxa NAT**

Un cop creada:
- 🔗 Afegir l’equip al **domini**

---

### ✅ 7. Comprovació del funcionament
- Iniciar sessió a l’equip **PC1**
- Comprovar l’accés correcte amb:
  - 👤 Usuari de Gestio
  - 👤 Usuari de Magatzem
  - 👤 Usuari de Gerencia

---

## 📚 Materials i links de suport
- **UD6.AA3 Desplegament**  
  📘 *Moodle 0224 – SOX*

