# Manual de comandos para Ubuntu

El presente manual es una recopilación personal de comandos para algunas tareas y configuraciones que he realizado en el tiempo que he usado Ubuntu. Muchos de estos comandos los he usados desde las versiones 14.XX por lo que pueden ser en casi todas las versiones modernas.

Cabe indicar que Ubuntu Server es la distribución Linux mas usada según w3techs.

## Como saber la versión de Ubuntu

Para conocer la versión de Ubuntu ejecutándose, se debe utilizar la siguiente sentencia:

```bash
lsb_release -a
```

## Atajos de teclado:

| Combinación                   | Descripción                                                                        |
| ----------------------------- | ---------------------------------------------------------------------------------- |
| `ImprPant`                    | Guarda una captura de todo el escritorio en la carpeta “Imágenes”.                 |
| `Shift` + `ImprPant`          | Nos permite seleccionar un trozo de la pantalla y guarda la captura en “Imágenes”. |
| `Alt` + `ImprPant`            | Guarda una captura de la ventana activa en “Imágenes”.                             |
| `Ctrl` + `ImprPant`           | Copia la captura de toda la pantalla en el portapapeles.                           |
| `Shift` + `Ctrl` + `ImprPant` | Copia la captura de un trozo de la pantalla en el portapapeles.                    |
| `Ctrl` + `Alt` + `ImprPant`   | Copia la captura de la ventana activa en el portapapeles.                          |
| `Ctrl` + `ALT` + `T`          | Abre el terminal.                                                                  |
| `Ctrl` + `ALT` + `L`          | Bloque la pantalla.                                                                |
| `Ctrl` + `L`                  | En Nautilus, cambia a la barra de ruta.                                            |
| `Ctrl` + `L`                  | En el Terminal, limpia el terminal, es como ejecutar el comando `clear`.           |

*Fuente: [Cómo hacer capturas de pantalla en Ubuntu Linux &#8211; Laboratorios Docentes de la ETSIT](https://labs.etsit.urjc.es/index.php/tutoriales/como-capturar-pantalla-en-ubuntu-linux/)*

## Actualización del sistema

- Actualizar el sistema:
  
  ```shell
  sudo apt-get update
  sudo apt-get upgrade
  ```

- Limpiar paquetes :
  
  ```shell
  sudo apt-get dist-upgrade
  
  ## o
  sudo apt full-upgrade
  ```

- Eliminar paquetes perdidos:
  
  ```shell
  sudo apt autoremove
  
  ## En los casos que no se puedan actualizar, ejecutar:
  sudo apt install --only-upgrade [lista de paquetes a actualizar]
  ```

- Actualizar los paquetes `snap`:
  
  ```shell
  sudo snap refresh

  ## Actualizar el Snap Store
  sudo pkill snap-store
  sudo snap refresh snap-store
  ```

## Apagar y reiniciar:

- Apagar la máquina:
  
  ```shell
  sudo shutdown -h now
  ```

- Reiniciar la máquina:
  
  ```shell
  sudo shutdown -r now
  ```

## Limpiar cache APT:

- Espacio el caché del APT:
  
  ```shell
  sudo du -sh /var/cache/apt/archives
  ```

- Limpiar el caché del APT:
  
  ```shell
  sudo apt-get clean
  ```

*Fuente:*

[*Cómo liberar espacio en disco en Ubuntu*](https://computerhoy.com/paso-a-paso/software/como-liberar-espacio-disco-ubuntu-49812)

## Otros comandos:

* Buscar un paquete
  
  ```shell
  sudo apt search [NOMBRE_PAQUETE]
  ```

* Reconfigurar un paquete:
  
  ```shell
  sudo dpkg-reconfigure [NOMBRE_PAQUETE]
  ```

* Buscar un paquete con `snap`:
  
  ```shell
  sudo snap search [NOMBRE_PAQUETE]
  ```

## Poner color a la Consola (Ubuntu Server)

* Si el archivo `.bashrc` no existe, copiarlo con la siguiente ruta:
  
  ```shell
  cp /etc/skel/.bashrc ~/.bashrc
  ```

* Abrir el archivo, en este caso con `vim` o cualquier editor para la consola:
  
  ```shell
  vim .bashrc
  ```

* Para editar en `vim` presionar la tecla `i`.

* Descomentar la siguiente línea quitando el caracter `#`:
  
  ```shell
  force_color_prompt=yes
  ```

* Guardar el archivo y salir del editor (`:wq` para `vim`).

* Recargar el archivo de configuración:
  
  ```shell
  source ~/.bashrc
  ```

*Fuente:*

[*Cómo activar los colores de la Terminal*](https://ubunlog.com/como-activar-los-colores-de-la-terminal/?utm_source=feedburner&utm_medium=%24%7Bfeed%2C+email%7D&utm_campaign=Feed%3A+%24%7BUbunlog%7D+%28%24%7BUbunlog%7D%29)

## Instalar .NET Core:

- Instalación del SDK:
  
  ```shell
  sudo apt-get update; \
    sudo apt-get install -y apt-transport-https && \
    sudo apt-get update && \
    sudo apt-get install -y dotnet-sdk-5.0
  ```

- Instalación del entorno de ejecución:
  
  ```shell
  sudo apt-get update; \
    sudo apt-get install -y apt-transport-https && \
    sudo apt-get update && \
    sudo apt-get install -y aspnetcore-runtime-5.0
  ```

*Fuente:*

[*Instalación de .NET en Ubuntu: .NET*](https://docs.microsoft.com/es-es/dotnet/core/install/linux-ubuntu)

## Instalar los wallpapers de las otras distros de Ubuntu:

- Instalar uno por uno:
  
  ```shell
  sudo apt-get install ubuntu-wallpapers-karmic ubuntu-wallpapers-lucid ubuntu-wallpapers-maverick ubuntu-wallpapers-natty ubuntu-wallpapers-oneiric ubuntu-wallpapers-precise ubuntu-wallpapers-quantal ubuntu-wallpapers-raring ubuntu-wallpapers-saucy ubuntu-wallpapers-trusty ubuntu-wallpapers-vivid
  ```

- Instalar todos de golpe:
  
  ```shell
  sudo apt-get install ubuntu-wallpapers*
  ```

*Fuente:*

[Descarga todos los wallpapers comunitarios de Ubuntu » MuyLinux](http://www.muylinux.com/2014/08/12/wallpapers-comunitarios-ubuntu)

## Sentencias a ejecutar luego de instalar Ubuntu:

- Abrir la consola y ejecutar las siguientes sentencias uno por uno:
  
  ```shell
  sudo apt-get update
  sudo apt-get upgrade
  sudo apt autoremove
  sudo apt-get dist-upgrade
  sudo apt-get install exfat-fuse exfat-utils hfsplus hfsutils ntfs-3g
  sudo apt-get install ubuntu-restricted-extras
  sudo apt-get install libavcodec-extra
  sudo apt-get install curl nano wget
  sudo apt-get install libdvdcss2.
  sudo apt-get install ttf-mscorefonts-installer
  sudo apt-get install mtp-tools ipheth-utils ideviceinstaller ifuse
  sudo apt-get install gdebi gdebi-core synaptic
  sudo apt-get install p7zip-full p7zip-rar rar unrar zip unzip
  sudo apt-get install build-essential
  sudo apt install libglvnd-dev pkg-config
  sudo apt-get install printer-driver-all
  sudo apt-get install vlc
  sudo apt install gnome-tweaks
  sudo apt install gnome-shell-extensions
  sudo apt install dconf-editor
  sudo apt install gnome-shell-extension-autohidetopbar
  sudo apt-get install ffmpeg
  sudo apt install net-tools
  sudo apt install snapd
  sudo apt install gedit-plugins
  sudo apt install htop
  sudo apt install tree
  ```

- Se puede instalar varios paquetes en un solo comando:
  
  ```shell
  sudo apt install build-essential libgd-dev openssl libssl-dev unzip apache2 php gcc libdbi-perl libdbd-mysql-perl
  ```

## Crear un acceso directo a una aplicación:

- Crear un archivo `.desktop` en la carpeta `/usr/share/applications` con permisos de administrador, ejemplo:
  
  ```shell
  sudo vim /usr/share/applications/sts.desktop
  ```

- Luego poner el siguiente código:
  
  ```vim
  [Desktop Entry]
  Name =STS
  Comment =Spring Tool Suite
  Exec =/home/emarquez/app/sts-4/SpringToolSuite4
  Icon =/home/emarquez/app/sts-4/icon.xpm
  Terminal =false
  Type =Application
  Categories=Developer;
  Keywords=Java;
  ```

- El siguiente código es un ejemplo que otros datos se pueden ingresar en este archivo:
  
  ```vim
  [Desktop Entry]
  Name=MarkText
  Comment=Next generation markdown editor
  Exec=marktext %F
  Terminal=false
  Type=Application
  Icon=marktext
  Categories=Office;TextEditor;Utility;
  MimeType=text/markdown;
  Keywords=marktext;
  StartupWMClass=marktext
  Actions=NewWindow;
  
  [Desktop Action NewWindow]
  Name=New Window
  Exec=marktext --new-window %F
  Icon=marktext
  ```

*Fuente:*

[Ubuntu crea el icono de acceso directo de androidstudio en el escritorio - programador clic](https://programmerclick.com/article/68481311309/)

[marktext/marktext.desktop at develop · marktext/marktext · GitHub](https://github.com/marktext/marktext/blob/develop/resources/linux/marktext.desktop)

## Instalar Nagios:

```shell
# 1:
wget https://assets.nagios.com/downloads/nagioscore/releases/nagios-4.4.4.tar.gz -O nagioscore.tar.gz
# 2:
tar xvzf nagioscore.tar.gz
# 3:
sudo ./configure --with-https-conf=/etc/apache2/sites-enabled
# 4:
sudo make all
# 5:
sudo make install-groups-users
# 6:
sudo make install
# 7:
sudo make install-init
# 8:
sudo make install-commandmode
# 9:
sudo make install-config
# 10:
sudo make install-webconf
# 11:
sudo systemctl start nagios
```

## Instrucciones para manejo de usuario:

Cabe indicar que el grupo de usuarios `sudo` es donde se adiciona a los administradores del sistema.

```shell
# Cambiar de sesión
sudo su - NOMBRE_USUARIO

#Para saber a que grupo pertenece un usuario
groups NOMBRE_USUARIO

# Adicionar un usuario a un grupo
sudo gpasswd -a NOMBRE_USUARIO NOMBRE_GRUPO

# Sacar un usuario de un grupo
sudo gpasswd -d NOMBRE_USUARIO NOMBRE_GRUPO

# Otra forma de adicionar un usuario a un grupo
sudo usermod -aG NOMRE_GRUPO NOMBRE_USUARIO

# Para ver los permisos de un usuario (estando en la sesión)
sudo -l
```

## Instalar Mono y MonoDevelop

```shell
# Instalar primero Mono
sudo apt install gnupg ca-certificates
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
echo "deb https://download.mono-project.com/repo/ubuntu stable-focal main" | sudo tee /etc/apt/sources.list.d/mono-official-stable.list
sudo apt update
sudo apt install mono-devel

# Instalar MonoDevelop
sudo apt install apt-transport-https dirmngr
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
echo "deb https://download.mono-project.com/repo/ubuntu vs-bionic main" | sudo tee /etc/apt/sources.list.d/mono-official-vs.list
sudo apt update
sudo apt-get install monodevelop
```

> *Nota: En el caso de tener un problema al ejecutar el aplicativo, ejecutar los siguientes comandos:*

```shell
cd /usr/lib
sudo mkdir gnome-terminal
cd gnome-terminal
sudo ln -s /usr/libexec/gnome-terminal-server
```

*Fuente:*

[Download - Stable | Mono](https://www.mono-project.com/download/stable/)

[Download | MonoDevelop](https://www.monodevelop.com/download/)

[c# - Error when trying to run code: Debugger operation failed, Native error= Cannot find the specified file - Stack Overflow](https://stackoverflow.com/questions/59336129/error-when-trying-to-run-code-debugger-operation-failed-native-error-cannot-f)

## Configurar ssh cliente

```shell
# Ejecutar la siguiente sentencia, en donde creará dos archivos en
# la carpeta "/home/usuario/.ssh/" con el nombre "id_rsa" (llave privada)
# y el archivo "id_rsa.pub" (llave publica)
ssh-keygen

# Para comprobar, listar los archivos de la carpeta
ls .ssh

# Copiar las llaves al servidor a donde se quiere ingresar
ssh-copy-id -i ~/.ssh/id_rsa.pub usuario@IP_SERVIDOR

# Ingresar al servidor con ssh cliente:
ssh usuario@IP_SERVIDOR

# Si se necesita pintar el log de ingreso al servidor:
ssh -vvvv usuario@IP_SERVIDOR
```

## Configuración de un servicio

```shell
# Para ver el estado de un servicio
sudo systemctl status SERVICIO

# Si el estado del servicio está en "disabled"
sudo systemctl enable SERVICIO

# Inciar un servicio
sudo systemctl start SERVICIO

# Parar un servicio
sudo systemctl stop SERVICIO

# Reiniciar un servicio
sudo systemctl restart SERVICIO

# Lista todas las unidades de todos los servicios
sudo systemctl list-units -t service --all
```

## Ver los logs del sistema

```shell
# Ir a la carpeta en donde se encuentra los log del sistema
cd /var/log/

# Ver el log de un aplicacion
sudo journalctl -fu apache2

# Ver la cantidad de disco
sudo journalctl --disk-usage

# Ver cuantas veces se ha reiniciado la máquina
sudo journalctl --list-boots

# Ver los log por tipo
sudo journalctl -p crit
```

## Listar los puertos usados

```shell
sudo netstat -tulpn
```

## Instalar NodeJS

```shell
# Download e installar el PPA del repositorio NodeSource
curl -sL https://deb.nodesource.com/setup_18.x | sudo -E bash -

# Instalar Node.js 16.x, incluyendo también se instalará npm.
sudo apt install nodejs

# Verificar la versión de Node.js instalada.
node -v

# Verficar la versión de npm instalada.
npm -v
```

*Fuente: [Installing Node.js and Express on Ubuntu 20.04 - Vultr.com](https://www.vultr.com/docs/installing-node-js-and-express-on-ubuntu-20-04/)*

*[How to Install Node.js and npm on Ubuntu 22.04 | Linuxize](https://linuxize.com/post/how-to-install-node-js-on-ubuntu-22-04/)*

## Instalar Github Desktop:

```shell
##
wget -qO - https://packagecloud.io/shiftkey/desktop/gpgkey | sudo tee /etc/apt/trusted.gpg.d/shiftkey-desktop.asc > /dev/null
##
sudo sh -c 'echo "deb [arch=amd64] https://packagecloud.io/shiftkey/desktop/any/ any main" > /etc/apt/sources.list.d/packagecloud-shiftkey-desktop.list'
##
sudo apt-get update
##
sudo apt install github-desktop
```

*Fuente: [GitHub - shiftkey/desktop: Fork of GitHub Desktop to support various Linux distributions](https://github.com/shiftkey/desktop/)*

## Cambiar la pantalla de inicio de sesión de Ubuntu:

Si se tiene dos monitores en Ubuntu y el inicio de sesión aparece en el monitor secundario, ejecutar la siguiente sentencia:

```shell
sudo cp ~/.config/monitors.xml ~gdm/.config/monitors.xml
```

*Fuente: [La pantalla de inicio de sesión de Ubuntu 20.04 no aparece en la pantalla principal](https://isolution.pro/es/q/au14253028/la-pantalla-de-inicio-de-sesion-de-ubuntu-20-04-no-aparece-en-la-pantalla-principal)*

## Registrar una clave pública:

```shell
## En el ejemplo se registra la clave 61E091672E206FF0
gpg --keyserver keyserver.ubuntu.com --recv 61E091672E206FF0
gpg --export --armor 61E091672E206FF0 | sudo apt-key add -
sudo apt-get update
```

*Fuente: [Cómo solucionar el error de GPG por falta de llave pública | Desde Linux](https://blog.desdelinux.net/como-solucionar-el-error-de-gpg-por-falta-de-llave-publica/)*

## Problemas con Opera al ejecutar un video HTML5:

Cerrar Opera y ejecutar los siguientes comandos:

```shell
snap install chromium-ffmpeg
sudo cp /usr/lib/x86_64-linux-gnu/opera/libffmpeg.so /usr/lib/x86_64-linux-gnu/opera/libffmpeg.so.tmp
ls /snap/chromium-ffmpeg/current/
sudo cp /snap/chromium-ffmpeg/current/chromium-ffmpeg-{version}/chromium-ffmpeg/libffmpeg.so /usr/lib/x86_64-linux-gnu/opera/
```

Fuente: [Opera browser does not play video from Netflix or HBO GO](https://signes.pl/opera-browser-does-not-play-netflix-or-hbogo/)

## Buscar log:

```shell
## Buscar en la carpeta archivos de tipo file con extensión .log
find /var/log/ -name "*.log" -type f

## Busca sin tener en cuenta si .log está en mayúscula o minúscula
find /var/log/ -iname "*.LOG" -type f

## Busca todos los archivos que no sea .log
find /var/log/ ! -iname "*.LOG" -type f

## Busca los archivos que han sido modificados hace 10 minutos
find /etc/ -mtime 10

## Buscar dentro de un archivo la palabra "server"
grep "server" /etc/nginx/sites-available/default

## Lista de un archivo log la primera columna
awk '{print $1}' /var/log/nginx/access.log | sort | uniq -c | sort -nr
```

## Crear un archivo bash ejecutable:

* Crear un archivo `archivo1.sh`
  
  ```bash
  vim archivo.sh
  ```

* Poner el siguiente código en el archivo
  
  ```bash
  #!/bin/bash
  #Variable:
  WELCOME="Hola"
  echo $WELCOME
  
  #Verificar la cantidad dde epacio en el SO
  CWD=$(pwd)
  FECHA=$(date +"%F%T")
  echo $FECHA
  
  df -h | grep /dev > uso_disco_"$FECHA".txt
  df -h | grep /dev/sda2 >> uso_disco_"$FECHA".txt
  
  echo "Se ha generado un archivo en la ubicacion $CWD"
  ```

* Cambiar las propiedades del archivo para ser ejecutado:
  
  ```bash
  chmod u+x archivo1.sh
  ```

* Ejecutar el archivo:
  
  ```bash
  ./archivo1.sh
  ```

## Automatizar una tarea desde el terminal

Para este ejemplo se usará una tarea que realice una copia de seguridad de la base de datos MySQL. Para ello, primero se creará el script:

```bash
#!/bin/bash
# Shell script para obtener una copia desde MySQL

PATH=/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin

set -e

readonly SCRIPT_DIR="$(cd "$(dirname "${BASH_SOURCE[0]}")" && pwd)""
readonly SCRIPT_NAME="$(basename "$0")"

run
make_backup

function assert_is_installed {
    local readonly name="$1"
    if [[!$(command -v ${name}) ]]; then
        log_error "El binario '&name' se requiere pero no esa en nuestro sistema"
        exit 1
    fi
}

function log_error {
    local readonly message "$1"
    log "ERROR" "$message"
}

function log {
    local readonly level="$1"
    local readonly message="$2"
    local readonly timestamp=$(date + "%Y-%m-%d %H:%M:%S") >&2 echo -e "${timestamp} [&{level}] [$SCRIPT_NAME] &{message}"

}

function run {
    assert_is_installed "mysql"
    assert_is_installed "mysqldump"
    assert_is_installed "gzip"
    assert_is_installed "aws"
}

function make_backup {
    local BAK="$(echo $HOME/mysql)"
    local MYSQL="$(which mysql)"
    local MYSQLDUMP="$(which mysqldump)"
    local GZIP="$(wich gzip)"
    local NOW="$(date + "+%d-%m-%Y")"
    local BUCKET=""

    USER=""
    PASS=""
    HOST=""
    DATABASE=""

    [ ! -D "$BAK" ] && mkdir -p "$BAK"
    FILE=$BAK/$DATABASE.$NOW-$(date + "%T").gz

    local SECONDS=0

    $MYSQLDUMP --single-transaction --set-gtid-purged=OFF -u $USER -h $HOST -p$PAS $DATABASE | $GZIP -9 > $FILE

    duration=$SECONDS

    echo "&(($duration /60) minutes)"

    aws s3 cp $BAK "s3://$BUCKET" --recursive
}
```

## Montar un disco

Para montar un disco nuevo, se recomienda usar la herramienta `GParted`, para ello usar los siguientes pasos:

1. Crear tabla de particiones.

2. Crear partición

3. Montar la partición, asignando una ruta, por ejemplo `/mnt/sda1`

Luego, si no se tiene acceso a crear un archivo o carpeta, ejecutar las siguientes sentencias:

```shell
sudo chgrp adm /mnt/sda1
sudo chmod g+w /mnt/sda1
```

## Uso del Firewall

```bash
## Muestra el estado (activo/inactivo) y las reglas del firewall. 
## Con el modificador numbered me muestra las reglas numeradas
sudo ufw status

## Lista las reglas enumeradas
sudo ufw status numbered

## Habilita un puerto
sudo ufw allow PUERTO

## Habilita un puerto con un comentario
sudo ufw allow PUERTO comment COMENTARIO

## Enciende el firewall
sudo ufw enable

## Borra una regla
sudo ufw delete NUMERO_REGLA

## Restringe las direcciones ip que pueden conectarse a cierto puerto.
## Recordar que SSH trabaja con el protocolo TCP
sudo ufw allow from DIRECCION_IP proto PROTOCOLO to any port PUERTO

## Elimina todas las reglas
sudo ufw reset
```

## Instalación y uso de Lynis

```shell
sudo apt update

## Instalar la herramienta
sudo apt update install lynis

## Ejecutar la siguiente sentencia para escanear el sistema
sudo lynis audit system
```

## Poner un servicio web en automático

Se debe crear un usuario, para ello se debe ejecutar la sentencia:

```shell
sudo adduser nodejs
```

Seguidamente, en la ruta `/lib/systemd/system/` crear el archivo `nombreservicio@.service` con el siguiente comando:

```shell
sudo vim /lib/systemd/system/nombreservicio@.service
```

Poner las siguientes líneas:

```bash
[Unit]
Description=Balanceo de carga
Documentation=https://github.com/usuario/linux
After=network.target

[Service]
Environment=PORT=%i
Type=simple
User=nodejs
WorkingDirectory=/home/nodejs/linux
ExecStart=/usr/bin/node /home/nodejs/linux/server.js
Restart-on=failure

[Install]
WantedBy=multi-user.target
```

## Personalizar Ubuntu 22.04

En mi caso, he realizo tres personalizaciones que no está en las herramientas de este sistema, los cuales son, poner transparente el panel superior (top bar), ocultar automáticamente el top bar y cambiar la imagen del login.

### Poner transparente el panel superior:

Para poder poner transparente el panel top bar, instalo la extensión [Transparent Top Bar (Adjustable transparency) - Extensiones de GNOME Shell](https://extensions.gnome.org/extension/3960/transparent-top-bar-adjustable-transparency/), en donde puede fijar el porcentaje de transparencia del panel.

### Ocultar automáticamente el panel superior:

Para poder ocultar el top bar, instalo la extensión [Hide Top Bar - Extensiones de GNOME Shell](https://extensions.gnome.org/extension/545/hide-top-bar/), en donde dejo activo la opción `In the above case, also show panel when fullscreen`.

### Cambiar la imagen del login:

Para ello ejecuto los siguientes comandos:

```shell
wget -qO - https://github.com/PRATAP-KUMAR/ubuntu-gdm-set-background/archive/main.tar.gz | tar zx --strip-components=1 ubuntu-gdm-set-background-main/ubuntu-gdm-set-background

sudo ./ubuntu-gdm-set-background --image /usr/share/Darkening_Clockwork_by_Matt_Katzenberger.jpg
```

Luego de ello, reiniciar el equipo.
