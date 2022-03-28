# Manual de ELK Stack (Elasticsearch, Logstash, Kibana)

Este es un manual de uso de ELK Stack, desde su instalación y configuración y algunas pruebas realizar.

## Instalación local Elasticsearch

Para instalarlo, se debe seguir los siguientes pasos:

- Bajar el software según el sistema operativo de la siguiente ruta [Get Started with Elasticsearch, Kibana, and the Elastic Stack | Elastic](https://www.elastic.co/es/start)
* Descomprimir el archivo en una ruta local.

* Ir a la carpeta `[Ruta instalación]\elasticsearch-8.1.1\config` y abrir el archivo `elasticsearch.yml`.

* Modificar y descomentar las siguientes atributos: 
  
  ```yaml
  #
  cluster.name: demo-elk
  #
  node.name: elk-1
  #
  network.host: 0.0.0.0
  # (Siguiente línea es nueva, agragarla al final del archivo)
  # Configuramos discovery.type como nodo único.
  discovery.type: single-node
  ```

* En la consola, ir a la siguiente ruta: `[Ruta instalación]\elasticsearch-8.1.1\bin`

* Ejecutar el comando `elasticsearch.bat` (Windows) o `.\elasticsearch` (Linux)

* En la consola aparecerá el token y la clave del usuario administrador (`elastic`), copiarlo en un editor para su posterior uso.

## 

## Instalación local Kibana

Para instalarlo, se debe seguir los siguientes pasos:

- Bajar el software según el sistema operativo de la siguiente ruta [Get Started with Elasticsearch, Kibana, and the Elastic Stack | Elastic](https://www.elastic.co/es/start)

- Descomprimir el archivo en una ruta local.

- En la consola, ir a la siguiente ruta: `[Ruta instalación]\kibana-8.1.1\bin`

- Ejecutar el comando `kibana.bat` (Windows) 

- En la consola aparecerá la ruta en donde se está ejecutando Kibana, por ejemplo: `http://localhost:5601/?code=624817` 

- El aplicativo pedirá ingresar el token que salió en la consola de Elasticsearch, copiarlo y dar siguiente.

- El aplicativo pedirá un usuario y clave para el ingreso, digitar el usuario (elastic) y la clave que salió en la consola de Elasticsearch, y presionar `Aceptar`.



## Instalación local Log

Para instalarlo, se debe seguir los siguientes pasos:

- Bajar el software según el sistema operativo de la siguiente ruta [Download Logstash Free | Get Started Now | Elastic](https://www.elastic.co/es/downloads/logstash)

- Descomprimir el archivo en una ruta local.

- En la consola, ir a la siguiente ruta: `[Ruta instalación]\logstash-8.1.1\bin`

- 
