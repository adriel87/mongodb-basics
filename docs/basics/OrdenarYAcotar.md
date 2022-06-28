# Ordenar

## sort
muchas veces vamos a querer que nuestras búsquedas estén ordenadas por algún campo


vamos a usar $sort
```Shell

db.<collection>.find(< query o no >).sort({
    <campo>: 1 # orden ascendente
}).limit(1) # limite de documentos

# ahora con un limite de 10 documentos y orden descendente

db.<collection>.find(< query o no >).sort({
    <campo>: -1 
}).limit(10) 

```

ademas podemos ordenar por mas de un campo

```Shell
db.<collection>.find().sort({
    <campo1>:1,
    <campo2>:-1,
    ...
})
```

## limit

ya vimos en el ejemplo anterior el uso de la función limit

básicamente lo que hace esta función es limitar la cantidad de documentos que nos devuelve la consulta
