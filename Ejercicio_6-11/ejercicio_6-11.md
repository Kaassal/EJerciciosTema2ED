# Ejecuta el programa "Hola mundo" en los siguientes lenguajes:

En este documento se explica y demuestra como ejecutar  _"Hola Mundo"_  en distintos lenguajes.

Para esto estoy usando una maquina virtual corriendo **Linux**

>Nota:  La maquina virtual esta corriendo **Ubuntu**, ten en  cuenta que los comandos de los instaladores de paquetes pueden ser algo distintos en diferentes distros.


Los lenguajes usados son:

-   Bash
-   Python
-   PHP
-   Javascript (nodejs)
-   C
-   C++
-   Java
-   Ensamblador (nasm)
-   Ruby
-   Go
-   Rust
-   Lisp

Antes de poder instalar los paquetes es recomendable ejecutar el siguiente comando:


    sudo apt-get update

>**Apt-get update** sirve para actualizar los repositorios que definimos en el archivo **/etc/apt/sources.list**. Se actualizan los listados de paquetes disponibles en las fuentes definidas en el archivo sources.list, pero no instala nada. Lo que hace es ver si hay nuevas versiones de los paquetes que tenemos en las fuentes definidas, pero sin modificar nada en nuestro sistema.
  
Luego instalamos los paquetes usando :

    sudo apt-get install python3.6  php  nodejs  gcc  g++  openjdk-8-jdk  ruby  golang  rustc  clisp nasm
## Bash 
Como la terminal de linux ya utliza bash no tenemos que instalar nada más para que poder interpretar Bash.
Podemos ejecutar el siguiente comando para comprobarlo:

    echo "Hola mundo"
### Ejecutar "Hola mundo" en Bash 
1. Creamos un archivo *.sh* donde escribiremos el codigo de *Hola Mundo*
	
~~~
   cat > HolaMundo.sh
~~~


   
2. Escribimos, dentro de el archivo *HolaMundo.sh* el codigo.
    
    ~~~~
    echo "Hola Mundo"
    ~~~~
    
    >Para salir y guardar nuestro codigo pusamos Ctrl+D

3. Damos permisos de ejecucion al procrama usando:

~~~~
chmod +x HolaMundo.sh
~~~~
4. Ejecutamos el archivo
~~~~
    ./HolaMundo.sh
~~~~
## Python
Hola mundo en python.

Python es un lenguaje **interpretado**, por lo tanto podemos abrir su interprete en la terminal para probar hola mundo:
~~~~
python3
~~~~
Escribimos el programa para probarlo 
~~~~
print ("Hola mundo")
~~~~
>Pulsa Ctrl+D para salir del interprete
   
### Python Script ejecutable

   1. Creamos un archivo *.py* donde escribiremos el codigo de *Hola Mundo*
	
~~~
   cat > HolaMundo.py
~~~


   
2. Escribimos, dentro de el archivo *HolaMundo.py* el codigo.
    
    ~~~~
    print ("Hola Mundo")
    ~~~~
    
    >Para salir y guardar nuestro codigo pusamos Ctrl+D

3. Damos permisos de ejecucion al procrama usando:
~~~~
chmod +x HolaMundo.py
~~~~
4. Abrimos el interpre te y ejecutamos el archivo
~~~~
    ./HolaMundo.py
~~~~


## PHP

_"Hola Mundo en PHP"_  
Al igua que Python **PHP** es un **lenguaje interpretado**. Entonces podemos abrir el interprete y probar "Hola mundo". Para abrir el interprete usamos:

~~~~
php -a

~~~~

Para probar el programa escribimos:

~~~~
echo "Hola Mundo";

~~~~
>Pulsa CTRL + D para salir del intérprete.

### PHP Script ejecutable

1.  Creamos un archivo de texto llamado  **HolaMundo.php**  donde escribriemos el codigo de "Hola Mundo"
~~~~
cat > Holamundo.php
~~~~
2.  Escribimos el código:
~~~~
<?php 
  echo "Hola mundo"; 
?>
~~~~

3.  Le damos permisos de ejecucion al programa:
~~~~
chmod +x HolaMundo.php
~~~~

4  Abrimos el intérprete y ejecutamos el programa:

~~~~
php ./Holamundo.php
~~~~
## Javascript (nodejs)

Hola mundo en Javascript
Como Javascript es un lenguaje interpetado podemos usar el interprete para probar "Hola mundo" de la siguiente manera:

1.  Ejecutamos el intérprete.

node

2.  Escribimos el codgio.

console.log('Hola mundo');

> Para salir del intérprete pulsamos CTRL+D.

### Nodejs Script ejecutable
1. Creamos un archivo de texto llamado  **HolaMundo.js**  donde escribriemos el codigo de "Hola Mundo"

2. Escribimos el codigo en el archivo   **HolaMundo.js**
~~~~
#!/usr/bin/env node

console.log('Hola mundo');
~~~~
3.  Le damos permisos de ejecución a programa usando:
~~~~
chmod  +x  HolaMundo.js
~~~~
4.  Abrimos el interprete y ejecutamos el programa
~~~~
node ./HolaMundo.js
~~~~
# C

_"Hola Mundo"_  en C.

Ejecutar el programa

1.  Creamos un archivo de texto llamado  **HolaMundo.c**  y escribimos el código:

~~~~
#include <stdio.h>
int main
{
printf("Hola Mundo");
return 0;
}

~~~~
2.  Compilamos y enlazamos:

~~~~
gcc -o HolaMundo HolaMundo.c

~~~~
3.  Abrimos el intérprete y ejecutamos el programa:

~~~~
./Holamundo
~~~~
