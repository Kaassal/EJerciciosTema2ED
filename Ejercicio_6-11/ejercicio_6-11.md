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
