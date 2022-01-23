## Comando principales

| Comando                                            | Descripción                                                                                                                                                                                             |
| -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| *__whoami__*                                       | Comando que devuelve el nombre del usuario de sesión.                                                                                                                                                   |
| *__id__*                                           | Comando que devuelve en detalle de los datos del usuario de sesión.                                                                                                                                     |
| *__ls__*                                           | Listar los archivos y carpetas del directorio actual.                                                                                                                                                   |
| *__ls__ -l*                                        | Lista en detalle los archivos y carpetasde del directorio actual.                                                                                                                                       |
| *__ls__ -lh*                                       | Similar al anterior, solo que en la columna del tamaño esta en Kb o Mb para una mejor lectura (´h´ es de 'human').                                                                                      |
| *__cd__*                                           | Regresa al directorio raiz.                                                                                                                                                                             |
| *__cd__ [dir]*                                     | Se posiciona en el directorio 'dir'.                                                                                                                                                                    |
| *__cd__ -*                                         | Vuelve al directorio donde se ubicó anteriormente.                                                                                                                                                      |
| *__pwd__*                                          | Muestra el directorio absoluto en donde nos encontramos en al consola.                                                                                                                                  |
| *__file__ archivo*                                 | Muestra la información de un archivo.                                                                                                                                                                   |
| *__tree__*                                         | Muestra, en forma de arbol, la estructura de los directorios en consola.                                                                                                                                |
| *__tree__ -L nivel*                                | Muestra, en forma de arbol, de los 'nivel' que se indican.                                                                                                                                              |
| *__mkdir__ dir*                                    | Crea el directorio "dir" en la ruta actual.                                                                                                                                                             |
| *__mkdir__ dir1 dir2 dir3*                         | Crea los directorio "dir1", "dir2" y "dir3" en la ruta actual.                                                                                                                                          |
| *__touch__ file*                                   | Crea un archivo con el nobre "file"                                                                                                                                                                     |
| *__cp__ nombre1 nombre2*                           | Copia un objeto con "nombre1" y lo ubica con el nombre "nombre2".                                                                                                                                       |
| *__mv__ nombre1 nombre2*                           | Mover un objeto con "nombre1" con el nombre "nombre2".                                                                                                                                                  |
| *__rm__ nombre*                                    | Elimina un objeto "nombre".                                                                                                                                                                             |
| *__rm__ nombre1 nombre2*                           | Elimina los objetos "nombre1" y "nombre2".                                                                                                                                                              |
| *__rm__ -r carpeta*                                | Elimina el contenido de la carpeta y la carpeta.                                                                                                                                                        |
| *__head__ file*                                    | Visualiza por el terminal la cabecera de una archivo "file" (las 10 primeras líneas).                                                                                                                   |
| *__head__ file -n lineas*                          | Es igual que el anterior solo que indica la cantidad de líneas a mostrar.                                                                                                                               |
| *__tail__ file*                                    | Visualiza por el terminal las líneas finales de un archivo "file" (las 10 primeras líneas).                                                                                                             |
| *__tail__ file -n lineas*                          | Es igual que el anterior solo que indica la cantidad de líneas a mostrar.                                                                                                                               |
| *__tail__ -f file*                                 | Queda pendiente en consola si hay algún cambio en el archivo`file` y muestra el cambio en tiempo real en la consola.                                                                                    |
| *__tail__ -f file1 file2*                          | Queda pendiente en consola si hay algún cambio en los archivos`file1` y `file2` y los muestra el cambio en tiempo real en la consola.                                                                   |
| *__less__ file*                                    | Visualiza el contenido de un archivo. (q para salir)                                                                                                                                                    |
| *__xdg-open__ fle*                                 | Abre el archivo con la aplicación por defecto.                                                                                                                                                          |
| *__nautilus__*                                     | Abre el aplicativo "Nautilus" que se utiliza para explorar la estructura de archivos de un sistea Linux, en especial en Ubuntu.                                                                         |
| *__type__ comando*                                 | Te muestra en la consola el tipo de comando que se usa en el terminal.                                                                                                                                  |
| *__alias__ nombreAlias="comando"*                  | Crea un alias de un comando para ser ejecutado en el terminal usando el alias.                                                                                                                          |
| *__alias__ ls2="ls -lh"*                           | Crea un aias "ls2" para poder ejecutar el comando "*ls -lh*".                                                                                                                                           |
| *__help__ comando*                                 | Lista la ayuda de un comando.                                                                                                                                                                           |
| *__man__ comando*                                  | Muestra el manual de usuario de un comando.                                                                                                                                                             |
| *__whatis__ comando*                               | Muestra una descripción corta del comando.                                                                                                                                                              |
| *__echo__ mensaje*                                 | Muestra en el terminal el mensaje ingresado.                                                                                                                                                            |
| *__cat__ archivo1 archivo2*                        | Muestra en el terminal el resultado de la unión de dos archivos                                                                                                                                         |
| *__ls__ -lh \| tee resultado.txt \| less*          | Lista en pantalla el resultado del comando __ls__ usando __less__ para visualizarlo, asimismo, exporta el resultado en un archivo "resultado.txt"                                                       |
| *export PATH=$PATH:/usr/games*                     | Con este comando se puede adicionar una ruta al final del PATH.                                                                                                                                         |
| *ls; mkdir directorio; cal*                        | Con el caracter "__;__" se puede ejecutar varios comandos sincronamente (se ejecuta un comando atraz de otro).                                                                                          |
| *ls & date & cal*                                  | Con el caracter "__&__" se puede ejecutar varios comandos asincronamente (se ejecuta los comandos paralelamente, en hilos distintos).                                                                   |
| *mkdir test && cd test*                            | Con el caracter "__&&__" (*AND*) se puede ejecuta el siguiente comando si el anterior se ejecutó correctamente.                                                                                         |
| *__chmod__ 755 file*                               | Cambia los atributos de un archivo para el usuario, grupo y el resto.                                                                                                                                   |
| *__chmod__ u-r file*                               | Quita un atributo, en este caso de lectura, para el usuario local.                                                                                                                                      |
| *__chmod__ u+r file*                               | Pone un atributo, en este caso de lectura, para el usuario local.                                                                                                                                       |
| *__chmod__ u-x,go=w file*                          | En este comando, se quita el atributo de ejecución para el usuario y solo se le dá el atributo de escritura para el grupo y el resto.                                                                   |
| *__chmod__ +x file*                                | En este comando, se otorga el permiso de ejecución para todos (usuario, grupo y otros) al archivo `file`.                                                                                               |
| *__sudo su__ root*                                 | Cambia de usuario en la consola, en este caso, al usuario *root*.                                                                                                                                       |
| *__passwd__* [USUARIO]                             | Comando para poder cambiar la contraseña de un usuario.                                                                                                                                                 |
| *__ln -s__ ruta nombre*                            | Con este comando se crea un link simbólico o acceso directo a una ruta con un nombre abreviado o acceso.                                                                                                |
| *__printenv__*                                     | Lista todas la variables de entorno.                                                                                                                                                                    |
| *__echo $HOME__*                                   | Lista la ruta del *HOME* en la sesión actual.                                                                                                                                                           |
| *__echo $PATH__*                                   | Lista la rutas configuradas de los binarios en donde se ejecutan en el sistema.                                                                                                                         |
| *__which__ criterio*                               | Hace una búsqueda en los archivos según el criterio ingresado.                                                                                                                                          |
| *__find__ ./ -name criterio*                       | Este comando hace una búsqueda desde la ruta (en este caso es desde la raiz) que concuerde con el nombre de archivo según el criterio.                                                                  |
| *__find__ ./ -name \*.txt \| less*                 | Este comando busca en todos los archivos con extensión *.txt* y para mostrarlo usar el comando *less*.                                                                                                  |
| __find__ ./ -type d -name doc\* \| less            | Este comando busca en todos directorios que empiecen con *doc* y para mostrarlo usar el comando *less*.                                                                                                 |
| *__find__ ./ -size 20M*                            | Este comando busca en todos directorios archivos que tenga mas de 20 MB.                                                                                                                                |
| *__grep__ criterio archivo*                        | Busca un texto en un archivo según un criterio.                                                                                                                                                         |
| *__grep__ -i the movies.csv \| less*               | Busca dentro del archivo *movies.csv* la palabra *the* sin tomar en cuenta las mayúsculas o minúsculas (comando *-i*) y para mostrarlo, llevarlo al comando *less*.                                     |
| *__grep__ -ci the movies.csv*                      | Cuenta (comando *c*) las veces que dentro del archivo *movies.csv* la palabra *the* sin tomar en cuenta las mayúsculas o minúsculas (comando *i*).                                                      |
| *__grep__ -vi towers movies.csv > sintowers.txt*   | Busca dentro del archivo *movies.csv* las líneas que no contienen la palabra *towers* sin tomar en cuenta las mayúsculas o minúsculas (comando *i*) y el resultado lo lleva al archivo *sintowers.txt*. |
| *__wc__ archivo*                                   | Muestra en la consola, el número de líneas, el número de palabras y la cantidad de bits de un *archivo*.                                                                                                |
| *__ifconfig__*                                     | Muestra la información de red de la computadora.                                                                                                                                                        |
| *__curl__ www.pagina.com*                          | Muestra el texto de la página web.                                                                                                                                                                      |
| *__curl__ www.google.com > index.html*             | Con este comando, lleva el contenido de la página a un archivo *index.html* en la ruta actual.                                                                                                          |
| *__wget__ www.pagina.com*                          | Graba en disco el contenido de la página web.                                                                                                                                                           |
| *__traceroute__ www.pagina.com*                    | Muestra en pantalla, la ruta de los puntos o IP que se conecta para poder llegar a la página web.                                                                                                       |
| *__netstat__ -i*                                   | Muestra la lista los dispositivos de red de la computadora.                                                                                                                                             |
| *__tar -cvf__ nombrecarpeta.tar nombrecarpeta*     | Con este comando se comprime una carpeta con el formato *.tar*.                                                                                                                                         |
| *__tar -cvzf__ nombrecarpeta.tar.gz nombrecarpeta* | Con este comando se comprime una carpeta con el formato *.gz*.                                                                                                                                          |
| *__tar -xzvf__ nombrecarpeta.tar.gz*               | Con este comando se descomprime el contenido de un archivo con el formato *.gz*.                                                                                                                        |
| *__zip -r__ nombrecarpeta.zip nombrecarpeta*       | Con este comando se comprime una carpeta con el formato *.zip*.                                                                                                                                         |
| *__unzip__ nombrecarpeta.zip*                      | Con este comando se descomprime un archivo con el formato *.zip*.                                                                                                                                       |
| *__ps__*                                           | Lista los todos los procesos que están ejecutandose en la terminal.                                                                                                                                     |
| *__ps__ aux*                                       | Lista los todos los procesos que están ejecutandose en el sistema operativo.                                                                                                                            |
| *__ps__ aux \| grep usuario*                       | Lista los todos los procesos que están ejecutandose por el usuario en el sistema operativo.                                                                                                             |
| *__kill__ pid*                                     | Elimina un proceso que tenga el PID (Process ID) ingresado.                                                                                                                                             |
| *__top__*                                          | Lista los procesos que en este momento están ejecutandose.                                                                                                                                              |
| *__source ~/.bashrc__*                             | Carga la configuración del archivo `.bashrc`.                                                                                                                                                           |
| *__sudo chown__ root:root file*                    | Cambiar el propietario de un archivo, en este caso, al archivo `file` le cambia el propietario a `root` y al grupo `root` .                                                                             |
| *__ip__ a*                                         | Lista las IP del equipo.                                                                                                                                                                                |
| *__sudo smbpasswd__ -a [usuario]*                  | Dar los permisos a un usuario para poder acceder a un recurso compartido para una red Windows usando Samba.                                                                                             |
| *__jobs__*                                         | Lista en consola los trabajos pendientes.                                                                                                                                                               |
| *__./script.sh__ &*                                | Ejecuta el script, pero sin regresa el control a la consola.                                                                                                                                            |
| *__route__ -n*                                     | Muestra en pantalla los datosd de red, incluso la puerta de enlace pretederminada o el dispositivo que está ototrgando internet.                                                                        |
| *__nslookup__ google.com*                          | Muestra la IP de un dominio.                                                                                                                                                                            |

## Comandos para el monitoreo de recursos del sistema

| Comando                                    | Descripción                                                             |
| ------------------------------------------ | ----------------------------------------------------------------------- |
| `cat /proc/cpuinfo \| grep "processor"`    | Comando para visualizar el consumo de CPU del sistema                   |
| `free` y `free -h`                         | Comando que devuelve la información de la memoria del sistema.          |
| `du` y `du -hsc /home/usuario/`            | Comando que devuelve información del disco duro.                        |
| `sudo ps auxf \| sort -nr -k 3 \| head -5` | Comando que devuelve los 5 procesos que consumen mas CPU en el sistema. |
| `sudo ps auxf \| sort -nr -k 4 \| head -5` | Comando que devuelve los 5 procesos que consumen mas RAM en el sistema. |

## Otras sentencias:

Las siguientes sentencias son utiles en el día a día:

```shell
# Lista los usuaris del SO
cat etc/passwd

# Ver las contraseñas de los usuarios (las claves están cifradas)
# Pero antes de tener los permisos necesarios (sudo por ejemplo)
cat /etc/shadow

#Crear un usuario no te pide la clave (debe tener los permisos necesarios)
useradd NOMBRE_USUARIO

#Crea un usuario pero te pide la clave del mismo (también te crea una carpeta en el home)
#debe tener los permisos necesarios
#Este comando no está en todas las distro de Linux
adduser NOMBRE_USUARIO

#Con la siguiente sentencia buscamos si fue creado
cat /etc/passwd | grep NOMBRE_USUARIO

#Eliminar un usuario (debe contar con los permisos necesarios)
userdel NOMBRE_USUARIO
```
