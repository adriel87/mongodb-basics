# Copias de seguridad 🤔

Seguramente en algún momento o de forma recursiva necesitemos realizar una copia de nuestra flamante base de datos o recuperar la información de una copia que previamente hagamos o descarguemos.

## Haciendo un Backup

### base de datos

para hacer una copia de nuestra base de datos hacemos lo siguiente

```Shell
# 1 forma
mongodump --uri="mongodb://mongodb0.example.com:27017" [additional options]

# 2 forma
mongodump --host="mongodb0.example.com:27017"  [additional options]

# 3 forma
mongodump --host="mongodb0.example.com" --port=27017 [additional options]

# en la pagina oficial de mongo veras varias maneras de usar este comando
```

### coleccion
para hacer un backup de nuestras colecciones basta con lanzar el siguiente comando

```Shell

mongoexport --db <nuestra-base-de-datos> -c <la colección> --out <nombre de la copia>.json

```
esto nos crea una archivo en la carpeta desde la que hemos lanzado el comando

## recuperando un Backup

esto vale tanto para bbdd como para colecciones

```Shell

mongorestore <nombreColeccion> <rutaDelBackup>

# ejemplo 

mongorestore mi-super-db .

#  si vamos a usar la ruta donde nos encontramos simplemente usamos el punto `.`


```



