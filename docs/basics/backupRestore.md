# Copias de seguridad 🤔

Seguramente en algun momento o de forma recursiva necesitemos realizar una copia de nuestra flamante base de datos o recuperar la informacion de una copia que previamente hagamos o descarguemos.

## Haciendo un Backup

para hacer un backup de nuestra base de datos basta con lanzar el siguiente comando

```shell

mongoexport --db <nuestra-base-de-datos> -c <la coleccion> --out <nombre de la copia>.json

```
esto nos crea una archivo en la carpeta desde la que hemos lanzado el comando

## recuperando un Backup

```shell

mongorestore <nombreColeccion> <rutaDelBackup>

# ejemplo 

mongorestore mi-super-db .

#  si vamos a usar la ruta donde nos encontramos simplemente usamos el punto `.`


```



