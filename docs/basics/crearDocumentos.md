
## Insertar nuevo documento
Para realizar esta practica seria bueno que tuvieras una base de datos corriendo y que accedieras a la shell de mongo.

### un solo documento

Por pasos
1. conéctate a tu base de datos
```Shell
mongo "mongodb+srv://<username>:<password>@<cluster>.mongodb.net/admin"
```
2. usa el esquema para realizar test
```Shell
use sample_training
```
3. mira como son los documentos en caso de que ya tengo algo la colección
```Shell
db.<coleccion>.findOne();
```

4. insertamos el nuevo documento
```Shell
db.inspections.insertOne({
tu documento
})
```

### varios documentos
repetimos los pasos ***1*** y ***2***  

```Shell
db.inspection.insertMany([tusdocumentos separados por coma])
```

## orden de inserción

vamos a realizar una prueba para ver como funciona la el orden de inserción en mongoDB

sitúate en tu colección para realizar test

a continuación inserta los siguientes documentos

```shell
db.inspections.insert([ { "test": 1 }, { "test": 2 }, { "test": 3 } ])
```

como podemos observar esto no nos da fallo y nos insert los 3 documentos

ahora vamos a darle un giro de tuerca

```shell
db.inspections.insert([{ "_id": 1, "test": 1 },{ "_id": 1, "test": 2 }, { "_id": 3, "test": 3 }])
```

hemos visto que aquí obtenemos un error por encontrarse el `_id` duplicado



## cuidado al usar el  shell

Puede que cuando estemos realizando alguna operación dentro de alguna de las colecciones por error escribamos mal el nombre de la colección.
***esto no da error***

y mongoDB simplemente creara una nueva colección