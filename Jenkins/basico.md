## Pasos para instalación de Jenkins en Ubuntu

### Pre-requisitos:

- Se debe instalar JDK8 o jdk11 ya sea de Oracle o Open

- Tener liberado el puerto 8080

### Instrucciones:

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
