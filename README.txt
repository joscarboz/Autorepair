---------------GUÍA DE EJECUCIÓN-------------------------

1.Ejecutar los imports

2.Ejecutar las definiciones de los métodos y los create de la toolbox

3.Cuando te pregunte por el tamaño del circuito, introducirlo, a pesar de que el circuito vaya a ser
generado más adelante. Es muy importante repetir este paso si pensamos realizar algún experimento con un circuito de otro tamaño.

4.Ejecutar el resto de métodos de definición, siempre en orden.

5.A continuación tendremos que introducir en el código el tamaño del circuito. Para los experimentos realizados bastaría con
ponerlo en 4*4, ya que al haber fijado valores pseudo-aleatorios, el circuito que se comenta en el artículo está fijado.
También se podría introducir una matriz que represente a un circuito de forma manual, pero no las conexiones de este, que se
generaría de forma pseudo-aleatoria (La explicación está en los comentarios del proyecto)

6.En el mismo cuadro deberemos introducir a qué inputs queremos que responda nuestro circuito, ya que la salida que 
estos produzcan será la referencia que tomará el algoritmo genético para saber en qué punto de la reparación está.

7.A continuación tendremos que averiar el circuito, ejecutando el método averiar acompañado de las coordenadas [i][j] de 
la puerta que queremos averiar dentro de la matriz.

8.En la siguiente caja de código ya se ejecutará el AG que usará todo lo anterior. Aquí podremos cambiar el número de generaciones,
la probabilidad de cruce y la de mutación para los individuos.

9.El programa devolverá una lista con las estadísticas para cada generación y un conjunto con los 3 circuitos con mayor puntuación.
(Esta puntuación corresponde al número de bits de salida que son similares a los del circuito original entre todos sus outputs, no al número de salidas completas que devuelve igual que las del circuito no dañado)






-----------------EXPERIMENTOS REALIZADOS-----------------

Para los experimentos que hemos realizado hemos utilizado las siguientes variables:

Circuito de tamaño -> 4 * 4

Inputs -> Variables, desde 1 hasta 16 introducidos obviamente en binario.

Averias -> Desde 1 hasta 16, implicando todo el circuito averiado.






----------NUEVOS EXPERIMENTOS--------
Para nuevos experimentos podríamos jugar con estos valores, probando qué ocurriría en circuitos mucho mayores por ejemplo.

También podríamos cambiar las random.seed para obtener distintos circuitos dentro de un mismo tamaño.

Se podrían añadir averías o inputs según lo que estemos intentado estudiar.

Y por último podríamos cambiar el número de individuos por generación, las probabilidades de mutación y cruce ó el número de generaciones.





----PROBLEMAS ENCONTRADOS-----------------------

Por alguna razón, al cambiar las seeds, a veces el programa consigue un comportamiento no sólo erróneo, sino ilógico.

Llegando a imprimir cadenas de texto que no debería o incluso cayendo en un bucle en el que no encuentra una salida,
 cosa que utilizando
por ejemplo la seed 12345 no ocurre nunca
.