---
title: "Orientada a servicios (SOA)"
date: 2024-09-18 06:07:00 -0600
categories: [Desarrollo de software]
tags: [Arquitectura de software]
---

## ¿Qué es una arquitectura orientada a servicios?
Utiliza componentes de software llamados servicios (se pueden pensar como componentes o pedazos de código que nos sirven para desarrollar funcionalidades). Aquí mostraremos la topología correspondiente a este servicio.

![alt text](/assets/arq-038.png){: width="500" }

Esta arquitectura esta distribuida en distintos componentes, tenemos la interfaz del usuario en donde interactúa con el usuarios, a su vez se comunica con los distintos servicios que necesite invocar durante la interacción. La segunda parte lo conforman los servicios, tiene un desarrollo separado lo cual los hace independientes, se comunican con la base datos para las lectura y escritura de los datos. 

Es pragmática debido a que si necesitamos agregar una funcionalidad al sistema lo que se debe hacer es crear un nuevo servicio sin modificar los que ya existen.

Esta topología tiene distintas variantes

![alt text](/assets/arq-039.png){: width="500" }

En la primera variante tenemos añadida una capa de comunicación (en este caso una API) que separa las responsabilidades de comunicación desde la interfaz del usuario. Al separarlo con una nueva capa tenemos más control sobre el flujo. Aquí se mandan a llamar los servicios a través de la API que tiene las responsabilidades de cambio en las bases de datos. Al separarlo podemos implementar un rate limiter para minimizar riesgos de ataques cibernéticos.

![alt text](/assets/arq-040.png){: width="500" }

La segunda variante tiene una separación de la interfaz mediante el dominio. Aquí se hace enfoque en funcionalidades de acuerdo a roles de usuario, también se tiene una distinción entre los servicios que se conectan en estas interfaces.

![alt text](/assets/arq-041.png){: width="500" }

La ultima variante nos habla de una separación granular por servicios y dominios, podemos notar que el servicio 4 necesita una separación de la base de datos por el mecanismo que maneja. Esto es muy importante ya que no siempre tendremos una base de datos monolítica, sino que tendremos distintas bases de datos (esto nos ayuda con el control de duplicidad de dato o bases de datos demasiado complejas). 

Una vez que comprendemos estas topologías también debemos entender el concepto de granularidad de servicios. La granularidad de servicios hace referencia al tamaño de los servicios que existen dentro de un software.

![alt text](/assets/arq-042.png){: width="500" }

Tenemos dos opciones de diseño: por capas y por dominio

- Capas: cada servicio tiene una capa de comunicación (API) , negocio, (cumple con la lógica), persistencia (se encarga del manejo de la base de datos).
- Dominio: se tiene la misma capa de comunicación (API) dentro de ella se tiene distintos componentes a nivel de servicio (pueden ser módulos).

Ahora bien, si nosotros tenemos múltiples servicios el flujo de peticiones que se genera a la  base de datos la puede corromper, generando problemas en el sistema, para solventar este problema tenemos: federación de librerías (es la integración de librerías mediante el trabajo colaborativo de las mismas, son integradas en los servicios que las requieran) y partición en la base de datos (similar a la partición de discos en windows, la partición de bases de datos busca dividir los datos en fragmentos mas pequeños que se distribuyen en diferentes tablas o servidores).

![alt text](/assets/arq-043.png){: width="500" }

¿Cuándo debemos usarla y cuando no?

![alt text](/assets/arq-044.png){: width="500" }

