# Aggregation Framework

## que es
es otra forma sencilla de realizar las consultas

primero veamos un ejemplo de una consulta con MQL, el lenguaje para hacer querys que hemos usado hasta ahora

```Shell
db.casitas.find({
    "extras":"wifi",
},
{
    "valor":1, "_id":0
})
```

ahora veamos como se ve con el framework

```Shell
db.casitas.aggregation([
    $match: {"extras":"wifi"},
    $project: {"valor":1, "_id":0}
])
```

si nos fijamos toda la sintaxis nueva esta dentro de `[]` indicando que es un array. Un array con acciones que vamos a llevar a cabo.

En este sentido el orden de cada accion gana importancia


## para que lo usamos

no parece muy util para una consulta simple. 

Vemos us potencial cuando queremos hacer varias acciones cuando realizamos una búsqueda sobre una colección, por ejemplo agrupar por un determinado campo.

nos da la habilidad de sobrepasar la funcionalidad de una simple busqueda puediendo realizar calculos, reformar y reorganizar los datos


### sintax

#### match

lo que queremos buscar

#### group

como lo queremos agrupar

#### project 

lo que queremos mostrar