---
title: "Por qué nos interesa saber Git o un sistema de control de versiones"
date: 2024-08-02 08:50:00 -0600
categories: [Git y GitHub]
tags: [Git]
---

Cuando se tiene un control de versiones, hacemos uso de una especie de máquina del tiempo, ya que, mediante ella, podremos viajar a distintas temporalidades dentro de un proyecto de programación.

Dentro de Git, a los proyectos se les suele llamar repositorios. Dentro de este concepto, existen diferentes tipos:

*Repositorio central: Hace referencia a un servidor que contiene todos los archivos o ficheros del proyecto. Usualmente, no existen copias o backups de este proyecto y su contenido, lo que también dificulta su uso cuando trabajan varios desarrolladores en él.*

*Repositorio distribuido: Este tipo de repositorio se enfoca en asignar a cada desarrollador una copia del proyecto, sobre la cual podrán realizar modificaciones. A su vez, en caso de pérdida de estos ficheros, se asegura que otro desarrollador tenga una copia del proyecto para sustituir la pérdida.*

## ¿Cómo funciona Git?

Su funcionamiento se puede ejemplificar con la toma de capturas de nuestro código a través de cada modificación, generando así un historial de las modificaciones realizadas durante el periodo de vida del proyecto.