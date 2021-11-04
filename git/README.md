# Comandos para el uso de Git

## Comandos básicos:

Comandos para iniciar un repositorio:

```shell
#1- Comando para iniciar un repositorio en una carpeta
git init

#2- Comando para clonar un repositorio
git clone [RUTA_REPOSITORIO] 

#3- Cambiar de branch
git checkout [NOMBRE_BRANCH]

#4- Crear una nueva rama y cambiar a esa rama
git checkout -b [NOMBRE_BRANCH]
```

Comandos para poder subir cambios:

```shell
#1- Diferencia de un archivo entre el proyecto local y el último commit
git diff [DIRECCION DEL ARCHIVO]

#2- Diferencias totales entre el proyecto local y el último commit
git diff

#3- Ver estado del proyecto local
git status

#4- Obtener cambios desde la rama
git pull [NOMBRE_BRANCH] origin

#5- Añadir todos los cambios
git add .

#6- Añadir el cambio de un archivo
git add [DIRECCION_ARCHIVO]

#7- Instanciar los cambios
git commit -m '[MENSAJE]'

#8- Subir los cambios desde el proyecto local hacia la rama
git push origin [NOMBRE_BRANCH]
```

Otros comandos:

```shell
#1- Listar los objetos diferentes (nuevos y/o modificados)
git status -z -u

#2 - Limpiar el cache de los archivos a ignorar, de esta forma el git ya no rastreará los cambios
git rm -r . --cached
```

## Lista de Comandos

Comando para actualizar `git` en Windows:

```shell
git update-git-for-windows
```

Luego de instalar Git ejecutar las siguientes sentencias:

```shell
git config --global user.name "Edgard Marquez"
git config --global user.email edgardma@gmail.com
```

Para revisar si se ejecutó correctamente, ejecutar la sentencia:

```shell
git config --list
```

Versión de Git:
git --version

Ayuda de los comandos:
git help

Para ver la configuración del usuario en el archivo de configuración:
git config --global -e

Para salir del editor escribir el siguiente comando:
:q

Para iniciar un repositorio en una carpeta:
git init

Lista de archivos que están registrados y/o modificados en ese momento en Git (los de color rojo, lo que están pendientes de subir, el de color verde, los listos para subir):
git status

Agregar todos los archivos para que Git esté pendiente de los cambios:
git add .

Agregar todos los archivos modificados para que Git esté pendiente de los cambios:
git add -A

Agregar todos los archivos para que Git esté pendiente de los cambios:
git add --all

Agregar un archivo para que Git esté pendiente de los cambios en el directorio actual:
git add NombreArchivo.extension
git add *.xml

Agregar un archivo para que Git esté pendiente de los cambios en todo los directorios del proyecto:
git add “*.xml”

Agregar el contenido de una carpeta para que Git esté pendiente de los cambios:
git add NombreCarpeta/

Agregar los archivos seleccionados dentro de una carpeta para que Git esté pendiente de los cambios, por ejemplo:
git add NombreCarpeta/*.pf

Para hacer un commit a Git se debe ejecutar el siguiente comando:
git commit -m “Descripción del mensaje”

Para restaura lo realizado hasta el momento del repositorio:
git checkout -- .

Para ver los commit subidos:
git log

Para ver el resumen de todos los commit:
git log --oneline

Para ver el resumen de todos los commit, pero de forma más decorativa:
git log --oneline --decorate --all --graph

Excluir archivos luego de un “git add”:
git reset NombreArchivo.extensión
git reset *.xml

Lista los comits de una manera corta
git log --oneline --decorate --all --graph

Para mostrar menos información o resumida en el status
git status -s

Para mostrar menos información o resumida en el status e indicar la rama:
git status -s -b

Si hay problemas con el caracter CRLF, ejecutar la siguiente sentencia:
git config core.autocrlf true

Crear un alias, para ello se debe crear con el siguiente comando:
git config --global alias.[Nombre_Alias] “comandos”

Ejemplo:
git config --global alias.lg “log --oneline --decorate --all --graph”

Luego se puede ejecutar la sentencia con el alias:

git lg

Otro ejemplo:
git config --global alias.s “status -s -b”

Ejecutar:
git s

Para poder revisar y modificar el archivo de configuración, ejecutar la siguiente sentencia:
git config --global -e

Para poder revisar el archivo de configuración, ejecutar la siguiente sentencia:
git config --global -l

El Stage: Es un lugar donde podemos confirmar los archivos y carpetas que conformarán el commit.

Para ver las diferencias de los archivos en el repositorio:
git diff

Para ver las diferencias en el Stage
git diff --staged

Para quitar un archivo del Stage:
git reset HEAD NOMBRE_ARCHIVO

Ejemplo:
git reset HEAD README.md

Para revertir los cambios:
git checkout -- NOMBRE_ARCHIVO

Ejemplo:
git checkout -- README.md

Adicionar y hacer un commit en una sola línea:
git commit -am “Comentario”

Para modificar el mensaje del comentario de un commit:
git commit --amend -m “Comentario”

Para adicionar unos cambios en el commit actual:
git reset --soft HEAD^

También puede funcionar de la siguiente forma:
git reset --soft ID_COMMIT

Para ir a un commit en particular y deshacer los cambios anteriores:
git reset --mixed ID_COMMIT

Renombrar el nombre del archivo dentro de un commit:
git mv NOMBRE_ARCHIVO NUEVO_NOMBRE_ARCHIVO

Eliminar un archivo de un commit
git rm NOMBRE_ARCHIVO

Agregar y actualizar los cambios en el repositorio:
git add -u

Para ignorar archivos se debe crear un archivo “.gitignore”

Ejemplo del contenido:
*.log
directorio/

Listar las ranas en un repositorio:
git branch

Crear una rama en Git
git branch nombre_rama

Cambiar de rama:
git checkout nombre_rama

Agregar un archivo y un commit
git commit -am “Mensaje”

Listar las diferencias entre dos ramas:
git diff rama master

Hacer un merge de una rama con la principal:
git checkout master
git merge nombre_rama

Borrar una rama:
git branch -d nombre_rama

Para crear y pasar a una rama:
git checkout -b nombre_rama

Crear un TAG en el repositorio:
git tag nombre_tag

Listar los TAG en el repositorio:
git tag

Borrar un TAG:
git tag -d nombre_tag

Crear un TAG con anotaciones:
git tag -a v1.0.0 -m “Versión 1.0.0”

Crear un TAG en un commit anterior:
git tag -a v0.1.0 345d7de -m “Versión alfa”

Mostrar la información del TAG
git show nombre_tag

Para poder llevar los cambios al Stash
git stash
git stash save
git stash save “Etiqueta”

Para saber todos los trabajos en progreso:
git stash list

Para obtener los cambios del “Stash”:
git stash pop

Para restaurar el último registro en el Stash:
git stash apply [ID_STASH]

Para borrar un Stash:
git stash drop

Para borrar todas las entradas que hay en el Stash:
git stash clear

Comandos:

Para obtener la lista de ramas tenemos:
git branch

Pasar a una rama específica:
git checkout [NOMBRE_RAMA]

Para tomar la rama “master” para que se realice los commit:
git rebase master

git lg

git checkout master

git merge rama-misiones-completadas

git lg

Borramos la rama:
git branch -d rama-misiones-completadas

Rebase - Squash
El git rebase, nos puede servir para actualizar el punto de separación de una rama

Juntar los 4 últimos commit:
git rebase -i HEAD~4

Con este comando aparecerá un editor para poder modificar las acciones a realizar en cada commit

Ejemplo 2: Modificar el comentario de un commit
Para este ejemplo, modificamos el comentario del primer commit:

Se ejecutamos la siguiente sentencia:
git rebase -i HEAD~1

Rebase - Edit
Para poder reestablecer un archivo modificado del repositorio:
git checkout -- [NOMBRE_ARCHIVO]

Ejemplo:
git checkout -- misiones.md

Para poder separar los cambios de un commit, se puede ejecutar el siguiente comando:
git rebase -i HEAD~2

Luego aparece en el editor de texto pre-configurado de git la siguiente pantalla:

Se cambia la palabra “pick” por “edit”, tal como se indica en la siguiente pantalla:

Entonces, revertimos los cambios del último commit con el siguiente sentencia:
git reset HEAD^

Individualizar cada cambio realizado, ejemplo:
git add README.md
git commit -m “Actualizaciones al README”

Las siguientes sentencias para adicionar el resto de cambios:
git commit -am “Agregamos mas cambios”

Hasta el momento, el repositorio se encuentra de esta forma:

Cuando ejecutamos “git s” muestra lo siguiente:

Para seguir, ejecutamos el siguiente comando:
git rebase --continue

Y ejecutamos “git s” y nos mostrará el siguiente resultado:

Ejecutamos el “git lg” y ya no estará el commit inicial, solo los commit posteriores:

WIP -> Work in progress

Sección 6: Inicios en GitHub, Git Remote, Push & Pull 

Explicación gráfica:

GitHub: Es una plataforma de desarrollo colaborativo de software para alojar proyectos.

“Origin” es un estandar para referirse al origen

Para saber las fuentes remotas que tenemos en el repositorio:
git remote -v


