---
title: "Cambiar el nombre de la rama master a main"
date: 2024-08-05 09:20:00 +0800
categories: [Git y GitHub]
tags: [Git]
---

Dentro de git existe el concepto de ramas, este concepto hace referencia a un lugar en el que se puede encontrar trabajando, en este caso un repositorio puede tener bastantes ramas.

Es recomendable trabajar en ramas diferentes a la rama main o master, ya que esta rama suele estar destinada a tener los cambios que realmente queremos que se conserven dentro de nuestro proyecto.

**git branch**  
Este comando ayuda a localizar sobre que rama estamos trabajando dentro de nuestro repositorio

![alt text](/assets/10-git.png){: width="700" }

Ahora bien para cambiar el nombre de la rama master podemos hacer uso del siguiente comando:

**git branch -m master main**  
Aquí cambiamos el nombre de la rama principal master a main para su uso más adelante.

![alt text](/assets/11-git.png){: width="700" }

El cambio de nombre que hicimos hace un momento no es algo que este impactando de manera global, si no que solo se limita al repositorio sobre el cual estemos trabajando en el momento. Puede que si nosotros descargamos un repositorio de internet este ya contenga la rama como main aunque en algunos casos no será así. Es por ello que para configurar este nombre de manera global usamos:

**git config --global init.defaultBranch main**  
Con este comando indicamos que cada vez que implementamos git a un repositorio este coloque como nombre a la rama principal (anteriormente **master**) el nombre de **main**

![alt text](/assets/12-git.png){: width="700" }  

![alt text](/assets/13-git.png){: width="500" }