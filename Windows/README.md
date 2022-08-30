# Manual de Windows

## Solución de problemas

### Problemas al no poder ejecutar un script en PowerShell:

Para solucionar este problema, seguir el siguiente manual:

https://appandroideando.blogspot.com/2020/05/solucionar-error-ng-no-se-puede-cargar.html


### Actualizar WSL2 de Ubuntu 20.04 a 22.04

Ejecutar los siguientes comandos desde la línea de comandos de Windows:

```shell
wsl --update

wsl --shutdown
```

Luego, ejecutar desde WSL2 shell el siguiente comando:

```shell
sudo do-release-upgrade
```

Con esto empezará la actualización de Ubuntu 20.04 a 22.04. Cuando finalice correctamente, se puede comprobar ejecutando el siguiente comando desde el shell:

```shell
lsb_release -a
```

El cual debe salir un resultado similar:

```
No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 22.04.1 LTS
Release:        22.04
Codename:       jammy
```

