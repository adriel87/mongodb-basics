# Copias de seguridad 🤔

Seguramente en algun momento o de forma recursiva necesitemos realizar una copia de nuestra flamante base de datos o recuperar la informacion de una copia que previamente hagamos o descarguemos.

## Haciendo un Backup

## recuperando un Backup

```shell

mongorestore <nombreColeccion> <rutaDelBackup>

# ejemplo 

mongorestore mi-super-db .

#  si vamos a usar la ruta donde nos encontramos simplemente usamos el punto `.`


```
