# Documentos
la parte donde guardar la información

un documento esta formado por : 

- pares clave/valor
```javascript
{
	{
		"nombre":"adriel"
		  clave   valor
	}
}
```

- otros documentos
```JavaScript

{
	{
		"nombre":"adriel",

		este es otro documento interno, con sus claves y valores
		"gustos":{
			"comida":"calamares",
			"color" : "morado"
		}
	}
}

```

## identificación
en mongoDB cada documento tiene un identificador único

normalmente representado de la siguiente forma

```javascript
{
	{
		"_id":"akjsdhk3hk39":
	}
}
```

## Hablamos de CRUD

### [CREAR](./crearDocumentos.md)
### [ACTUALIZAR](./actualizarDocumentos.md)
### [LEER](./leerDocumentos.md)
### [ELIMINAR](./eliminarDocumentos.md)

## Otras manipulaciones

### [subdocumentos](./subDocuments.md)
### [ordenar](./OrdenarYAcotar.md)
### [upsert](./updatinData.md)
### [indices](./indices.md)



