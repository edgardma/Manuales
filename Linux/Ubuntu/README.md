## Actualización del sistema

- Actualizar el sistema:
  
  ```shell
  sudo apt-get update
  sudo apt-get upgrade
  ```

- Limpiar paquetes :
  
  ```shell
  sudo apt-get dist-upgrade
  ```

- Eliminar paquetes perdidos:
  
  ```shell
  sudo apt autoremove
  ```

- Actualizar los paquetes `snap`:
  
  ```shell
  sudo snap refresh
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
curl -sL https://deb.nodesource.com/setup_16.x | sudo -E bash -

# Instalar Node.js 16.x, incluyendo también se instalará npm.
sudo apt install nodejs

# Verificar la versión de Node.js instalada.
node --version

# Verficar la versión de npm instalada.
npm --version
```

*Fuente: [Installing Node.js and Express on Ubuntu 20.04 - Vultr.com](https://www.vultr.com/docs/installing-node-js-and-express-on-ubuntu-20-04/)*

## 

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

*Fuente: https://github.com/shiftkey/desktop/*

## 

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

*Fuente: https://blog.desdelinux.net/como-solucionar-el-error-de-gpg-por-falta-de-llave-publica/*

## Problemas con Opera al ejecutar un video HTML5:

Cerrar Opera y ejecutar los siguientes comandos:

```shell
snap install chromium-ffmpeg
sudo cp /usr/lib/x86_64-linux-gnu/opera/libffmpeg.so /usr/lib/x86_64-linux-gnu/opera/libffmpeg.so.tmp
ls /snap/chromium-ffmpeg/current/
sudo cp /snap/chromium-ffmpeg/current/chromium-ffmpeg-{version}/chromium-ffmpeg/libffmpeg.so /usr/lib/x86_64-linux-gnu/opera/
```

Fuente: [Opera browser does not play video from Netflix or HBO GO](https://signes.pl/opera-browser-does-not-play-netflix-or-hbogo/)
