# Actualizar

para realizar una actualizacion sobre una coleccion hay principalmente 2 formas de hacerlo

- updateOne : Actualiza solo un documento de la coleccion
- updateMany : Actualiza varios documentos de la coleccion

## Solo uno
para actualizar un solo documento debemos tener en cuenta que la consulta que lanzemos debe ser lo mas precisa posible.

En caso de que mas de un documento cumpla con la condicion establecida en la consulta es posible que solo se actualice uno de nuestros documentos. Que puede o no ser el deseado

al lio

```shell
db.zips.updateOne({"zip":"12534"}, {"$set":{"pop": 2345}})
					consulta               update
```

## varios a la vez

para actualizar varios documentos a la vez tenemos que primero lanzar una consulta a traves de algun campo y su clave, pueden establecer mas de un campo en esa consulta.

Luego indicamos que es y como queremos cambiarlo por ejemplo a;adir cierta cantidad a un campo

```shell
db.zips.updateMany({ "city": "HUDSON" }, { "$inc": { "pop": 10 } })
						filtro                     update
```

lo que hacemos en la parte superior es:
1. indicar cual es nuestro filtro
2. determinar la accion para cada uno de los elementos que cumplan con el filtro


## operadores

Habras visto en los ejemplos que despues de la consulta tenemos un campo que nos indica que hacer en el update se ve asi

`ejemplo`
***$inc*** 

algunos ejemplos

- $inc: realiza un incremento
- $set: establece un nuevo valor
- $push: a;ade un elemento a un array

