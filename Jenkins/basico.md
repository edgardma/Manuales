## Pasos para instalación de Jenkins

### Pre-requisitos:

- Se debe instalar JDK8 o jdk11 ya sea de Oracle u OpenJDK

- Tener liberado el puerto 8080 (para la instalación por defecto)

### Instalación en Ubuntu:

Se debe ejecutar las siguientes sentencias:

```
sudo apt-get update
sudo apt-get upgrade
wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo add-apt-repository "deb https://pkg.jenkins.io/debian binary/"
sudo apt-get update
sudo apt-get install jenkins
```

Validar la ejecución de Jenkins en un navegador a la siguiente ruta `localhost:8080`.

En el caso que Jenkins aún no está activo, ejecutar las siguiente sentencia en la consola: 

```
sudo service jenkins status
sudo service jenkins start
sudo service jenkins status
```

### Instalar en Docker

Para instalar Jenkins en Docker, se puede usar la siguiente sentencia (tanto para Windows como en Ubuntu) en donde se puede especificar el puerto en donde se ejecutará el servicio, en este caso, el puerto 9080:

```
docker run -d -p 50000:50000 -p 9080:9080 -e JENKINS_OPTS="--httpPort=9080" --name jenkinsdocker jenkins/jenkins:lts
```

La primera vez, Docker bajará los archivos necesarios para crear el contenedor, por lo cual, puede tomar su tiempo para concluir. En el caso que ya tenga esos archivos, Docker lo creará mucho mas rápido.

Desde la consola, para acceder al contenido del contenedor, se debe ejecutar la siguiente sentencia:

```
docker exec -i -t [id_contendor] /bin/bash
```

Luego, para poder leer el contenido del archivo creado luego de la instalación, se puede ejecutar la siguiente sentencia desde la consola:

```
head /var/jenkins_home/secrets/initialAdminPassword
```

Finalmente, validar la ejecución de Jenkins en un navegador local a la siguiente ruta `localhost:9080`.
