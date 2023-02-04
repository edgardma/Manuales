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
