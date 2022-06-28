# indices

los indices sirven para hacer que nuestras consultas sean mas eficientes y rápidas

es una de las mejores formas de mejorar el performance de nuestra maquina

## crear un indice

```Shell
db.<collection>.createIndex({<campo>:1})
```
el valor de 1 o -1 indica si el indice es ascendente o descendente