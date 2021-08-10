## Tipos de Archivos

| Atributo | Descripción                    |
| -------- | ------------------------------ |
| *-*      | Archivo normal.                |
| *d*      | Un directorio.                 |
| l        | Un link simbólico.             |
| *b*      | Un archivo de bloque especial. |

## Tipos de Modo

| Dueño       | Grupo       | World       |
| ----------- | ----------- | ----------- |
| *rwx*       | r-x         | r-x         |
| 1 \| 1 \| 1 | 1 \| 0 \| 1 | 1 \| 0 \| 1 |

## Modo Octal

| Octal | Binario | Permisos |
| ----- | ------- | -------- |
| 0     | 000     | ---      |
| 1     | 001     | --x      |
| 2     | 010     | -w-      |
| 3     | 011     | -wx      |
| 4     | 100     | r--      |
| 5     | 101     | r-x      |
| 6     | 110     | rw-      |
| 7     | 111     | rwx      |
