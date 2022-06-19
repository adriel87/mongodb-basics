# Operadores de consultas expresiva
La verdad es que la traduccion no deja las cosas muy claras, llevemos las cosas a un terreno mas asequible.

Basicamente lo que nos permiten las expressive query operator es usar variables dentro de las consultas.

Permitir usar operadores logicos en las conultas

## sintaxis
`"$expr": <logic operation>`

en lenguaje "humano"

```mongo
db.<coleccion>.find({ 
	"$expr": { 
		"$eq": [ "$end station id", "$start station id"] } }).count()
```

como vemos arriba en el ejemplo estamos comparando dos elementos de un mismo documento y devolviendo 


