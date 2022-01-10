# Instalación

## En Docker

Para instalar Redis en Docker, se debe ejecutar las siguientes sentencias:

```dockerfile
## Para bajar Redis
sudo docker run --name redis -d redis:6.2.6
## Para la información contenedor
sudo docker inspect redis 
## Para listar los contenedores
sudo docker container ls
```


