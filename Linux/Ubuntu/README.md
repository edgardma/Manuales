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
  sudo apt-get install exfat-fuse exfat-utils hfsplus hfsutils ntfs-3g
  sudo apt-get install ubuntu-restricted-extras
  sudo apt-get install libavcodec-extra
  sudo apt-get install curl nano wget
  sudo apt-get install libdvdcss2.
  sudo apt-get install ttf-mscorefonts-installer
  sudo apt-get install gdebi gdebi-core synaptic
  sudo apt-get install p7zip-full p7zip-rar rar unrar zip unzip
  sudo apt-get install build-essential
  sudo apt-get install printer-driver-all
  sudo apt-get install vlc
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

    Se puede instalar varios paquetes en un solo comando:

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
```

*Fuente:*

[Ubuntu crea el icono de acceso directo de androidstudio en el escritorio - programador clic](https://programmerclick.com/article/68481311309/)

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

## Otras instrucciones:

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
