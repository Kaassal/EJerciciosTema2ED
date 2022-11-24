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
	

   `cat > HolaMundo.sh`
   
2. Escribimos, dentro de el archivo *HolaMundo.sh* el codigo.
    
    `ehco "Hola mundo"`
    
    >Para salir y guardar nuestro codigo pusamos Ctrl+D

3. Damos permisos de ejecucion al procrama usando:
`chmod +x HolaMundo.sh`

4. Ejecutamos el archivo

    `./HolaMundo.sh`
