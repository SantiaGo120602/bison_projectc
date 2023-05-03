##Lenguajes de programación
##Bizon
##Santiago Javier Vivas
##Samuel Medina Mora
##Julieth Manzano
##Alejandro Toloza

>Requisitos:
* Make
* gcc
* bison
* flex

>Ejecución:

## **1)**
¿Puedes cambiar la sintaxis para hacerla más intuitiva? Si añades símbolos de cierre a las sentencias condicionales if/then/else/ fi y a los bucles while/do/done, ¿puedes flexibilizar la sintaxis de las listas de sentencias?

> Se agregó el token "tt" para terminar los condicionales y bucles y se eliminó el ";" de la lista de declaraciones para hacer la sintaxis más intuitiva y flexible.


## **2)**
En el último ejemplo, las funciones de usuario evalúan todos los argumentos reales, los colocan en una matriz temporal y luego los asignan a los argumentos ficticios.
¿Por qué no hacerlo de uno en uno y asignar los argumentos ficticios a medida que se evalúan los reales?


> Al hacer una implementación con una matriz temporal, se permite una evaluación más eficiente de los argumentos, ya que se pueden evaluar todos juntos y luego asignarlos en una sola operación en lugar de hacer múltiples asignaciones. Además, si se produce un error en uno de los argumentos reales, los valores de los argumentos ficticios no se modificarán y se mantendrán los valores originales. Esto puede ser importante si los valores de los argumentos ficticios se utilizan en otros cálculos más adelante en la función.

Por otro lado, si se realiza la implementación uno a uno, como se ha hecho en este caso, puede que en la mayoría de los casos funcione correctamente, sin embargo, los valores ficticios antiguos (que han sido reemplazados por los argumentos reales actuales) se pierden y no es posible reasignarlos, dejándolos como estaban originalmente. Si esto genera un error, no hay manera de evitarlo.

En resumen, la razón principal de utilizar una matriz temporal es para lograr una evaluación eficiente y mantener los valores originales de los argumentos ficticios en caso de error, lo que puede ser importante si se usan en cálculos posteriores.
