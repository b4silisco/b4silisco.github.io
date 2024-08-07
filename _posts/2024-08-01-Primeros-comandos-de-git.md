---
title: "Primeros comandos de git"
date: 2024-08-01 08:54:00 +0800
categories: [Git y GitHub]
tags: [Git]
---

**git --version**
Este comando nos ayuda a verificar que Git este completamente instalado y además arroja la versión con la que nosotros estamos trabajando

![alt text](/assets/01-git.png){: width="700" }

**git help**
Nos arroja la ayuda de Git, en ella nos muestra los comandos que podemos ejecutar y que parámetros requiere para funcionar

![alt text](/assets/02-git.png){: width="700" }

Antes de poder usar comandos e iniciar a trabajar con repositorios es necesario identificarnos para que Git sepa quienes somos.
Esto hace referencia a una configuración que de cierta forma es personal ya que nos ayudará a identificarnos dentro del repositorio.

**git config --global user.name "Fullbuster"**
Este comando toma como parámetro el user name para identificarnos y dentro de comillas indicamos el valor de este parámetro.

**git config --global user.email "quinthony35@gmail.com"**
Este comando asocia el nombre de usuario que anteriormente registramos como el correo para este usuario y mediante el nos identificarán incluso en la plataforma oficial de GitHub

**git config --global -e**
Lista todos los comandos que se hayan usado anteriormente.
