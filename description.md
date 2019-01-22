### Diccionarios por comprensión

Los diccionarios por comprensión tienen una motivación similar al de las listas por comprensión, al igual que las listas el código es mas resumido y claro, la diferencia es que es posible desplegar los datos dentro de un diccionario.

Vimos que la principal diferencia entre una lista y un diccionario es la forma en la que se accede a los distintos elementos: en la lista es un acceso numérico y en el diccionario se accede por llave.

Recordemos como funcionaba el diccionario.

``` python
# se definen los elementos del diccionario como par llave:valor.
mi_dict = {'llave_1' : 123, 'llave_2': 100, 'llave_3' : 311 }

# se accede a un elemento del diccionario a través de su llave.
mi_dict['llave_2']
```
 _Salida:_
**>100**


Al igual que las listas por comprensión, el dicionario requiere trabajar con un **iterable**.

Veamos la sintaxis general para la definición de un diccionario.

``` python
{ expresion_para_llave : expresion_para_valor for elemento in iterable}
```
Como podemos ver en la sintaxis, lo nuevo es que ahora debemos ocuparnos también de las llaves, la dificultad adicional al uso del diccionario con respecto a la lista por comprensión, puede venir dada por la definición de las llaves.

Las partes del diccionario por comprensión son:

  * **expresion_para_llave** : es una expresión que define a la llave, esta expresión debe dar como resultado una llave diferente durante cada iteración, ya que en un diccionario nos encontramos con la restricción de que la llave no debe repetirse
  * `:` : los dos puntos separan la expresión de la llave, con la expresión que da lugar al valor para esa llave.
  * **expresion_para_valor** : es la expresión que define el valor para una llave dada, funciona igual que en la lista por comprensión.
  * `for`: es el llamado al `for`, al igual que en la lista por comprensión.
  * `elemento`: es el nombre con el que definimos a cada elemento del iterable durante cada iteración (igual que en la lista)
  * `in`: indica sobre que vamos a iterar.
  * `iterable`: es el objeto que vamos a recorrer.