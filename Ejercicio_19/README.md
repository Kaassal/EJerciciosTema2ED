## Crea una biblioteca dinámica en Java que proporciona las funciones para sumar, restar, multiplicar y dividir 2 números enteros. Crea un programa que haga uso de ella y comprueba que se ejecuta correctamente.

1.  Creamos un archivo aritmetica:

```
mkdir aritmetica

```

2.  Creamos clase  **aritmetica/Aritmetica.java**:
~~~~
nano Artitmetica.java
~~~~

```
package aritmetica;

public class Aritmetica {

  public static int suma (int sumando1, int sumando2) {
        return (sumando1+sumando2);
  }

  public static int resta  (int minuendo, int sustraendo) {
        return (minuendo-sustraendo);
  }

  public static int multiplicacion (int  numero1, int numero2) {
        return (numero1*numero2);
  }

  public static float division (int dividendo, int divisor) {
        return (dividendo/(float)divisor);
  }

}

```

3.  Compilamos:

```
javac  aritmetica/Aritmetica.java

```

> Nota: Obtenemos como resultado  _aritmetica/Aritmetica.class_.
 ### Crear programa usando la biblioteca

1.  Creamos un archivo Main.java y escribimos el codigo:
~~~~
nano Main.java
~~~~

```
import aritmetica.Aritmetica;

public class Main {

  private static final int NUM1 = 5;
  private static final int NUM2 = 2;


  public static void main (String[] args) {
    System.out.println ("Dados los números " + NUM1 + " y " + NUM2 );
    System.out.println ("La suma es " + Aritmetica.suma(NUM1, NUM2) );
    System.out.println ("La resta es " + Aritmetica.resta(NUM1, NUM2) );
    System.out.println ("La multiplicación es " + Aritmetica.multiplicacion(NUM1, NUM2) );
    System.out.println ("La división es " + Aritmetica.division(NUM1, NUM2) );
  }


}

```

2.  Compilamos:

```
javac  Main.java

```

> Nota: Obtenemos un archivo  _Main.class_.

3.  Ejecutamos:

```
java  Main
```
