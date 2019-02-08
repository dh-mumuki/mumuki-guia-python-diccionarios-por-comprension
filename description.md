Los **diccionarios por comprensión** tienen una motivación similar a la de las listas por comprensión. Como vimos en la [lección anterior](https://mumuki.io/data-science.digitalhouse/lessons/415-nivelacion-python-listas-por-comprension), el código es más resumido, claro y eficiente. La diferencia es que es ahora volcaremos los datos dentro de un diccionario en lugar de una lista.

Vimos que una diferencia importante entre las listas y los diccionarios es la forma en la que se accede a los elementos que contienen. Como las listas son colecciones ordenadas, podemos acceder a sus elementos a partir del índice que marca su posición en la lista. Los diccionarios, por el contrario, no se encuentran ordenados, sino que se estructuran a partir de pares **clave:valor**; para acceder al valor de un elemento en particular, basta con hacer un llamado a la clave única que lo identifica.

Recordemos cómo trabajamos con un diccionario:

``` python
# Se definen los elementos del diccionario como pares clave:valor
mi_dict = {'clave_1': 123, 'clave_2': 100, 'clave_3': 311}

# Se accede a un valor particular a través de su clave
mi_dict['clave_2']

ム
> 100
```

Al igual que las listas por comprensión, un dicionario por comprensión requiere trabajar con un **iterable**.

Veamos la sintaxis general para la definición de un diccionario por comprensión:

``` python
{**expresión_para_clave** : **expresión_para_valor** for **elemento** in **iterable** [if **condición**]}
```
Como podemos ver en la sintaxis, lo nuevo es que ahora debemos ocuparnos también de las claves.

Vamos a explicar de forma ordenada cómo funciona la sintaxis de los diccionarios por comprensión:

  * **expresión_para_clave** : es una expresión que define a la clave; debe dar como resultado una clave diferente durante cada iteración, ya que en un diccionario nos encontramos con la restricción de que las claves no deben repetirse.
  * `:` : los dos puntos separan la expresión de la clave de la expresión que da lugar al valor asociado.
  * **expresión_para_valor** : es la expresión que define el valor para una clave dada; funciona igual que en las listas por comprensión.
  * `for`: da inicio a un bucle, al igual que en las listas por comprensión.
  * **elemento**: es el nombre de la variable a la que asignamos cada elemento del iterable durante cada iteración (igual que en las listas por comprensión).
  * `in`: indica sobre qué vamos a iterar.
  * **iterable**: es el objeto que vamos a recorrer.
  * `if`: señala la expresión condicional que vamos a evaluar sobre los elementos del iterable que recorremos (al igual que en las listas por comprensión, su inclusión resulta opcional).
  * **condición**: es el condicional que va a ser evaluado.
