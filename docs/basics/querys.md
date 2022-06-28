# Consultas

Para realizar consultas por ejemplo con el comando find vemos que necesitamos establecer una condición. 

Esto no es mas que indicar los resultados que hacen match con la consulta por ejemplo

```shell
db.<collection>.find({"name":"pepito"})
```

si bien la consulta de arriba es valida es demasiado especifica para muchos casos de uso en los que necesitamos evaluar los valores de los campos.

## Query Operators
estos operadores son los que nos dan el poder de realizar evaluaciones a los valores de los campos que vayamos a evaluar.

si conoces algo de SQL seria algo como todo lo que pones dentro del bloque WHERE

para usar un query operator vamos a usar el símbolo de dólar ***`$`***

la sintaxis correcta para usarlo es:
`{<field>:{<opertator>:<value>}}`

imaginemos una colección personas y queremos buscar las que tengan una edad mayor de 30:

```shell
db.personas.find({"edad":{"$gt": 30}})
```

Si no indicamos el tipo de operador por defecto tenemos el $eq que es el operador de `igual que`

## Tabla de operadores

| operator 	| description       	|
|----------	|-------------------	|
| $eq      	| igual que         	|
| $ne      	| distinto que      	|
| $gt      	| mayor que         	|
| $gte     	| mayor o igual que 	|
| $lt      	| menor que         	|
| $lte     	| menor o igual que 	|



### [Logic Operator](./logicOperators.md)
### [Expressive Query Operator](./expressiveQueryOperator.md)

