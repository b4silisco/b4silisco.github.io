---
title: "Características no funcionales comunes"
date: 2024-09-09 06:07:00 -0600
categories: [Desarrollo de software]
tags: [Arquitectura de software]
---

Características no funcionales, comúnmente se les llama “características estructurales de calidad o arquitectónicas” y son las cosas que el sistema tiene como características de calidad, que además puede hacer, pero que no esta relacionado completamente con el dominio.

Son ampliamente importantes, debido a que se en algunas ocasiones el desarrollarlas requiere de conocer nuevos conceptos, adicional a ello debemos entender que estas características tiene cierto roce entre si, como ejemplo tenemos a el establecimiento de seguridad que puede no ser completado debido a un requerimiento de mantenibilidad, como se explicaba dentro del post de **Tradeoffs**. Aquí se hace un análisis de equilibrio que es muy especifico dependiendo del software que se este desarrollando y las necesidades que debe cubrir.

A continuación ejemplificamos algunas de estas características basándonos en preguntas

- Disponibilidad:
    - **¿Puedo acceder al sistema cuando lo necesito?**
    - **¿Cuánto tiempo pasa sin que pueda acceder por año, mes, semana o día?**
    - Se debe pensar como diseñador que tanto se requiere que el sistema este disponible. Debemos tener en cuenta que aumentar la disponibilidad a veces es muy caro. Suele ser expresada em porcentajes.

- Rendimiento
    - **¿Cuánto tiempo tarda en responder desde que sale mi petición?**
    - **¿Qué tan rápido es el sistema?**
    - **¿Cuánto tiempo tarda en completarse la tarea principal?**
    - Se define como que tan eficiente es al momento de responder el sistema ante las peticiones de los usuarios. Como es de suponer un sistema rápido supone costos elevados, nuestro trabajo como arquitectos de software es concientizar a los clientes sobre esta situación y tomar la mejor decisión para el desarrollo del proyecto.

- Extensibilidad
    - **¿Puedo agregar nuevas funcionalidades de manera sencilla?**
    - **¿Se pueden crear nuevas funciones sin programar?**
    - Mientras más extensible sea el sistema más difícil y costoso es de desarrollar respecto a recursos y habilidades técnicas.

- Escalabilidad
    - **¿Puedo hacer crecer el sistema para que atienda a más usuarios?**
    - **¿Cuánto esfuerzo se requiere para atender a más usuarios de manera simultánea?**
    - **¿Qué se requiere para que pueda procesar más datos/atender más peticiones?**
    - Es de las características que más se habla dentro del mundo del desarrollo de software, es de las más complicadas de implementar e inclusive la más cara, usualmente se habla dentro del entorno de startups.

- Tolerancia a fallos
    - **¿Puedo soportar fallos en el uso sin perder disponibilidad?**
    - **¿Puede seguir disponible aunque el hardware que lo soporta falle?**
    - **¿Qué pasa si se producen fallos intencionales?**
    - Todo esto puede lograrse mediante técnicas especificas que veremos más adelante. Sirve para evitar errores por parte de los usuarios, ya sea por que no sabe utilizar el software. Suele estar relacionada con la disponibilidad del sistema.

- Consistencia
    - **¿Es la misma información consultada a través de diferentes dispositivos u ocasiones?**

- Confiabilidad
    - **¿Se puede comprobar que la información que el sistema presenta es correcta y exacta?**
    - Se puede considerar como atributos intermedio entre los requerimientos funcionales y no funcionales.

- Seguridad
    - **¿Pueden acceder a la información solo usuarios autorizados?**
    - **¿Pueden acceder al sistema solo usuarios autorizados?**
    - **¿Esta protegido el sistema contra ataques de personas malintencionadas?**
        - Es el atributo de software más importante que existe actualmente. Al se tan importante el costo de su implementación es elevado, suele pelearse con otras características debido al choque que hay entre ellas.

- Auditabilidad
    - **¿Puedo saber qué es lo que esta pasando dentro del sistema?**
    - **¿Puedo inspeccionar la información para saber por qué esta respondiendo de cierta forma?**
    - Es requerido cuando se habla de temas gubernamentales, se busca responder que esta haciendo el sistema y saber por que esta haciendo.

- Monitoreabilidad
    - **¿El sistema comunica métricas sobre su estado actual?**
    - **¿Puedo agregar o expandir estas métricas de manera sencilla?**
    - Tiene que ver con el estado general del sistema

- Interoperabilidad
    - **¿Puede el sistema usarse fácilmente con otros sistemas?**
    - Se enfoca en que el sistema pueda complementarse con otros si tener que programar módulos extras.

Todas estas características sirven de ayuda para lograr los objetivos como arquitecto, se logra de dos formas: las cosas que tiene que ver con el dominio del negocio y las cosas que el software tiene como atributos que permiten que el software funcione de la manera en la que se espera.