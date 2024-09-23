---
title: "Microkernel"
date: 2024-09-18 06:07:00 -0600
categories: [Desarrollo de software]
tags: [Arquitectura de software]
---

Es un estilo de arquitectura sencillo que también es llamado como micro-núcleo y tiene el siguiente estilo de topología.

![alt text](/assets/arq-031.png){: width="500" }

En esta topología se tiene un sistema o modulo central que hace la funcionalidad principal del sistema, después se suele enriquecer este modulo central con más funcionalidades mediante plug-ins.

Ejemplo de ello son los editores de código que vienen con una funcionalidad y principal y nosotros mismos le podemos agregar plug-ins que expanden y diversifican en gran medida las funcionalidades de los editores. También tenemos a los navegadores que tienen como función principal la búsqueda de información, nosotros podemos expandirlo con plug-ins/extensiones según sea el caso.

Debemos pensar en microkernel como un software donde la funcionalidad básica tiene muchas variaciones: un sistema de facturación en el cual para cada uno de los clientes se tienen variaciones diferentes respecto a los estados de la republica. Aquí el sistema central tiene una especie de plantilla y de acuerdo a cada una de la variaciones se genera un plug-in, de tal forma que permite que el sistema puede crecer y evolucionar de acuerdo a las variaciones.

El modulo central de nuestro sistema puede tener su propia arquitectura, por ejemplo: puede tener una arquitectura basada en eventos u otro sistema de microkernel o puede ser basada en capas. Aquí los estilos de arquitectura no son exclusivos. 

Una de las dificultades de esta arquitectura es como se va a definir una forma de crear plug-ins de manera que se comuniquen de manera sencilla. Una vez que se logra esto podemos extender nuestro software de una manera sencilla si tener que modificar el sistema central

![alt text](/assets/arq-032.png){: width="500" }

¿Cuándo usarla y cuando no?

Cuando usarla

- Cuando queramos distribuir software de manera sencilla y seguir mejorándolo después - caso de todos lo editores de texto.
- Cuando se busque que el software sea extensible - esta arquitectura nos puede permitir agregar plug-ins de manera casi infinita
- Cuando el caso de negocio tenga muchas variaciones - podemos pensar variaciones como leyes
- Cuando la funcionalidad central pueda servir para muchos casos -
- Cuando quieras una arquitectura más o menos simple

Cuando no usarla

- Cuando el performance sea muy importante - en esta arquitectura la comunicación con el módulo central y los plug-ins puede llegar a no ser tan eficiente.
- Cuando la tolerancia a fallos sea muy importante - también es una arquitectura monolítica, es por ello que no se lleva muy bien con la tolerancia a fallos.
- Cuando la escalabilidad sea muy importante - es difícil escalarlo para que acepte más peticiones por parte de los usuarios, al ser una arquitectura monolítica si e quiere hacer crecer este sistema es necesario que crezca en conjunto (tanto el módulo central como los plug-ins).





