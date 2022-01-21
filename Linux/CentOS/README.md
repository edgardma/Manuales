# Instruciones para CentOS

- Lista de paquetes instalados
  
  ```shell
  rpm -qa
  ```

- Información de un paquete:
  
  ```shell
  ## Datos del paquete
  rpm -qi [NOMBRE_PAQUETE]
  
  ## Ubicación de los archivos del paquete
  rpm -qc [NOMBRE_PAQUETE]
  ```

- Actualizar el sistema:
  
  ```shell
  # Ingresar como root
  su
  
  # Actualizar el sistema
  sudo yum update
  ```

- Instalar paquetes adicionales:
  
  ```shell
  ## Instalar las herramientas de red
  sudo yum install net-tools
  ```

- Verificar las direcciones IP del sistema operativo:
  
  ```shell
  ip a
  ```
- Eliminar un paquete:
  
  ```shell
  rpm -e [NOMBRE_PAQUETE]
  ```
- cccc


