---
title: OverTheWire - Krypton
tags: [laboratorio, overthewire]
keywords: laboratorio, overthewire
summary: "Cómo resolver el laboratorio Bandit de OVerTheWire"
sidebar: mydoc_sidebar
permalink: mydoc_otw_krypton.html
folder: mydoc
topnav: topnav
---

## **Nivel 0 → Nivel 1**
{% include objetivo.html content="La siguiente cadena de texto es la contraseña del próximo nivel, esta encriptada en base64: **S1JZUFRPTklTR1JFQVQ=**" %}
{% include comandos.html content="echo, base64" %}
{% include callout.html content="Paso la cadena de texto con un **echo** al comando **base64 -d** para desencriptarlo." type="primary" %}
<link href="css/miEstilo.css" rel="stylesheet" type="text/css">
<div id="barra"><img src="images/terminal/botones.png" id="botones"><center id="texto_barra">verabelik.github.io</center></div>
<div id="terminal">echo 'S1JZUFRPTklTR1JFQVQ=' | base64 -d<br/>
KRYPTONISGREAT<br/>
</div>
{% include solucion.html content="KRYPTONISGREAT" %}