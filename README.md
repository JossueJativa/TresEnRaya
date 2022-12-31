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
El juego de Tres en Raya tiene muchas posibilidades para poder ganar, y de esto depende si el jugador o la máquina comienza primero. Suponiendo que el Jugador es X y la máquina O, en total hay unicmente 138 posiciones finales. Si empiezna las X, hay 91 posibilidades de que el Jugador gane, 44 posibilidades en las que la computadora gane y unicamente 3 en la que exista un empate; y todo esto viceversa si empieza la Maquina, es decir comienzan los O. 

Para armar un arbol de posibilidades tomando en cuenta esto, se debe considerar que se utiliza el algoritmo de Minmax, el cual se basa en un conjunto de datos que conforman contrucciones logicas basadas en nodos y sus conecciones. El algoritmo minmax ayuda a elegir el mojor movimiento, tomando en cuenta que se elegirá el peor movimiento para ti por parte del contrario, ya que la finalidad de ambos jugadores, es ganar el juego. El algoritmo Minmax es recursivo por lo que va regresando hacia atras, comunicando a su nodo superiro cual es el mejor nodo hoja alcanzado ahsta ese momento. 

![image](https://user-images.githubusercontent.com/121683973/210115686-5deba4d2-c911-4881-bced-a8efdf1fdeb5.png)

Si se decide armar el arbol de posibilidades desde cero del Tres en Raya, se debera iniciar con un tablero vacio, y las 9 posibilidades en las que el usuario ingrese su icono, ya sea X o O, y luego sera el turno del siguiente usuario, unicamente con 8 posibilidades para ingresar su icono, y asi sucesivamente hasta que todos los espacios esten llenos. 


## Instrucciones para ejecutar en Windows y Linux  

### Windows:
Para ejectar el programa en windows se puede proceder de tres diferentes formas:

* IDE: Se puede descargar y utilizar un IDE, como Visual Studio Code para correr el programa, se debe instalar el IDE de preferencia, con sus respectivos plugins para compilar cierto lenguaje y finalmente se deberá abrir el archivo que se desea ejecutar y correrlo. 

* CMD: Por otro lado se puede utilizar la linea de comandos de Windows para ejecutar el archivo. Para esto se instalará un compilador externo llamado G++
1. Descargar e instalar el compilador Mingw del siguiente enlace https://sourceforge.net/projects/mingw/files/latest/download?source=files tomando en cuenta que se deben descargar los compiladores de C y C++
2. Para configurar el compilador ir a las proppiedades del sistema, configuraciones avanzadas del sistema, y luego ir a configuracion de variables de entorno. Se puede utilizar el compilador ya sea en variables del sistema o variables de usuario, dependiendo de lo que se quiera. 
3. Finalmente para compilar algun codigo, se debe saber donde esta el codigo e ir a la consola y cambiar de directorio a la ruta donde se encuentre el programa que se desea compilar en C++ y se escribe "g++ nombreArchivo -o nombreADarAlEjecutable" y luego abrimos el archivo .exe en esa capeta y listo ya corre el archivo. 

* Online GDB: Se puede utilizar el compilador online, en el sigiente enlace: https://www.onlinegdb.com/
1. Ingresar al enlace
2. Importar el codigo desde tu PC al compilador online
3. Seleccionar el lenguaje para compilar "C++"
4. Finalmente dar click en "Run"
5. Y listo ya esta corriendo el programa. 

--- 
### Linux 
Para ejectar el programa en windows se puede proceder de tres diferentes formas: 

* IDE: Se puede descargar y utilizar un IDE, como Visual Studio Code para correr el programa, se debe instalar el IDE de preferencia, con sus respectivos plugins para compilar cierto lenguaje y finalmente se deberá abrir el archivo que se desea ejecutar y correrlo. 

* CMD: Primero se debe abrir el terminal de linux, y descargar el compilador. Para verificar si tenemos este, se debe escribir gcc --version para compilador de C y c++ --version para compilador de C++. Si no fueron encontrados los compiladores, se deben instalar. 
1. Escribir en el terminal "sudo apt install gcc" e ingresar contraseña y completar la instalacion 
2. Luego escribir en el termina "sudo apt get install g++" e ingresar contaseña y completar la instalacion. 
3. 

* Online GDB: Se puede utilizar el compilador online, en el sigiente enlace: https://www.onlinegdb.com/
1. Ingresar al enlace
2. Importar el codigo desde tu PC al compilador online
3. Seleccionar el lenguaje para compilar "C++"
4. Finalmente dar click en "Run"
5. Y listo ya esta corriendo el programa. 
