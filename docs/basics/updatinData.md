# actualizando 

es normal tener que actualizar datos den un documento o varios de una colección.

## sintaxis

```Shell

db.<collection>.updateOne({
    <query>
},
{
    <update>
})

```

primero tenemos que indicar que documentos queremos actualizar y luego actualizamos los campos que necesitemos

un ejemplo mas real

```Shell
db.casas.updateOne({
    "owner":"paco",
},
{
    "value": {$inc: 100000}
}
)
```

en este update buscamos dentro de la colección de casas la primera casa que por propietario tenga a paco y luego le indicamos que el valor de la casa se incremente en 100000

## upsert

funciona como una mezcla de insert y update, donde vamos a crear una nuevo registro/documento a partir del que vamos a modificar.

es un parámetro opcional al final del método de update


```Shell

db.<collection>.updateOne({
    <query>
},
{
    <update>
},
{
    "upsert":true
})

```