---
title: "Arquitectura vs diseño"
date: 2024-08-30 06:07:00 -0600
categories: [Desarrollo de software]
tags: [Arquitectura de software]
---

Dentro del proceso de desarrollo de software debemos tener en cuenta en donde empieza y donde termina la arquitectura y el diseño de software. Cual es la responsabilidad de la arquitectura y la responsabilidad del diseño de software. 

Nos ayuda a definir quien tiene que tomar las decisiones y quienes deben colaborar durante el proceso. Que tanto colaboran arquitectos y desarrolladores.

![alt text](/assets/arq-013.png){: width="600" }

En este grafico se hace notar del lado izquierdo se denotan todas la decisiones que corresponden a la arquitectura de software y en el lado superior derecho las decisiones respecto al diseño. de software. En el medio podemos definir que se encuentra el punto de colaboración entre desarrolladores y arquitectos.

Si nos enfocamos en la imagen nosotros podemos decir que para determinar el tipo de decisión se toman los siguientes criterios:

- Si la decisión tiene que ver más con estrategia se puede decir que es de arquitectura. Cuando se dice estrategia se incluyen decisiones que tiene implicaciones a largo plazo, esta decisiones tiene impacto directo sobre otras
- Si la decisión tiene que ver con táctica se dice que no tiene una correlación sobre otras, por lo cual se consideran independientes.

A continuación damos algunos ejemplos de decisiones:

- Decisión de arquitectura: cambiar el estilo de arquitectura de monolito a microservicios. Este tipo de decisiones conlleva a un esfuerzo mayor que una decisión, como lo puede ser partir un servicio en distintos servicios.

Como se puede observar las dos figuras que se desarrollan en este contexto son tanto el desarrollador como el arquitecto

![alt text](/assets/arq-014.png){: width="600" }

Para el arquitecto las principales funciones son:

- Determinar las características que corresponde al sistema, estas características se obtienen directamente de las necesidades de las funcionalidades que el negocio necesita
- Determina el estilo, que estilo se adapta mejor a las necesidades del negocio
- Denotar las decisiones de arquitectura, respecto a que modelos se deben utilizar
- Principios, nos ayuda a proporcionar un marco de desarrollo de código limpio, mantenible y escalable
- Interacción de los componentes, como se comunican los componentes en las distintas fases evolutivas del sistema

A través de establece y tomar decisiones de acuerdo a la arquitectura se crean artefactos, que más adelante el desarrollador debe desarrollar.

- Clases: que clases se implementan y componen el sistema
- UI: hace referencia a la interfaz gráfica que tiene el sistema
- Código: el desarrollo del código que hace funcional el sistema





