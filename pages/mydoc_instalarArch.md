---
title: Instalar Arch
tags: [sistemas operativos, arch]
keywords: instalacion, arch, sistemas, operativos, sistemas operativos
last_updated: 27 Febrero 2022
summary: "Como realizar la instalación de Arch a través de su instalador."
sidebar: mydoc_sidebar
permalink: mydoc_instalarArch.html
folder: mydoc
topnav: topnav
---

## 1 - Bootear Arch desde un pendrive
![Image text](images/InstalarArch/01.png)

## 2 - Archinstall
Usar el comando **archinstall** para comenzar la instalación.

## 3 - Seleccionar espejo
Seleccionar el espejo desde el que queremos realizar las descargas. Elegiremos el país más cercano, en mi caso España.

## 4 - Idioma del teclado
Elegiremos el idioma de nuestro teclado escribiendo el número que aparece al lado de las iniciales del país.

## 5 - Discos
Seleccionamos el disco donde queremos hacer la instalación.

## 6 - Eliminar disco
Seleccionamos que queremos eliminar el disco completo.

## 7 - Sistema de ficheros
Escogemos que sistema de ficheros queremos usar.

## 8 - Estructura
Le decimos que queremos una estructura por defecto del sistema escogido.

## 9 - Encriptación
Si queremos podemos encriptar el sistema añadiendo una contraseña.

## 10 - Swap
Dependiendo de la potencia de nuestro equipo podemos utilizar una partición de swap.

## 11 - Nombre de la máquina
Escogemos un nombre para nuestra máquina.

## 12 - Contraseña root
Escribimos la contraseña para el usuario root.

## 13 - Nuevo usuario
Añadimos un nombre y una contraseña para crear nuestro usuario.

## 14 - Sudoers
Escribimos Y para añadir el nuevo usuario a la lista de superusuarios.

## 15 - Instalación mínima
Seleccionamos la opción 3 para tener una instalación de software mínima.

## 16 - Drivers
Instalamos los drivers de nuestra tarjeta grafica y de la tarjeta de sonido.

## 17 - Kernel
Escogemos el kernel que queremos instalar.

## 18 - Software
Si queremos añadir algún otro programa podemos escribirlo en este moento, separado por comas. Yo aprovecho para instalar un navegador web.

## 19 - Internet
Necesitamos escoger la interfaz de internet. Tenemos 3 posibilidades: Copiar la misma configuración que tenemos ahora mismo en la instalación, usar NetworkManager para seleccionar una red de forma gráfica, o seleccionar la red enp0s3 que en mi caso es la red cableada.

## 20 - Hora
Seleccionamos la zona horaria y le decimos que la actualice automaticamente.

## 21 - Resumen
Ahora nos mostrará un resumen con toda las configuraciones que hemos seleccionado.Una vez estemos conformes y le demos enter comenzará la instalación.

## 23 - Reiniciar el sistema