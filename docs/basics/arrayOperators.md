# Array Operators

Los operadores que nos permiten trabajar con los arrays dentro de mongo db

## operadores

### $push

- permite a;adir un elemento a un array
- convierte un campo a un campo de array si previamente era de un tipo diferente


### $all

- permite realizar busquedas 
- la sintaxis es similar a los operadores logicos
  - `{<field> : {"$all":[<parameters...>]}`
  - ejemplo
```mongodb
db.listingsAndReviews.find({
    "amenities":{
    "$size":20,
    "$all":["Wifi","Shampoo"]
  }
}).size()  
```
 como vemos en el ejemplo anterior buscamos con all y hacemos match si se encuentran todos los parametros que pasemos dentro del array

 ### $size

 - con size indicamos el tama;o minimo de el array en el que vamos a buscar

 - en el ejemplo de arriba lo usamos indicamos que el array tiene que ser de 20

