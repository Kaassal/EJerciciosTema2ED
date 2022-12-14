# Automatiza el proceso de compilación de ejecutable y biblioteca, su enlazado y la generación del archivo ejecutable para código fuente en C con make. Haz uso de un buildfile.

Estos son los archivos utilizados en el ejercicio:

-   main.c
-   aritmetica.c
-   aritmetica.h
-   makefile con su respectivo código.

```
###################################################
#
#  EJEMPLO DE ARCHIVO 	Makefile    (cc0) jamj2000
#
###################################################


###### MACROS

# Compilador de C
CC     = gcc

# Opciones del compilador, en este caso Optimización
CFLAGS = -O

# Directorio de instalación
PREFIX = /usr/local

# Ejecutable resultante
OUTPUT = programa


###### REGLAS

# .PHONY indica objetivos especiales, que no corresponden a archivos
#
# Las reglas tienen la forma
# objetivo(target) : dependencias
# <TAB>	comando1 
# <TAB>	comando2
# <TAB>	...
#
# La primera regla es la regla por defecto, puede invocarse simplemente con la orden make

all: main.o  libaritmetica.so
	$(CC) $(CFLAGS)  -Wl,-rpath=$(PREFIX)/lib  main.o  libaritmetica.so  -o  $(OUTPUT)
.PHONY: all


main.o: main.c  aritmetica.h
	$(CC) $(CFLAGS)  -c  main.c


aritmetica.o: aritmetica.c
	$(CC) $(CFLAGS)  -c  -fPIC  aritmetica.c


libaritmetica.so: aritmetica.o
	$(CC) $(CFLAGS)  -shared  -fPIC  -o  libaritmetica.so  aritmetica.o


clean:
	rm  *.o  *.so  $(OUTPUT)
.PHONY: clean


install: all
	[ -d $(PREFIX) ] || mkdir $(PREFIX)
	[ -d $(PREFIX)/bin ] || mkdir $(PREFIX)/bin
	[ -d $(PREFIX)/lib ] || mkdir $(PREFIX)/lib
	install -m 0755 $(OUTPUT) $(PREFIX)/bin
	install -m 0644 libaritmetica.so $(PREFIX)/lib
.PHONY: install


help:
	@echo "Objetivos válidos para make:"
	@echo ""
	@echo "  all (el objetivo por defecto si no se indica nada)"
	@echo "  clean"
	@echo "  install"
	@echo "  help"
	@echo ""
.PHONY: help

```

1.  Lo primero que haremos será ejecutar make:

```
make

```

2.  Una vez dentro del make ejecutamos todo lo siguiente:

```
gcc -O  -c  main.c

```

```
gcc -O  -c  -fPIC  aritmetica.c

```

```
gcc -O  -shared  -fPIC  -o  libaritmetica.so  aritmetica.o

```

```
gcc -O  -Wl,-rpath=/usr/local/lib  main.o  libaritmetica.so  -o  programa

```

Ejecutar:

```
make install

```

> Nota: Con esto instalamos la biblioteca y el ejecutable en el sistema.
