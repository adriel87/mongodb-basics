# Operadores logicos

Esta parte esta muy relacionada con los [query opertaros](./querys.md)

Los operadores logicos ayudan a crear querys mas especificas estableciendo una serie de condiciones en funcion de si se van cumpliendo o no ciertas consultas.

Veamos un mini ejemplo

```shell
db.routes.find({ "$and": 
	[ 
		{ "$or" :[ { "dst_airport": "KZN" }, { "src_airport": "KZN" } ] }, 
		{ "$or" :[ { "airplane": "CR2" }, { "airplane": "A81" } ] } 
	]
})

```

como vemos los operadores en este caso son

- $and : operador logico que representa "***Y***"
- $or : operador logico que representa "***O***"

Ademas podemos ver claramente como es la sintaxis en las que luego de usar nuestro operador logico tenemos que introdocir dentro de un array las condiciones y estas a su ves tendran su consulta

## tabla de operadores
| operator 	| description       	|
|----------	|-------------------	|
| $and     	| Y                 	|
| $or      	| O                 	|
| $nor     	| O negado          	|
| $not     	| niega la consulta 	|


Repasemos la sintaxis

and,or y not

`{<operador> : [ condicion1, condicion2, ...n condiciones ]}`

not

`{$not : {condicion}}`
