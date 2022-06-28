# BSON vs JSON

  

## JSON

  

JavaScript Object Notation

  

en mongo los documentos son básicamente objetos de JS. Se usa el formato JSON para definir la sintaxis de los mismos

  

```json

{

{

"_id": "09020398llskjfl-asdfjk",

"name": "adriel",

"age": 35

}

}

```

como vemos los field se escriben entre comillas dobles

  

### las ventajas del formato JSON son

  

- amigable para el desarrollador

- su lectura es muy sencilla

- familiar, el formato JSON es un standard en la industria 

  

### desventajas

  

- esta basado en texto

- consume mucho espacio

- esta limitado en cuanto a tipos se refiere

  
  

## BSON

  

Binary JSON

  

es la representación en binario de una archivo con formato JSON

  

### ventajas

  

- Es rápido

- menos espacio

- flexible

- tiene un alto performance

- es de propósito general

  
  

| | JSON | BSON |

| --- | --- | --- |

| encoding | UTF-8 string | binary |

| data Support | string, boolean, Number, Array | string, boolean, Number(integer, long, float,...), Array, date, Raw Binary |

| readability | Human and machine | Machine only |

  
  

# import and export data

  

para archivos JSON

  

- mongoimport

- mongoexport

  

```shell

mongoexport --uri="mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/

sample_supplies" --collection=sales --out=sales.json

  

mongoimport --uri="mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/

sample_supplies" --drop sales.json

  

```

  

para archivos BSON

  

- mongorestore

- mongodump

  

```shell

mongodump --uri "mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies"

  

mongorestore --uri "mongodb+srv://<your username>:<your password>@<your cluster>.mongodb.net/sample_supplies" --drop dump

```

  

# usar la consola

  

```shell

  

show databases

#muestra un listado de las bases de datos

  

use <database>

#cambia a la base de datos seleccionada

  

db.<coleccion>.find({"key": "value"})

# devuelve un listado/cursor con el filtro que se aplica en el find

  

db.<coleccion>.find({"key": "value"}).count()

# devuelve la cantidad de registros que cumplen con wl filtro

  

db.<coleccion>.find({"key": "value"}).pretty()

# devuelve la informacion en un formato mas amigable, para versiones de shel inferiores a la 4.5

  

```