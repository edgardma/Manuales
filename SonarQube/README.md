# Manual de SonarQube

## Instalación

Para instalar SonarQube localmente se debe descargar la versión 'Community Edition' desde su página web:

```
https://www.sonarqube.org/downloads/
```

En esta página escoger la columna que dice 'Community Build' y presiona el botón 'Download for free', saldrá una pantalla que dice 'Sign up and download' y escoger la opción ´Download only´.

Se descargará un archivo con extensión ".zip", por ejemplo `sonarqube-9.7.1.62043.zip` para la versión 9, o `sonarqube-24.12.0.100206.zip` para la versión 10, que es el mas actual.

Luego, copiar el archivo a una ruta, por ejemplo `C:\server\`.

Descomprimirlo en la ruta copiada.

Previamente, se debe instalar el JDK de Java.

> *Para poder ejecutar SonarQube 9 necesita Java 11, con otra versión anterior o posterior no funciona, según las pruebas realizadas.*
> 
> *Para SonarQube 10 se necesita JDK 17, según las pruebas realizadas.*

Para ejecutar SonarQube localmente, ejecutar el siguiente script:

```shell
# Para la versión 9
cd C:\server\sonarqube-9.7.1.62043\bin\windows-x86-64

# Para la versión 10
cd C:\server\sonarqube-10.7.0.96327\bin\windows-x86-64

StartSonar.bat
```

Luego de esto, pueden ir a la aplicación desde un navegador:

```
## Ruta local
http://localhost:9000/

## Usuario y clave por defecto
Usuario: admin
Clave: admin
```

Al ingresar, le pedirá cambiar la clave del usuario `admin`, ingresa la clave anterior (`admin`) y digita la nueva clave dos veces.



*Fuente: https://docs.sonarqube.org/latest/setup/get-started-2-minutes/*
