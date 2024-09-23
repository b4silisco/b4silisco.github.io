---
title: "Estilo en capas"
date: 2024-09-16 06:07:00 -0600
categories: [Desarrollo de software]
tags: [Arquitectura de software]
---

Se caracteriza por ser el más sencillo de entender, ejecutar, además de ello es barato de implementar. Tiene componentes que se posicionan uno sobre o otro o uno después de otro.

Lo que es bastante característico de esta arquitectura es que las capas solo pueden comunicarse entre la capa anterior y la capa que esta después de ella. Teniendo en cuenta el siguiente diagrama el objetivo de este estilo de arquitectura es que la capa 1 no tenga comunicación con la capa 4, esto evita que se tengan dependencias cruzadas y el software sea complejo de entender. A pesar de ser sencillo de implementar también se tiene variaciones de esta topología

![alt text](/assets/arq-027.png){: width="500" }

## Variantes de la topología

![alt text](/assets/arq-028.png){: width="500" }

Dependiendo de los requerimientos en ocasiones se necesitara que alguna capa tenga comunicación con una capa que no se debería tener comunicación. Esta capa es denominada “capa abierta”, esto hace que se rompa el estilo de arquitectura y también que la complejidad incremente en cierto grado. 

Para entender de mejor manera esto usaremos como ejemplo el patrón de arquitectura MVC

![alt text](/assets/arq-029.png){: width="500" }

Dentro de este patrón se manejan las capas de vista, controlador y modelo

- vista - es la capa que interactúa con los usuarios finales, puede ser mediante interfaces gráficas, apis u otro medio que permita a los usuarios usar el sistema.
- controlador - dirige las peticiones de los usuarios hacia el receptor que responderá a las peticiones que el usuario haga a través de la capa vista.
- modelo - encapsula el dominio del negocio, se asegura de que se cumpla con la funcionalidad del sistema, generalmente incluye la conexión con la base de datos y la persistencia.

## ¿Cómo sabemos cuando usarla y cuando no?

Es una manera muy fácil de organizar el software, este estilo evita el que se crucen componentes, peticiones y dependencias. Cuando se piensa en un sistema modular normalmente se divide las funciones del sistema en diferentes módulos, pero si se hace uso indiscriminado de todos los módulos respecto a todos los módulos se crea el llamado “código espagueti” que es muy difícil de mantener. 

La arquitectura en capas nos brinda una estructura que nos permite desarrollar el software de manera mantenible en el paso del tiempo. 

Se puede recurrir a esta arquitectura cuando no se han establecido completamente los requerimientos del software. Al ser simple y sencilla el implementar es rápido y no supone grandes costos.

![alt text](/assets/arq-030.png){: width="700" }

No debe usar se cuándo: 

Como se trata de un sistema “monolítico” es difícil que pueda dividirse para que diversas persona trabajen sobre el, de tal forma que el trabajo colaborativo representa complicaciones.

Si se requiere escalabilidad tendremos muchos problemas para implementarlo, en esta arquitectura si se quiere hacer crecer algo es necesario que crezca en conjunto, esto supone gastos adicionales, tiempo y personal.

