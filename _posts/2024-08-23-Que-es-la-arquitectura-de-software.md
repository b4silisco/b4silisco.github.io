---
title: "¿Qué es la arquitectura de software?"
date: 2024-08-23 06:07:00 -0600
categories: [Desarrollo de software]
tags: [Arquitectura de software]
---

## Arquitectura de software

Es un concepto muy utilizado en la industria de la tecnología, a pesar de que hay distintas definiciones para este concepto no existe un estándar que lo defina.

Nosotros tomaremos dos definiciones:

- La primera es de Martin Fowler que define la arquitectura de software como las distintas cosas que son difíciles de cambiar
- La segunda de Ralph Johnson que enuncia que la arquitectura de software son todas la cosas importantes.

En otras definiciones se suele hacer referencia a los planos arquitectónicos de una casa, esto llevado al software podemos imaginar los planos bien definidos de los componentes, como interactúan entre si y como esta construido el sistema.

![alt text](/assets/arq-001.png){: width="200" }

También se tiene el plano a un roadmap que hace referencia a como se va desarrollando el sistema en el tiempo.  

![alt text](/assets/arq-002.png){: width="400" }

![alt text](/assets/arq-003.png){: width="600" }

Debido a que existen múltiples definiciones nos enfocaremos en 4 dimensiones: 

- Características del sistema (requerimientos no funcionales): normalmente se asocian a requerimientos técnicos y cualidades de un sistema, definen el criterio de éxito de un sistema. Son requeridos para que el sistema funcione de manera correcta
    - Ejemplos: disponibilidad, seguridad, escalabilidad

![alt text](/assets/arq-004.png){: width="500" }

- Decisiones arquitectónicas: son reglas de como se tiene que construir el sistema. Es buena práctica poner las decisiones en un documento y explicar el porque se toman esas decisiones. En general son restricciones que impactan la implementación de los desarrolladores.
    - Ejemplo: se puede definir que la capa de presentación no tendrá acceso a la base de datos, solamente se tiene acceso a la base de datos a través de una capa de servicios o de negocios.

![alt text](/assets/arq-005.png){: width="500" }

- Principios de diseño: son una guía de implementación del sistema.
    - Ejemplo: poner un principio de diseño como apalancamiento de mensajería entre diseños, mejorando el èrformance

![alt text](/assets/arq-006.png){: width="500" }

Estilo arquitectónico: generalmente se refiere al estilo o la estructura, cuando nos preguntan sobre la arquiectura del sistema generalmente hablamos de esta dimensión.

![alt text](/assets/arq-007.png){: width="500" }

**4 dimensiones de la arquitectura de software**

![alt text](/assets/arq-008.png){: width="600" }