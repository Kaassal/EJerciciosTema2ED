## 18. Bibliotecas. Crea una biblioteca dinámica en C que proporcione las funciones para sumar, restar, multiplicar y dividir 2 números enteros. Crea un programa que haga uso de ella y comprueba que se ejecuta correctamente

Como ejemplo se crea una biblioteca llamada `aritmetica` con las cuatro operaciones básicas: `suma`, `resta`, `multiplicacion` y `division`.
1. Creamos el archivo donde almacenaremos el codigo de nuestra bibioteca
~~~~
nano aritmetica.c
~~~~
2. Añadimos el codigo a nuestra biblioteca
~~~~
int suma (int sumando1, int sumando2) {

return (sumando1+sumando2);

}

int resta (int minuendo, int sustraendo) {

return (minuendo-sustraendo);

}

int multiplicacion (int numero1, int numero2) {

return (numero1*numero2);

}

float division (int dividendo, int divisor) {

return (dividendo/(float)divisor);

}
~~~~
3. Compilamos a código objeto dinámico

~~~~
gcc  -c  -fPIC  aritmetica.c
~~~~

>Se habrá generado un archivo  `aritmetica.o`  con código objeto dinámico.

4.  Empaquetamos en biblioteca dinámica  `libaritmetica.so`

~~~~
gcc  -shared  -fPIC  -o  libaritmetica.so  aritmetica.o
~~~~
5. Aunque el proceso de creación de la libreria ya está completo la usaremos en un programa para saber que funciona, primero creamos y añadimos el codigo a un archivo llamado programa.c
~~~~
nano programa.c
~~~~
~~~~
#include <stdio.h>

#include "aritmetica.c"

#define NUM1 5

#define NUM2 2

int main (){

printf ("Dados los números %d y %d\n", NUM1, NUM2);

printf ("La suma es %d\n", suma (NUM1, NUM2));

printf ("La resta es %d\n", resta (NUM1, NUM2));

printf ("La multiplicación es %d\n", multiplicacion (NUM1, NUM2));

printf ("La división es %f\n", division (NUM1, NUM2));

return 0;

}
~~~~
6. Compilamos 
~~~~
gcc -o programa programa.c
~~~~
7. Ejecutamos el programa 
~~~~
./programa
~~~~
