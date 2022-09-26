# T01 0822 Robot
# 
Un robot se desplaza horizontalmente por el eje X. Recibe las instrucciones de movimiento en un string, que contiene "I" para moverse una posición a la izquierda y "D" para moverse una posición a la derecha. Parte de una posición dada. Mostrar cuántos puntos diferentes visita el robot cuando se ejecutaron todos los comandos. Un punto se considera visitado si coincide con la posición del robot antes o después de ejecutar algún comando.

Input Format

Lee la secuencia de comandos y luego la posición inicial.

Constraints

La secuencia tiene como máximo 100 comandos y como mínimo 1 comando. Los comandos son "I" o "D". La posición inicial es un entero entre -10000 y 10000, ambos inclusive. Asumir datos válidos.

Output Format

Imprimir la cantidad de puntos diferentes alcanzados.

```
Sample Input 0

II
0
```
```
Sample Output 0

3
```
Explanation 0

Parte de la posición 0. Con el primer movimiento a la izquierda, queda en la posición -1, con el segundo movimiento a la izquierda, queda en la posición -2. En total, visitó 3 posiciones diferentes.

```
Sample Input 1

DDIIII
-10
```

```
Sample Output 1

5
```

Explanation 1

Parte de la posición -10, se desplaza a la derecha (llega a la -9), luego a la derecha (llega a la -8), luego a la izquierda (visita la -9 nuevamente), luego a la izquierda (llega a la -10 nuevamente), luego a la izquierda (llega a la -11) y finalmente a la izquierda (llega a la -12). Total de posiciones diferentes: 5.

```
Sample Input 2

I
10000
```

```
Sample Output 2

2
```
