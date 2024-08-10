---
title: "Nuestro primer repositorio"
date: 2024-08-01 09:07:00 +0800
categories: [Git y GitHub]
tags: [Git]
---

Dentro del mundo de git y github los proyectos se gestionan por carpetas, sin embargo a estas se les suele llamar *repositorios*

**git init**  
Este comando nos ayuda a inicializar git dentro de un repositorio, para ello ya debemos ubicarnos dentro de ella.

![alt text](/assets/03-git.png){: width="700" }

Una vez que se ha ejecutado el comando podemos notar que nuestra rama principal se llama master, sin embargo en la actualidad muchas personas pueden considerar esto ofensivo, es por ello que lo recomendable es llamar a nuestra rama principal main, esto podemos hacerlo mediante el siguiente comando

**git config --global init.defaultBranch main**  

Dejando estas recomendaciones un poco de lado, una vez que nosotros inicializamos git en un repositorio, este generará una carpeta oculta llamada .git la cual contendrá todos los estados y cambios que generemos en nuestro repositorio, es de suma importancia resguardar bien esta carpeta y no dejar perderla por ningún motivo.

![alt text](/assets/04-git.png){: width="300" }

**git atatus**  
Este comando nos da información sobre los commits, ramas en las que nos encontramos.
Asimismo hace un sondeo acerca de que archivo y ficheros no están listos para usarlos con git, para poderle indicar esto a git podemos usar el siguiente comando:

![alt text](/assets/05-git.png){: width="700" }

**git add**  
Nos permite indicar a git que archivo y ficheros queremos que usen y se mantengan bajo versiona miento por git

![alt text](/assets/06-git.png){: width="700" }

Ahora, observamos que tenemos bastantes ficheros y por lo tanto agregar uno por uno puede ser tedioso, es por ello que podemos hacer uso del siguiente comando:

**git add .**

![alt text](/assets/07-git.png){: width="700" }

![alt text](/assets/08-git.png){: width="700" }

Habrá ocasiones en las que agreguemos ficheros que no queramos que sean versionados por git, para quitar este versionamiento del fichero podemos usar el comando:

**git reset .Ds_Store**

Ahora que ya tenemos a las ficheros para guardar una fotografía de sus cambios podemos hacerlo mediante

**git commit -m "Primer commit"**  
Este comando nos permite asignar la fotografía de nuestro repositorio y además nos permite agregar un mensaje que se adjuntará a este commit

![alt text](/assets/09-git.png){: width="700" }


