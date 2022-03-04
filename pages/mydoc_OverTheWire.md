---
title: OverTheWire Bandit
tags: [laboratorio, overthewire]
keywords: laboratorio, overthewire
last_updated: 4 Marzo 2022
summary: "Cómo resolver el laboratorio Bandit de OVerTheWire"
sidebar: mydoc_sidebar
permalink: mydoc_overthewire.html
folder: mydoc
topnav: topnav
---

## **Nivel 0**
{% include objetivo.html content="Debemos conectarnos al laboratorio mediante una conexion SSH. <br/>
**→ Host:** bandit.labs.overthewire.org<br/>
**→ Puerto:** 2220<br/>
**→ Usuario:** bandit0<br/>
**→ Contraseña:** bandit0<br/>
" %}
{% include comandos.html content="ssh" %}
{% include callout.html content="Para conectarme mediante ssh solo necesito saber que el comando **ssh** funciona de la siguiente manera:<br/>&nbsp;&nbsp;&nbsp;&nbsp;→	ssh usuario@[host] -p [puerto]<br/>**Ejemplo:** ssh admin@mi.conexion.org -p 2222" type="primary" %}
<link href="css/miEstilo.css" rel="stylesheet" type="text/css">
<div id="barra"><img src="images/terminal/botones.png" id="botones"><center id="texto_barra">verabelik.github.io</center></div>
<div id="terminal">
ssh bandit0@bandit.labs.overthewire.org -p 2220<br/>
bandit0@bandit.labs.overthewire.org's password: bandit0<br/>
bandit0@bandit:~$
</div>
<br/>

## **Nivel 0 → Nivel 1**
{% include objetivo.html content="La contraseña del siguiente nivel esta almacenada en un archivo llamado **readme** localizado en el directorio **home**." %}
{% include comandos.html content="ls, cat" %}
{% include callout.html content="Realizo un **ls** para ver el contenido de la carpeta y un **cat [archivo]** para imprimir el contenido del archivo:" type="primary" %}
<link href="css/miEstilo.css" rel="stylesheet" type="text/css">
<div id="barra"><img src="images/terminal/botones.png" id="botones"><center id="texto_barra">verabelik.github.io</center></div>
<div id="terminal">ssh bandit0@bandit.labs.overthewire.org -p 2220<br/>
bandit0@bandit:~$ ls<br/>
readme<br/>
bandit0@bandit:~$ cat readme<br/>
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
</div>
{% include solucion.html content="boJ9jbbUNNfktd78OOpsqOltutMc3MY1" %}

## **Nivel 1 → Nivel 2**
{% include objetivo.html content="La contraseña del siguiente nivel esta almacenada en un archivo llamado **-** localizado en el directorio **home**." %}
{% include comandos.html content="ls, cat" %}
{% include callout.html content="Hago un **ls** para ver el contenido de la carpeta y un **cat ./[archivo]** para imprimir el contenido del archivo:" type="primary" %}
<link href="css/miEstilo.css" rel="stylesheet" type="text/css">
<div id="barra"><img src="images/terminal/botones.png" id="botones"><center id="texto_barra">verabelik.github.io</center></div>
<div id="terminal">ssh bandit1@bandit.labs.overthewire.org -p 2220<br/>
bandit1@bandit:~$ ls<br/>
-<br/>
bandit1@bandit:~$ cat ./-<br/>
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9<br/>
</div>
{% include solucion.html content="CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9" %}

## **Nivel 2 → Nivel 3**
{% include objetivo.html content="La contraseña del siguiente nivel esta almacenada en un archivo llamado **spaces in this filename** localizado en el directorio **home**." %}
{% include comandos.html content="ls, cat" %}
{% include callout.html content="Hago un **ls** para ver el contenido de la carpeta y un **cat 'archivo'** para imprimir el contenido del archivo:" type="primary" %}
<link href="css/miEstilo.css" rel="stylesheet" type="text/css">
<div id="barra"><img src="images/terminal/botones.png" id="botones"><center id="texto_barra">verabelik.github.io</center></div>
<div id="terminal">ssh bandit2@bandit.labs.overthewire.org -p 2220<br/>
bandit2@bandit:~$ ls<br/>
spaces in this filename<br/>
bandit2@bandit:~$ cat "spaces in this filename"<br/>
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK<br/>
</div>
{% include solucion.html content="UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK" %}

## **Nivel 3 → Nivel 4**
{% include objetivo.html content="La contraseña del siguiente nivel esta almacenada en un archivo oculto localizado en el directorio **inhere**." %}
{% include comandos.html content="ls, cat" %}
{% include callout.html content="Hago un **ls -la** para ver el contenido oculto de la carpeta y un **cat 'direccion_archivo'** para imprimir el contenido del archivo:" type="primary" %}
<link href="css/miEstilo.css" rel="stylesheet" type="text/css">
<div id="barra"><img src="images/terminal/botones.png" id="botones"><center id="texto_barra">verabelik.github.io</center></div>
<div id="terminal">ssh bandit3@bandit.labs.overthewire.org -p 2220<br/>
bandit3@bandit:~$ ls -la inhere/<br/>
total 12<br/>
drwxr-xr-x 2 root    root    4096 May  7  2020 .<br/>
drwxr-xr-x 3 root    root    4096 May  7  2020 ..<br/>
-rw-r----- 1 bandit4 bandit3   33 May  7  2020 .hidden<br/>
bandit3@bandit:~$ cat inhere/.hidden <br/>
pIwrPrtPN36QITSp3EQaw936yaFoFgAB<br/>
</div>
{% include solucion.html content="pIwrPrtPN36QITSp3EQaw936yaFoFgAB" %}

## **Nivel 4 → Nivel 5**
{% include objetivo.html content="La contraseña del siguiente nivel esta almacenada en un archivo de lectura humana en el directorio **inhere**." %}
{% include comandos.html content="ls, cat, file" %}
{% include callout.html content="Hago un **ls** para ver el contenido de la carpeta y un **file inhere/*** para ver los tipos de archivos. Una vez que ya se que archivo necesito, uso un **cat** para ver su contenido:" type="primary" %}
<link href="css/miEstilo.css" rel="stylesheet" type="text/css">
<div id="barra"><img src="images/terminal/botones.png" id="botones"><center id="texto_barra">verabelik.github.io</center></div>
<div id="terminal">ssh bandit4@bandit.labs.overthewire.org -p 2220<br/>
bandit4@bandit:~$ ls inhere/<br/>
-file00  -file02  -file04  -file06  -file08<br/>
-file01  -file03  -file05  -file07  -file09<br/>
bandit4@bandit:~$ file inhere/*<br/>
inhere/-file00: data<br/>
inhere/-file01: data<br/>
inhere/-file02: data<br/>
inhere/-file03: data<br/>
inhere/-file04: data<br/>
inhere/-file05: data<br/>
inhere/-file06: data<br/>
inhere/-file07: ASCII text<br/>
inhere/-file08: data<br/>
inhere/-file09: data<br/>
bandit4@bandit:~$ cat inhere/-file07<br/>
koReBOKuIDDepwhWk7jZC0RTdopnAYKh<br/>

</div>
{% include solucion.html content="koReBOKuIDDepwhWk7jZC0RTdopnAYKh" %}