---
title: "Demostración de la creación, puesta en escena y commits"
date: 2024-08-09 08:50:00 -0600
categories: [Git y GitHub]
tags: [Git]
---

Ahora crearemos un nuevo fichero al que llamaremos **README.md**, es un archivo especial con la extensión markdown, es muy utilizado al momento de subir repositorios a sitios como GitHub.

![alt text](/assets/14-git.png){: width="600" }

Una vez que lo creamos escribimos un mensaje sobre él siguiendo las reglas de markdown y después de ello lo añadimos al stage de git.

![alt text](/assets/15-git.png){: width="600" }

Ahora bien si nosotros cambiamos de opinión y ya no queremos agregar este fichero o archivo al stage podemos quitarlo con el siguiente comando:


**git reset README.md**

![alt text](/assets/16-git.png){: width="600" }

Y veremos que VSCode nos marca este archivo como untrack, es decir que no se encuentra dentro del stage de git.

![alt text](/assets/17-git.png){: width="600" }

Si en un futuro yo edito el README es necesario hacer git add y git commit, esto quitaría un poco de tiempo, es por ello que haremos estas dos acciones en una sola línea de comando.

**git commit -am "Readme updated"**

![alt text](/assets/18-git.png){: width="600" }

Es necesario mencionar que este comando solo funciona si ya se ha dado seguimiento anterior al fichero.

Otro comando muy necesario es:

**git log**

Nos ayuda a ver los logs de mi repositorio.

![alt text](/assets/19-git.png){: width="600" }

Dentro de la información que nos ofrece ese comando esta lo siguiente:

**hash:**  este es único y nunca habrá dos commits que tengan el mismo hash, funge como identificador único del commit realizado.

![alt text](/assets/20-git.png){: width="600" }

**head:**  punto en el cual se encuentra la última versión de nuestro repositorio.

![alt text](/assets/21-git.png){: width="600" }

**author:**  Indica el autor que ha realizado ese commit proporcionando el nombre y su correo electrónico.

![alt text](/assets/22-git.png){: width="600" }

**date:**  Indica la fecha y la hora en la que se realizo el commit.

![alt text](/assets/23-git.png){: width="600" }

**mensaje:** en el se encuentra el mensaje que fue adjuntado al momento de hacer commit.

![alt text](/assets/24-git.png){: width="600" }


**Debemos tener en cuenta que los commits están ordenados del más reciente al más antiguo.**
