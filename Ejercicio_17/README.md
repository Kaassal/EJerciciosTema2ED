## Bibliotecas. ¿Qué tipo es el más utilizado actualmente? ¿Por qué?

Las bibliotecas mas utilizadas a dia de hoy son las bibiotecas dinamicas, por las siguientes razones:

### Usando una libreria estática
-   El programa  **ocupa más espacio en disco**, ya que las librerías necesarias se encuentran en el propio programa. Como ventaja tenemos lo podemos llevar de un sistema a otro sin necesidad de migrar también las librerías (ya que están incluidas)
-   El programa en sí  **consume más RAM en ejecución**, ya que las librerías están embebidas. Sin embargo,  **se ejecuta en principio más rápido**  ya que todo lo necesario está incluido en el propio programa.
-   Si una biblioteca que se utilizó durante la compilación se actualizara,  **sería necesario recompilar**  el programa para que incluyera los cambios que se han realizado en esa biblioteca.

### Usando una libreria dinamica
-   Obtenemos programas de **tamaño reducido**, ya que sólo incluyen referencias a las bibliotecas y nada embebido.  Además esto resulta en una **menor ocupación en RAM**.
-   El programa puede sacar partido de las actualizaciones de las bibliotecas  **sin necesidad de recompilar**.
>Es importante que estas bibliotecas tengan un sistema de versiones, ya que:
>-   En ocasiones las  **actualizaciones de bibliotecas no son compatibles**  con los programas que las utilizan. Por ello hay un sistema de versionado en las bibliotecas compartidas.
