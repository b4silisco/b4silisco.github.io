---
title: "Basada en eventos (EDA)"
date: 2024-09-18 06:07:00 -0600
categories: [Desarrollo de software]
tags: [Arquitectura de software]
---

## Qué es la arquitectura basada en eventos
En este estilo de arquitectura principalmente se utiliza eventos para desacoplar y desencadenar la comunicación entre los distintos servicios y/o componentes del sistema.

Aquí entendemos como eventos como un cambio en el estado del sistema o una actualización de si mismo, al tener esta arquitectura podemos tener esta arquitectura como un sistema aislado o se puede combinar con otros estilos de arquitectura.

La arquitectura basada en eventos se basa en el cambio de eventos, tenemos una comunicación que se establece de manera asíncrona desencadenando flujos de trabajo.

En este estilo de arquitectura existen dos topologías:

![alt text](/assets/arq-033.png){: width="500" }

- Broker: es una topología en la cual se desencadenan los eventos de manera secuencial, lo que nos permite es tener un alto nivel de sensibilidad dentro del sistema teniendo un buen performance
- mediador: existe una figura central en la cual todos los eventos se comunican y se desencadena un flujo de trabajo.

![alt text](/assets/arq-034.png){: width="500" }

La topología broker se basa en un flujo donde los procesadores de los eventos desencadenan un flujo de manera continua, es muy útil cuando se tiene un flujo de procesamiento simple y no es necesaria orquestación.

En ella encontramos distintos componentes:

- Productor del evento: genera un evento inicial, se manda a través de la cola de mensaje s través de un broker que lo manda a un procesador de eventos
- Procesador de eventos: cuando el procesador de eventos recibe el evento desencadena un flujo de trabajo interno que a su vez desencadena un flujo de procesamiento, el evento se añade a una colla que a se pueden procesar o desencadenar a través de procesadores de eventos distintos y generando distintas funcionalidades.

Debemos tener en cuenta que dentro de esta topología los eventos pueden desencadenar 1 o más procesos de manera simultanea 

Ventajas:

- Desacoplamiento: tiene un índice de desacoplamiento alto
- Escalabilidad: es posible darle escalabilidad a cada uno de los componentes de manera individual
- Rendimiento: se tiene un buen rendimiento, debido a que el flujo no tiene intermediarios, por lo cual se aprovecha el poder de procesamiento de cada de los procesos, producer y brokers.
- Extensibilidad: es posible que esta topología expanda sus funcionalidades debido a la capacidad de generar más de un proceso por evento.

Desventajas:

Dentro de esta topología no se tiene un control sobre el flujo, por lo que es muy difícil saber si existen errores o perdidas de información. Por ello es complicado el manejo de errores es esta topología.

![alt text](/assets/arq-035.png){: width="500" }

En esta topología se tiene al mediador como principal componente y se encarga de manejar, controlar el flujo de trabajo y de iniciar los eventos que requieren coordinación dentro de los canales de eventos para ser recibidos por los procesadores de eventos que necesiten procesar.

Es decir lo que tenemos es: un productor de eventos el cual genera un evento inicial que se añade a una cola de mensajes, esta cola es monitoreada por el mediador y dependiendo del evento inicial coordina y orquesta los distintos canales a los cuales tiene que distribuir los eventos procesados, que a su vez son procesados por procesadores de eventos. Cuando los procesadores de eventos terminan su trabajo notifican al mediador de los procesos realizados.

De tal forma que podemos monitorear todo el flujo de trabajo. 

Ventajas:

- Control del flujo: ya que el mediador esta monitoreando y conoce el flujo de trabajo al realizar
- Manejo de errores: se puede implementar un mejor manejo de los errores
- Recuperabilidad: esto debido al monitoreo contante del flujo de trabajo
- Consistencia de los datos: al estar monitoreando de manera constante el flujo de trabajo podemos notar como se mueve la información dentro de los procesos.

Desventajas: 

- Acoplamiento entre procesadores
- Menor escalabilidad
- Menor tolerancia a fallos

¿Qué pasa si nosotros queremos comunicación síncrona en nuestro sistema?

Lo que podemos hacer es la implementación de una comunicación pseudosincrona a través de “Request - Reply”

![alt text](/assets/arq-036.png){: width="500" }

En este modelo tenemos un productor de eventos y un consumidor de eventos. En el proceso de estos eventos tenemos la siguiente serie de pasos:

- Primero se genera un mensaje
- Después de que se crea el mensaje ocurren dos cosas en simultaneo: el mensaje se pone en una cola de mensajes y por otro lado el productor de mensaje se pone en espera del mensaje (2).
- Luego se recibe el mensaje a través del consumidor de eventos (3), este lo procesa, trabaja con el y genera un nuevo mensaje de respuesta (4).
- Se agrega el nuevo mensaje a una cola de mensajes (5).
- Y por ultimo el productor de eventos acepta la cola de eventos, la recibe y la procesa (6).

Cuando usarla y cuando no

![alt text](/assets/arq-037.png){: width="500" }

