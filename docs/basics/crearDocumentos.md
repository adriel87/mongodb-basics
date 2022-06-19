
## Insertar nuevo documento
Para realizar esta practica seria bueno que tuvieras una base de datos corriendo y que accedieras a la shell de mongo.

### un solo documento

Por pasos
1. conectate a tu base de datos
```shell
mongo "mongodb+srv://<username>:<password>@<cluster>.mongodb.net/admin"
```
2. usa el esquema para realizar test
```shell
use sample_training
```
3. mira como son los documtos en caso de que ya tengo algo la coleccion
```shell
db.<coleccion>.findOne();
```

4. insertamos el nuevo documento
```shell
db.inspections.insertOne({
tu documento
})
```

### varios documentos
reperimos los pasos ***1*** y ***2***  

```shell
db.inspection.insertMany([tusdocumentos separados por coma])
```

## orden de insercion

vamos a realizar una prueba para ver como funciona la el orden de insercion en mongoDB

situate en tu coleccion para realizar test

a continuacion inserta los siguientes documentos

```shell
db.inspections.insert([ { "test": 1 }, { "test": 2 }, { "test": 3 } ])
```

como podemos observar esto no nos da fallo y nos insert los 3 documentos

ahora vamos a darle un giro de tuerca

```shell
db.inspections.insert([{ "_id": 1, "test": 1 },{ "_id": 1, "test": 2 }, { "_id": 3, "test": 3 }])
```

hemos visto que aqui obtenemos un error por encontrarse el `_id` duplicado



## cuidado al usar el  shell

Puede que cuando estemos realizando alguna operacion dentro de alguna de las colecciones por error escribamos mal el nombre de la coleccion.
***esto no da error***

y mongoDB simplemente creara una nueva coleccion