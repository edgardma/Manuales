## Prueba de un diagrama en Markdown usando Mermaid

Le siguiente código es una prueba para el uso de un diagrama en un archivo Markdown:

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

El siguiente código es una prueba un poco mas complicada de un diagrama en un Markdown:

```mermaid
flowchart TD;
    A[Desplegar en produccion]-->B[¿Es viernes?];
    B--Si-->C[No desplegar];
    B--No-->D[Ejecutar deploy.bat para desplegar];
    C---->E[Buen fin de semana];
    D---->E[Buen fin de semana];
```


