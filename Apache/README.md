## Cambiar el puerto de Apache

```shell
# Modificar el archivo ports.conf, cambiar el puerto 80 a 8080
sudo nano /etc/apache2/ports.conf

# Modifcar el archivo 000-default.conf, cambiar el puerto 80 a 8080
sudo nano /etc/apache2/sites-available/000-default.conf

# Reiniciar el servicio
sudo systemctl restart apache2
```


