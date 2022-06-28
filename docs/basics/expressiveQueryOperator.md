# Operadores de consultas expresiva
La verdad es que la traducción no deja las cosas muy claras, llevemos las cosas a un terreno mas asequible.

Básicamente lo que nos permiten las expressive query operator es usar variables dentro de las consultas.

Permitir usar operadores lógicos en las consultas

## sintaxis
`"$expr": <logic operation>`

en lenguaje "humano"

```mongo
db.<coleccion>.find({ 
	"$expr": { 
		"$eq": [ "$end station id", "$start station id"] } }).count()
```

como vemos arriba en el ejemplo estamos comparando dos elementos de un mismo documento y devolviendo 


