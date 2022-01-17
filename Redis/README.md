# Instalación

## En Docker

Para instalar Redis en Docker, se debe ejecutar las siguientes sentencias:

```shell
## Para bajar Redis
sudo docker run --name redis -d redis:6.2.6
## Para la información contenedor
sudo docker inspect redis 
## Para listar los contenedores
sudo docker container ls
```

Tambien se puede crear el contenedor y ejecutarlo en un puerto local con la siguiente sentencia:

```shell
sudo docker run -p 6379:6379 -d redis:6.2.6 redis-server
```

Y para poder ver el log del contenedor, ejecutar la siguiente sentencia:

```shell
sudo docker logs CONTENEDOR_ID
```
