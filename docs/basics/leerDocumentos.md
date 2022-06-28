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

## tips
imagina que estas en una coleccion y no tienes ni idea de como luce el modelo de datos que se esta actualmente utilizando en la coleccion

```shell
db.<colection>.findOne()
```

## Seleccionar que campos mostrar

En mas de una ocasion tenemos demasiada informacion en un documento y es necesario filtrar la informacion de salida de la busqueda, por ejemplo solo obtener el nombre y la edad de una coleccion de personas

Justo depues de establecer como vamos a lanzar la consulta tenemos que indicar que es lo que se va a ver hay basicamente 2 formas para filtrar:

### incluyendo
Aqui indicamos los campos que queremos ver

```shell
db.<colection>.find({<query>},{<campo>:1})
```

como vemos indicamos con un uno que se va a mostrar

### excluyendo

lo hacemos igual que en el punto anterior pero a la inversa, la busqueda mostrara todo salvo lo que pongamos en el filtro

```shell
db.<collection>.find({<query>},{<campo>:0})
```

### excepciones

Desde [atlas](https://university.mongodb.com/) recomiendan trabajar o bien incluyendo o excluyendo.

Si bien hay una consulta que es bastante tupica y es quitar el id autogenerado por mongo cuando se crea un nuevo documento.

```shell
db.<colection>.find({query},{<campo>:1, "_id":0})
```

