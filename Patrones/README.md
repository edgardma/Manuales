# Patrones de diseño

## Escenarios:

1. Supongamos que quiero crear una aplicación, por ejemplo, una aplicación de administración de Kafka, que se utilizará para crear, eliminar, obtener y modificar temas de Kafka en el clúster de Kafka.
¿Qué patrón de diseño de comportamiento sería adecuado en este escenario? **-> Patrón de comandos** 

2. ¿Qué patrón de diseño le permite alterar el comportamiento de un objeto en tiempo de ejecución asociándolo con diferentes subobjetos para realizar varias tareas? **-> Patrón de estrategia**

3. Supongamos que está trabajando en un sistema de gestión de imágenes. Está viendo un problema de rendimiento con una página, porque cada vez que un usuario abre esa página, el sistema tiene que cargar un conjunto de imágenes grandes.
Desea implementar un mecanismo de carga diferida para cargar cada imagen solo cuando sea necesario. ¿Qué patrón de diseño sería apropiado para esto? **-> Patrón de proxy**

4. Los objetos de fachada a menudo son '¿qué patrón de diseño?' porque solo se requiere un objeto de fachada. **-> Patrón Singleton**

5. Ha implementado un patrón de estado y cada estado mantiene una referencia de su estado anterior y siguiente. Ahora, supongamos que se agrega un nuevo estado. ¿Los estados existentes necesitan algún cambio de comportamiento? **-> No, ninguno de los estados existentes necesita un cambio de comportamiento.**

6. ¿Qué patrón se puede utilizar para implementar un cajero automático que dispensa billetes de mayor a menor denominación? **-> Patrón de Cadena de Responsabilidad**

7. Suponga que está construyendo un nuevo software para un dron.
 Considere los siguientes puntos:
* El dron debe ser capaz de cambiar su comportamiento sobre la marcha, basado en su propia evaluación del clima.
* El dron cambiará la forma en que responde a los controles del usuario y a otros sensores en función de si se establece en modo de buen o mal tiempo. 
* Completamente por separado, el dron puede mostrar luces rojas o azules, según las preferencias del usuario. 

- ¿Qué patrón de diseño elegirá para implementar el comportamiento dependiente del clima y que cambia automáticamente? **-> patrón de estado**

8. Utilice el patrón Adapter para convertir el código existente y el patrón Bridge para diseñar código nuevo.
