## Bibliotecas. Define qué se entiende por biblioteca o librería y los tipos que existen.
### ¿Que es una librería?
Una **librería** es un conjunto de archivos que se utiliza para desarrollar software. Suele estar compuesta de código y datos, y su fin es ser utilizada por otros programas de forma totalmente autónoma. Simple y llanamente, es un archivo importable.

---
### ¿Que tipos de libreías existen?

- 1.  **Bibliotecas estáticas:** es un fichero que contiene varios archivos de  **código objeto** en su interior que se utilizan en los ficheros ejecutables, copiándolos y relocalizandolos según la necesidad. En este caso la biblioteca actúa como recipiente de archivos.

- 2.  **Bibliotecas dinámicas**: son archivos que tienen código objeto construidos de manera independiente a su ubicación. Esto nos indica que este tipo de bibliotecas se utilizan cargando los archivos en el tiempo de ejecución y no se enlazan en el tiempo de compilación; siendo esta su diferencia respecto a las estáticas, que se enlazan.


- 3.  **Bibliotecas remotas**: Esta es una biblioteca que utiliza ejecutables separados y por medio de un procedimiento remoto, llevado a cabo por otro ordenador. Estas bibliotecas trabajan con un enfoque que maximiza la reutilización del sistema operativo; el código que soporta la biblioteca es el que le da a la aplicación el soporte y seguridad para otro programa. 
