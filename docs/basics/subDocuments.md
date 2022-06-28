# subDocuments

Un subdocument no es mas que meter/embeber un documento dentro de otro. Esto es util por muchos motivos como el modelado de una base de datos.

Pero como buscamos la informacion dentro de esos documentos.

## dot notation

`dot notation` o notación por punto es muy similar a cuando tratamos de acceder a las propiedades de un objeto por ejemplo en JS

```javascript
const persona = {
    name:'paco',
    age: 25
}

// para acceder a name usamos dot notation

persona.name

```

pues en mongoDB se trabaja de forma similar por no decir igual


```shell
db.<collection>.find({
    "<tu documento>.<elcampo>": <expresion o valor a validar/comparar>
})
```

también es posible que lo que tengamos sea una array de objeto, para lo cual solo tenemos que indicarle la posición, sin embargo no es como en JS que usamos `[0]` para determinar la primera posición.

seguimos usando la notación del punto veamos un ejemplo de sintaxis

```shell
db.<collection>.find({
    "<tu array documento>.<posicion>.<elcampo>": <expresion o valor a validar/comparar>
})
```

donde la `posicion` es un valor numérico

