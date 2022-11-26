## Lenguaje C. Código en varios archivos. Obtener el código objeto a partir del código fuente de los 3 archivos siguientes:

1. Creamos los archivos, empezando por *main.c*:
~~~~
nano main.c
~~~~
2. Añadimos codigo fuente a  *main.c*:
~~~~
#include <stdio.h>
int suma (int a, int b);
extern char *mensaje;
extern int num1, num2;
int main(){
printf("%s\n", mensaje);
printf("%d\n", suma (num1, num2) );
return 0;
}
~~~~
3. Creamos *suma.c*:
~~~~
nano suma.c
~~~~
4. Añadimos codigo fuente a  *suma.c*:
~~~~
int suma (int a, int b) {
return a + b;
}
~~~~
5. Creamos *datos.c*:
~~~~
nano datos.c
~~~~
6. Añadimos el codigo fuente a  *datos.c*:
~~~~
char *mensaje="Hola a todos y todas";
int num1 = 8;
int num2 = 10;
~~~~
7.  Por ultimo compilamos los tres usando.

~~~~
gcc -c main.c suma.c datos.c
~~~~
**Al ejecutar este comando obtendremos 3 archivos: main.o, suma.o y datos.o**

## Lenguaje C. Código en varios archivos. Obtener el código binario ejecutable a partir del código objeto de los 3 archivos anteriores:
Para obtener el codigo ejecutable apartir del codigo objeto usamos:
~~~~
gcc -o programa main.o datos.o suma.o
~~~~

## Deberemos obtener un archivo programa binario ejecutable. Si lo ejecutamos obtenemos el siguiente resultado:
~~~~
./programa
~~~~
~~~~
Hola a todos y todas
18
~~~~

> Nota: Obtenemos el "Hola a todos y todas porque está declarado en datos.

> Nota: Obtenemos el 18 porque en datos se declara que **num1**=8 y **num2**=10 y en suma que es una funcion que dice que **a** y **b** se suman y en el main se llama a la funcion suma y se declara que **a** es **num1** y **b** es **num2** lo esto da 18 como resultado.

