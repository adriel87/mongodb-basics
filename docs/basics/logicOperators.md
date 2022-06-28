# Operadores lógicos

Esta parte esta muy relacionada con los [query opertaros](./querys.md)

Los operadores lógicos ayudan a crear querys mas especificas estableciendo una serie de condiciones en función de si se van cumpliendo o no ciertas consultas.

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

- $and : operador lógico que representa "***Y***"
- $or : operador lógico que representa "***O***"

Ademas podemos ver claramente como es la sintaxis en las que luego de usar nuestro operador lógico tenemos que introducir dentro de un array las condiciones y estas a su ves tendrán su consulta

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
