# Ingeniería Inversa

Para poder hacer una ingeniería inversa de un `APK`, para ello se necesita las siguientes herramientas:

## Herramientas

| Aplicación   | Descripción                                                             | Url                                                                                                                    |
| ------------ | ----------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| *Dex2Jar*    | Herramienta para convertir archivos `.dex` a archivos `.class` de Java. | [Link](https://github.com/pxb1988/dex2jar)                                                                             |
| *JD Project* | Herramienta para convertir archivos `.class` a archivos `.java`         | [Link](http://java-decompiler.github.io/)                                                                              |
| *APKTool*    | Herramienta para convertir los recursos del `APK`                       | [Link 1](https://ibotpeaches.github.io/Apktool/install/)[Link 2](https://bitbucket.org/iBotPeaches/apktool/downloads/) |



## Pasos

| No. | Pasos                                                                                                                      |
| --- | -------------------------------------------------------------------------------------------------------------------------- |
| *1* | Conseguir el `APK`                                                                                                         |
| *2* | Abrir el APK, se puede usar 7z, y extraer el archivo `.dex` y usar la herramienta `Dex2Jar` para generar el archivo `.jar` |
| *3* | Abrir el archivo `.jar` con la herramienta `JD Project` para visualizar el código fuente.                                  |
| *4* | Para extraer los recursos, abrir el el `APK` con la herramienta `APKTool`                                                  |



***Fuente***:

- [INGENIERÍA INVERSA CON APLICACIONES DE ANDROID]([INGENIERÍA INVERSA CON APLICACIONES DE ANDROID](https://www.creadpag.com/2018/05/ingenieria-inversa-con-aplicaciones-de.html))
