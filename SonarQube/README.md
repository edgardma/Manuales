# Manual de SonarQube

## Instalación

Para instalar SonarQube localmente simplemente se debe descargar la versión 'Community Edition' desde su página web:

```
https://www.sonarqube.org/downloads/
```

Luego de descargar el archivo, por ejemplo `sonarqube-9.7.1.62043.zip`, descomprimirlo en una carpeta, por ejemplo `C:\server\`.

> *Para poder ejecutar SonarQube 9 necesita Java 11, con otra versión anterior o posterior no funciona, según las pruebas realizadas.*



Para ejecutar SonarQube localmente, ejecutar el siguiente script:

```shell
cd C:\server\sonarqube-9.7.1.62043\bin\windows-x86-64

StartSonar.bat
```

Luego de esto, pueden ir a la aplicación desde un navegador:

```
http://localhost:9000/

## Usuario y clave por defecto
Usuario: admin
Clave: admin
```





*Fuente: https://docs.sonarqube.org/latest/setup/get-started-2-minutes/*


