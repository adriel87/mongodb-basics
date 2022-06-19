# Leer
para leer documentos de una coleccion solo tenemos que:

1. Usar una BD
```shell
use <database>
```

2. usar una de sus colecciones
```shell
db.<colection>.find({query})
```
donde query es la consulta que vamos a lanzar

### tips
imagina que estas en una coleccion y no tienes ni idea de como luce el modelo de datos que se esta actualmente utilizando en la coleccion

```shell
db.<colection>.findOne()
```
