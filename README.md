# TresEnRaya
Integrantes: Enrique Merizalde, Andres Loza, Jossue Jativa, Jaime Mendoza
---
## Descripción del Juego:
Tres en raya es un juego de 2 jugadores, que se juega sobre una matriz de 3 filas x 3 columnas. El juego consiste en que uno de los jugadores utiliza "X" y el otro "O" en distintas posiciones de la matriz segun el turno correspondiente. El primer jugador en conseguir tener 3 de sus figuras, ya sea "X" o "O", de manera vertical, horizontal o diagonal, habra ganado el juego. Si ninguno gana, se considera un empate. 


## Explicar las principales rutinas 
Las principales rutinas que posee este codigo son: 
* ShowBoard: Esta funcion vacía mostrará el tablero de 3 filas x 3 columnas donde se jugará Tres en Raya.
* ShowInstructions: Esta funcion vacía muestra la tabla con valores del 1 al 9 indicando al usuario como jugar Tres en Raya, tomando en cuenta se utilizaran los respectivos numeros del 1 a 9 para mostrar las 9 diferentes posiciones en las que puede jugar el usuario. 
* Initialise: Esta funcion vacía inicializa el tablero vacio 
* DeclareWinner: Esta funcion vacía nos permit delarar el ganador de la partida de 3 en raya
* RowCrossed: Esta funcion booleana devolvera verdadero si alguna de las filas se cruza con la jugada del mismo jugador, sino devolvera falso 
* ColumnCrossed: Esta funcion booleana devolvera verdadero si alguna de las columnas se cruza con la jugada del mismo jugador, sino devolvera falso 
* DiagonalCrossed: Esta funcion booleana que devolvera verdadero si alguna de las diagonales se cruza la jugada del mismo jugador, sino devolvera falso 
* GameOver: Esta funcion booleana devolverá verdadero si e juego finaliza y sino devolvera falso.
* Minmax: Esta funcion int devuelve un entero, seteando incilmente el score a cero y el bestscore a cero. Luego se verifica si la partida ya ha terminado o no. Si la partida no ha ternimado se ejecuta un algoritmo que nos devolver el bestScore.
* Bestmove: Esta funcion calcula el mejor movimiento y devuelve un entero. Se tilizan dos ciclos for, uno para recorrer las filas de la matriz y uno para recorrer las columnas de la matriz, y luego se calcula el mejor movimiento devolviendo x*3+y;
* PlayTresEnRaya: Esta es la funcion principal del programa y es vacia, la cual permite como tal jugar tres en raya, ya utiliza todas las demas funciones dentro de ella para pdoer ejecutar el juego.
* Main Esta funcion es el main del prograa, es decir donde corre, la cual nos preguntará si deseamos jugar o salir, y luego si deseamos que la maquina comience o que el usuaurio comince jugando, y dependiendo de esto se ejecutará el juego. 


## Tabla de tiempos en mejores y peores casos
Al jugar tres en raya existen los mejores y los peores casos, es decir donde los jugadores tienen mayores probabilidades de ganar o menores porobabilidades de ganar. En este sistema podemos dividir el tiempo de mejores y peores casos en 2, mejores y peores casos para el humano y la máquina. 
* Humano: Para los humanos, en los mejores casos, usualmente el tiempo que se demoran en tomar una decision en base a la partida que se esta jugando son de 10 a 20 segundos. Por otro lado, en los peores casos, las personas se toman un maximo tiempo de 1 minuto para tomar la decision de su siguiente movimiento. 
* Máquina: Para la Computadora, los mejores y peores casos usualmente toman relativamente el mismo tiempo en tomar una desicion para el siguiente movimiento, ya sea en un mejor o peor resultado, debido a que las maquinas siguen una serie de pasos o algoritmos establecidos que permiten definir de manera rapida la mejor forma de jugar la partida. Usualmente este tiempo es menor a 1 segundo.

> Nota: En ambos casos podemos percatarnos de que los tiempos son bajos, pero los de la computadora son mucho mas bajos que el de los humanos, y esto es debido a que unicamente se juega tres en raya sobre una matriz de 3 filas x 3 columnas, por lo que a medida que hipteticmanete vaya incrementando el tamaño de esta matriz, el tiempo que tomará en tomar una desicion ya sea la computadora o el humano, ira incrementando.


## Tabla Estudio Combinatorio del Juego (Arbol de posibilidades)
El juego de Tres en Raya tiene muchas posibilidades para poder 


## Instrucciones para ejecutar en Windows y Linux  




