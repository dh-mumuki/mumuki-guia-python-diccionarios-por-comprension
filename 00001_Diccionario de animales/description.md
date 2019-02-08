> :memo: **¿Qué devuelve mi_diccionario después de la ejecución de éste código? :bulb: Tip: len() nos indica la cantidad de elementos que posee un determinado objeto (cuando se trata de un _string_, por ejemplo, obtenemos la cantidad de caracteres contenidos en él).**

``` pyhton
animales = ['ballena', 'elefante', 'gallina']

mi_diccionario = {x:len(x) for x in animales}
```