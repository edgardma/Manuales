## Artículos

[The Software Architecture Handbook](https://www.freecodecamp.org/news/an-introduction-to-software-architecture-patterns/)

## Arquitectura Orientada a Eventos (Event-Driven)

Trata sobre cómo conectar componentes a través de eventos. Cada componente publica eventos a un bus de eventos común y los componentes interesados a estos eventos pueden estar suscritos y luego responder al respecto.

No hay otra forma de comunicación, el bus de eventos pasa ser el método principal de comunicación entre componentes. Algo complejo es saber si una acción que hicimos tuvo el resultado que esperábamos, en general suelen ser eventualmente consistentes, lo que significa que cuando hacemos una escritura el sistema no nos garantiza que va a estar disponible hasta que ese evento no se distribuya en todas las partes que lo necesita.

**Provisión de eventos (EventSourcing).** En vez de que nuestra aplicación tenga el estado actual del sitio, podríamos tener solamente guardados los eventos que nos importan.

**Elementos:**

- Eventos

- Productores de eventos (publicadores)

- Consumidores de eventos (suscriptores)

- Bus de eventos

### Dieferencia entre un Topic y un Queue

La diferencia entre un Topic y un Queue es que en el caso de los Topic todos sus subscriptores reciben el mismo mensajes cuando el mensaje es publicado y en el caso de los Queue es que solo un receptor recibe el mensaje cuando este es depositado en la cola. *(Fuente: [Mensajería en las aplicaciones(Parte 2) | Java México](https://www.javamexico.org/blogs/jali/mensajeri_en_las_aplicaciones_parte_2#:~:text=La%20diferencia%20entre%20un%20Topic,es%20depositado%20en%20la%20cola.))*

### Diferencia entre SOAP y REST

SOAP y REST son dos enfoques distintos para la transmisión de datos en línea. Especificamente, ambas definen cómo diseñar API (Interfaces de Programación de Aplicaciones), las cuales permiten la comunicación de datos entre aplicaciones. REST es un conjunto de principios arquitectónicos; mientras SOAP es un protocolo oficial, cuyo mantenimiento está a cargo del Consorcio W3C. La principal diferencia es que SOAP es un protocolo, y REST no lo es. *(Fuente: [Diferencias entre REST y SOAP](https://www.redhat.com/es/topics/integration/whats-the-difference-between-soap-rest#:~:text=Diferencias%20entre%20SOAP%20y%20REST,-Es%20posible%20que&text=REST%20es%20un%20conjunto%20de%20pautas%20que%20ofrece%20una%20implementaci%C3%B3n,caso%20de%20la%20mensajer%C3%ADa%20XML.))*

# Los beneficios de la arquitectura de microservicios con Java y Spring Boot

La arquitectura de microservicios es una forma de diseñar y desarrollar aplicaciones complejas y escalables, basada en la división de la lógica de negocio en servicios independientes y colaborativos. Cada servicio se encarga de una funcionalidad específica, tiene su propio ciclo de vida y se comunica con los demás mediante protocolos ligeros, como HTTP o mensajes.

Java es uno de los lenguajes de programación más populares y versátiles del mundo, que ofrece un alto rendimiento, seguridad, portabilidad y una gran variedad de bibliotecas y herramientas. Spring Boot es un proyecto de Spring Framework que facilita la creación y el despliegue de aplicaciones basadas en Spring, proporcionando una configuración automática, un servidor embebido y una serie de características listas para usar.

Spring Boot y Spring Cloud son dos proyectos complementarios que ofrecen un conjunto de componentes y patrones para implementar microservicios con Java de forma rápida y eficiente. Algunos de estos componentes son:

- **Spring Cloud Config Server**: Permite centralizar y gestionar la configuración de los microservicios, facilitando el cambio dinámico de propiedades sin necesidad de reiniciar las instancias.
- **Spring Cloud Netflix Eureka**: Implementa el patrón de descubrimiento de servicios, que consiste en un registro donde los microservicios se registran y consultan la ubicación de otros servicios, permitiendo el escalamiento horizontal y el balanceo de carga.
- **Spring Cloud Netflix Zuul**: Implementa el patrón de API Gateway, que consiste en un punto de entrada único para todas las peticiones externas, que se encarga de enrutarlas al servicio adecuado, así como de aplicar filtros de seguridad, monitorización o transformación.
- **Spring Cloud LoadBalancer**: Proporciona un balanceador de carga del lado del cliente, que distribuye las peticiones entre las instancias disponibles de un servicio, teniendo en cuenta factores como el rendimiento, la latencia o la disponibilidad.
- **Spring Cloud Circuit Breaker**: Implementa el patrón de cortocircuito, que consiste en detectar y aislar los fallos en las comunicaciones entre servicios, evitando la propagación del error y permitiendo la recuperación o la ejecución de acciones alternativas.
- **Spring Cloud Sleuth y Zipkin**: Permiten implementar el rastreo distribuido, que consiste en seguir el flujo de una petición a través de los diferentes servicios involucrados, facilitando la depuración y la monitorización del comportamiento y el rendimiento del sistema.

Estos son solo algunos ejemplos de las ventajas que ofrece la arquitectura de microservicios con Java y Spring Boot. Con esta combinación se puede lograr una mayor agilidad, flexibilidad, escalabilidad y resiliencia en el desarrollo y despliegue de aplicaciones complejas, adaptándose a las necesidades cambiantes del mercado y ofreciendo una mejor experiencia al usuario final.

Origen: Conversación con Bing, 22/10/2023
(1) Microservicios con Spring Boot - Creando el Primer Microservicio. https://www.youtube.com/watch?v=-ksmE3KoX9U.
(2) Curso de microservicios en Java con Spring Boot y Spring Cloud. https://www.youtube.com/watch?v=2hhha1uIGXo.
(3) Curso #microservicios con #SpringBoot - 03 Microservicio Product y JPA. https://www.youtube.com/watch?v=0crp-uwM5Fo.
(4) Cómo crear y desplegar microservicios con Spring Boot, Spring Cloud .... https://www.adictosaltrabajo.com/2020/12/22/como-crear-y-desplegar-microservicios-con-spring-boot-spring-cloud-netflix-y-docker/.
(5) Microservicios con Spring Boot y Spring Cloud Netflix Eureka. https://www.udemy.com/course/microservicios-con-spring-boot-y-spring-cloud/.
(6) Microservicios con Spring Boot y Spring Cloud Netflix Eureka. https://bing.com/search?q=arquitectura+de+microservicios+con+Java+y+Spring+Boot.
(7) Curso de microservicios con Java y Spring Boot - EscuelaIT. https://escuela.it/cursos/curso-de-microservicios-con-java-y-spring-boot.
(8) undefined. https://www.paypal.com/donate/?hosted_button_id=GW79NV9RF22H6.
(9) undefined. https://github.com/digitallab-academy/ms-course-youtube.
(10) undefined. https://www.digitallab.academy/.