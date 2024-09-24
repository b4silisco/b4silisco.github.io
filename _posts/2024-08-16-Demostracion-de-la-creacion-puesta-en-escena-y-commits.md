---
title: "Demostración de la creación, puesta en escena y commits"
date: 2024-08-16 08:50:00 -0600
categories: [Git y GitHub]
tags: [Git]
---

Ahora crearemos un nuevo fichero al que llamaremos README.md. Este es un archivo especial con la extensión Markdown, que se utiliza frecuentemente al subir repositorios a plataformas como GitHub. Este archivo permite proporcionar información importante sobre el proyecto, como su propósito, cómo instalarlo y usarlo, así como cualquier otra información relevante que los colaboradores y usuarios deban conocer.

![alt text](/assets/14-git.png){: width="600" }

Una vez que creamos el archivo README.md, escribimos un mensaje sobre él siguiendo las reglas de Markdown. Esto puede incluir encabezados, listas, enlaces, imágenes y otros elementos que ayuden a estructurar la información de manera clara y concisa.

Después de redactar el contenido, lo añadimos al stage de Git, utilizando el comando adecuado. Esto permite que los cambios realizados en el archivo sean registrados en la próxima confirmación (commit).

![alt text](/assets/15-git.png){: width="600" }

Ahora bien, si nosotros cambiamos de opinión y ya no queremos agregar este fichero o archivo al stage, podemos quitarlo con el siguiente comando:


**git reset README.md**

![alt text](/assets/16-git.png){: width="600" }

Y veremos que VSCode nos marca este archivo como untracked, es decir, que no se encuentra dentro del stage de Git.

![alt text](/assets/17-git.png){: width="600" }

Si en un futuro edito el README, es necesario hacer git add y git commit; esto quitaría un poco de tiempo. Es por ello que haremos estas dos acciones en una sola línea de comando.

**git commit -am "Readme updated"**

![alt text](/assets/18-git.png){: width="600" }

Es necesario mencionar que este comando solo funciona si ya se ha dado seguimiento previo al fichero.

Otro comando muy necesario es:

**git log**

Nos ayuda a ver los logs de mi repositorio.

![alt text](/assets/19-git.png){: width="600" }

Dentro de la información que nos ofrece ese comando esta lo siguiente:

**hash:**  Este es único y nunca habrá dos commits que tengan el mismo hash; funge como identificador único del commit realizado.

![alt text](/assets/20-git.png){: width="600" }

**head:**  punto en el cual se encuentra la última versión de nuestro repositorio.

![alt text](/assets/21-git.png){: width="600" }

**author:**  Indica el autor que ha realizado ese commit proporcionando el nombre y su correo electrónico.

![alt text](/assets/22-git.png){: width="600" }

**date:**  Indica la fecha y la hora en la que se realizo el commit.

![alt text](/assets/23-git.png){: width="600" }

**mensaje:** en el se encuentra el mensaje que fue adjuntado al momento de hacer commit.

![alt text](/assets/24-git.png){: width="600" }


**Debemos tener en cuenta que los commits están ordenados de más reciente a más antiguo.**
