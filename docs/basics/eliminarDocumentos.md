# Eliminar
para eliminar documentos podemos o bien eliminar de uno en uno o eliminar varios a la vez

## solo uno
```shell
db.<coleccion>.deleteOne({query})
```
## Varios a la vez
```shell
db.<colection>.deleteMany({query})
```

## Toda la colección
```shell
db.<colection>.drop()
```

este ultimo comando borrara toda la colección, asi que ***CUIDADO***

