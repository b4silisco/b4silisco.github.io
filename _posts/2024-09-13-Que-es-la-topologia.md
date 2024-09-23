---
title: "Qué es la topología?"
date: 2024-09-13 06:07:00 -0600
categories: [Desarrollo de software]
tags: [Arquitectura de software]
---

## Definición de topología
Se puede definir como la composición abstracta de algo, nos ayuda con la representación de relaciones entre los nodos. Podemos imaginarlo como un estilo de arquitectura que define las relaciones entre componentes, como tal no es la forma exacta, sino la forma abstracta de un sistema que se puede moldear para que cumpla con los requerimientos específicos del sistema. 

Estas son las topologías más comunes en arquitectura de software:

- Monolítica - En ella los componentes del sistema están integrados en un solo bloque o unidad. Todas la funcionalidades residen en una única aplicación.
    - **Ejemplo**: Una aplicación web tradicional donde la lógica de negocio, la interfaz de usuario y la gestión de datos están contenidas en un solo proyecto.

![alt text](/assets/arq-021.jpg){: width="300" }

- Cliente/Servidor - El sistema se divide en dos componentes principales: el cliente, que interactúa con el usuario, y el servidor, que gestiona la lógica de negocio y los datos.
    - **Ejemplo**: Una aplicación web donde el navegador actúa como cliente y un servidor web procesa las solicitudes y devuelve las respuestas.

![alt text](/assets/arq-022.png){: width="500" }

- Arquitectura de microservicios - El sistema se divide en servicios pequeños e independientes que se comunican entre sí a través de APIs. Cada microservicio se encarga de una parte específica de la funcionalidad total del sistema.
    - **Ejemplo**: Un sistema de comercio electrónico donde los servicios de pago, inventario y gestión de usuarios están separados y se comunican entre ellos a través de servicios web.

![alt text](/assets/arq-023.png){: width="500" }

- Arquitectura en capas - El sistema se organiza en capas que cumplen diferentes responsabilidades, como presentación, lógica de negocio y acceso a datos. Cada capa se comunica con la adyacente.
    - **Ejemplo**: Una aplicación empresarial donde la interfaz de usuario, la lógica de negocio y la base de datos están separadas en capas distintas.

![alt text](/assets/arq-024.png){: width="500" }

- Arquitectura en malla - Los servicios en una arquitectura de malla están conectados entre sí de manera más dinámica y flexible, permitiendo la comunicación directa entre ellos sin pasar por un intermediario central.
    - **Ejemplo**: Un sistema de microservicios que utiliza un servicio de malla para manejar la comunicación entre servicios sin tener que pasar por un controlador o API Gateway central.

![alt text](/assets/arq-025.png){: width="500" }

- Arquitectura orientada a eventos - Los componentes del sistema se comunican a través de eventos, donde un evento desencadena la ejecución de uno o más componentes sin necesidad de una interacción directa.
    - **Ejemplo**: Un sistema de notificaciones que envía correos electrónicos automáticamente cuando se produce un evento específico, como la creación de una nueva cuenta de usuario.

![alt text](/assets/arq-026.png){: width="500" }

También es importante tener en cuenta que la topología afecta directamente la escalabilidad, mantenibilidad y el rendimiento del sistema. Por lo tanto el elegir la teología del sistema influye directamente en el comportamiento y las capacidades del sistema en producción. 

