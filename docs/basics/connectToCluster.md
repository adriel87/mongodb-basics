# Conexión a base de datos

para realizar una conexión a través de una consola

1. tenemos que tener instalado el [shell de mongo] (https://www.mongodb.com/try/download/shell)
2. conectarnos con una una base de datos o cluster, para ello necesitamos la cadena de conexión
  - mongodb+srv://`<usuario>:<contraseña>@<direccion>`

3. lo siguiente es ejecutar el comando 

```Shell
mongosh mongodb+srv://m001-student:1234@sandbox.8g75v.mongodb.net/test
```

si todo va bien estaremos en la shell de nuestro cluster de mongo

### puede seguir por los [documentos](./documentos.md)
