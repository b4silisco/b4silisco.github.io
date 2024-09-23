---
title: "Tradeoffs"
date: 2024-09-02 06:07:00 -0600
categories: [Desarrollo de software]
tags: [Arquitectura de software]
---

Son conocidos como compensaciones, en la arquitectura de software todo es un tradeoff, por lo cual es importante analizarlos, buscar ventajas y desventajas.

![alt text](/assets/arq-015.png){: width="600" }

Con ayuda de este gráfico podemos diferenciar distintos tipos de tradeoffs:

- El lado izquierdo representa tradeoffs con mayor impacto, es decir, que las decisiones que necesitamos analizar con mayor detalle y mayor tiempo generalmente corresponden a decisiones de arquitectura
- El lado derecho corresponde a decisiones que conllevan menos tiempo de analizar y menos tiempo de implementar, son tradeoffs del diseño de software.

Imaginemos un caso práctico donde tenemos un e-commerce que tiene distintos componentes y módulos.

![alt text](/assets/arq-016.png){: width="700" }

El contexto que usaremos como ejemplo es el carrito del e-commerce en donde se debe comunicar con la pasarela de pago y el control de inventario. 
La forma en que se puede implementar nos arroja dos opciones: tópicos y una serie de mensajes 

Del lado izquierdo se tiene la implementación por tópicos, aquí tenemos a el carrito que produce al tópico y los suscriptores (en este caso el consumidor de pagos y el consumidor de inventarios) reciben estas notificaciones y mensajes.

Del lado derecho tenemos una cola de mensajes, a través de colas independientes se manda mensajes distintos a cada uno de los consumidores.

Si nosotros comparamos estas dos formas de implementación podemos notar que la implementación por tópicos (izquierdo) es más escalable y extensible, si nosotros necesitamos agregar un nuevo consumidor, en este caso agregamos el historial de transacciones.

Ahora bien, si nosotros quisiéramos agregar un nuevo consumidor a a la cola de mensajes es necesario crear un mensaje independiente como una cola de mensajes.

De manera que en el lado izquierdo con la misma infraestructura solo suscribimos al consumidor y listo, mientras que del lado derecho a través de las colas de mensaje los cambios son más notorios.

![alt text](/assets/arq-017.png){: width="700" }

Si nosotros hacemos una comparación para obtener ventajas y desventajas tenemos lo siguiente:

- En la implementación por tópicos (lado izquierdo) el mensaje es homogéneo (igual) para todos los consumidores, entonces toda la información enviada es consumida por ellos, esto supone una carga de performance (por la carga de información adicional) y de seguridad (se comparte información idéntica que no debe tener acceso un consumidor)
- En la implementación mediante cola de mensajes (lado derecho) tenemos mensajes independientes, aquí no se tiene brecha de seguridad como en la otra implementación.

Aquí es donde el tema de análisis de tradeoffs cobra sentido en temas de seguridad y performance, esto debe ser comparado de acuerdo a el sistema, es decir aquí en este ejemplo la seguridad tiene mayor importancia que la extensibilidad y escalabilidad del sistema.

Por ultimo mencionar que no solo se tiene ventajas, sino que también existen desventajas y los mostramos en el siguiente gráfico.

![alt text](/assets/arq-018.png){: width="800" }

Implementación por tópicos

- Ventajas:
    - Extensibilidad y desacoplamiento:  Agregar un nuevo consumidor o servicio es relativamente fácil y sencillo.
- Desventajas:
    - Acceso generalizado a la información bajo el mismo contrato: todo los consumidores y servicios pueden acceder a toda la información.

Implementación de cola de mensajes:

- Ventajas:
    - Acceso granular y contratos únicos: cada consumidor solo tiene acceso a cierto tipo de información
- Desventajas:
    - Mantenibilidad y acoplamiento: al esta dividido en más módulos y servicios tiende a crecer de manera desmesurada en algunos casos, dificultando la mantenibilidad.