# Problemas con Gradle en un entorno de acceso a internet con Proxy

Al estar en un entorno de trabajo que utiliza un Proxy para acceder a internet y a pesar de haber configurado el proxy para el entorno del Android Studio, al abrir una aplicación da el siguiente problema de error:

```
Gradle 'Prueba2' project refresh failed: Could not GET 'http://repo1.maven.org/maven2/com/android/tools/build/gradle/'. Received status code 407 from server: Proxy Authentication Required Gradle settings
```

Para resolver este problema, se debe seguir los siguientes pasos:  
  
1- Cerrar el Android Studio.  
2- Ir a la ruta `C:\Users\usuarioWindows\.gradle`.  
3- Crear el archivo `gradle.properties` en esta ruta.  
4- Poner el siguiente contenido en el archivo `gradle.properties`:

```
systemProp.http.proxyHost=servidorProxy
systemProp.http.proxyPort=numeroPuertoProxy
systemProp.http.proxyUser=usuarioRed
systemProp.http.proxyPassword=passwordUsuario
systemProp.http.nonProxyHosts=localhost
systemProp.https.proxyHost=servidorProxy
systemProp.https.proxyPort=numeroPuertoProxy
systemProp.https.proxyUser=usuarioRed
systemProp.https.proxyPassword=passwordUsuario
systemProp.https.nonProxyHosts=localhost
```

5- Abrir el Android Studio.

Con estos pasos realizados ya no se mostrará ese mensaje.



***Fuente***:

- [Bug while creating a new project (proxy setup?)](https://issuetracker.google.com/issues/36971337)
