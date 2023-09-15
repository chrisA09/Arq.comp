# Codificacion Binaria

## Sistemas numericos

### Lineales

Permite la representacion continua de los infinitos valores posibles de nros expresador en cualquier base mediante el polinomio del *teorema fundamental de la numeracion* con la sumatoria de infinitos terminos

> Cualquier valor de la magnitud analogica puede ser expresado

### Modulares

Podemos definir al modulo como la *maxima contidad de simbolos* que puede representar el sistema. `Este es el caso usado mayoritariamente en un computador actual`. El `almacenamiento es modular y binario` solo se puede representar una cierta cantidad de digitos binarios o bits en el bloque asignado.

## Sistema binario modular

Lo utilizan internamente los circuitos electronicos digitales. Cada nro se representa en este sistema por un conjunto de elementos, denominados `*bit*`.

- valor logico del bit -> "0" o "1"
- valor fisico del bit -> estados electricos de distinto valor

### Byte

Es el conjunto de 8 bits, y es la unidad elemental de medida de la informacion representada por este sistema. Un byte es un bloque de 8 bits.

- MSB: Most significant bit
- LSB: Least significant bit

### Bolques comunes utilizados por MS-Windows

Byte = B (8 bits)  
Word = W (12 bits)  
Double Word = DW (32 bits)  
Quadruple Word = QW (64 bits)

> Estos bloques son los más utilizados por las codificaciones para los tipos de datos estándar de los diferentes lenguajes. Dependiendo del tipo de arquitectura o para tipos  de datos definidos por el usuario  se pueden ver otros bloques ; 80 bits, 128 bits 256 bits, etc

## Codigos

Representacion de ciertos elementos a traves de la asignacion, a cada una de ellos, de una combinacion determinada de simbolos.

- Codigos binarios: Son aquellos que en el alfabeto del codigo lo integran los digitos binarios 0 y 1.

- Codigos de bloque:  las distintas palabras tiene todas el mismo nro de simbolos. Pueden coincidir con un modulo para tratamiento de la informacion. Ej un byte

Los codigos que se necesitan codificar con cierta frecuencia, han sido estandarizados.  
Estos son:  

- Codigos de cambio unico(un bit entre codigos consecutivos). *ej: grey,exceso 3,etc*

- Codigos para representar los caracteres alfanumericos. *ej: letras, nros, signos de puntuacion, control, graficos,etc. ASCII, ANSI EBCDIC, UNICODE*

- Codigos para representar numeros. *ej: Naturales, Enteros, Reales, Complejos*

- Codigos detectores(EDC) y/o los correctores (ECC) de errores. *Ej: Parity(P), Cyclic Redundancy Check(CRC), Hamming, etc*

### Codigos de cambio unico

- Codigos continuos: La combinacion que representa a un elemento no difiere mas que en un bit de la combinancion que representa al elemento anterior.

- Codigo ciclico: Tampoco difieren en mas que un bit las combinaciones correspondientes al primer y al ultimo elemento.  
*Ej.*

| Elementos | b1 | b0 |
|:---------:|----|----|
|     A     |  0 |  0 |
|     B     |  0 |  1 |
|     C     |  1 |  1 |
|     D     |  1 |  0 |

- `Codigo Gray o Binario reflejado`: Gray desarollo una forma sistematica para diseñar codigos continuos y ciclicos para distitntos nros de elementos.

1. Cualquier secuencia de palabras del codigo Gray forman un codigo continuo.
1. El codigo Gray es un codigo de bloque.
1. Tomando las primeras palabras 2n palabras del codigo forman un codigo ciclico.
1. Dada una lista con las primeras 2n palabras del codigo Gray, las palabras ubicadas simetricamente con relacion al eje que divide la lista en dos solo difieren en 1 bit.
1. Como consecuencia de lo anterior, si de una lista de las primera 2n palabras del codigo se suprimen simetricamente las primeras m palabras y las ultimas m, la lsita resultante es un codigo ciclico de (2n-2m) elementos.

| b3 | b2 | b1 | b0 | b3 | b2 | b1 | b0 |
|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
|  0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
|  0 |  0 |  0 |  1 |  0 |  0 |  0 |  1 |
|  0 |  0 |  1 |  0 |  0 |  0 |  1 |  1 |
|  0 |  0 |  1 |  1 |  0 |  0 |  1 |  0 |
|  0 |  1 |  0 |  0 |  0 |  1 |  1 |  0 |
|  0 |  1 |  0 |  1 |  0 |  1 |  1 |  1 |
|  0 |  1 |  1 |  0 |  0 |  1 |  0 |  1 |
|  0 |  1 |  1 |  1 |  0 |  1 |  0 |  0 |
|  1 |  0 |  0 |  0 |  1 |  1 |  0 |  0 |
|  1 |  0 |  0 |  1 |  1 |  1 |  0 |  1 |
|  1 |  0 |  1 |  0 |  1 |  1 |  1 |  1 |
|  1 |  0 |  1 |  1 |  1 |  1 |  1 |  0 |
|  1 |  1 |  0 |  0 |  1 |  0 |  1 |  0 |
|  1 |  1 |  0 |  1 |  1 |  0 |  1 |  1 |
|  1 |  1 |  1 |  0 |  1 |  0 |  0 |  1 |
|  1 |  1 |  1 |  1 |  1 |  0 |  0 |  0 |

- Codigos de caracteres alfanumericos.

se consideran caracteres a:

los codigos de control(ctrl, LF, TAB, SPACE)  
los digitos(0,.....,9)  
las letras (A,......,Z,a.....z)  
los signos de puntuacion(".",",",";", etc...)  
los caracteres especiales("*", "&", "$", "Ñ", "ü"...)

> Para representarlos se asignan codigos numericos mediante una tabla. El computador opera con los codigos, no con los simbolos graficos.

### Distintos tipos de esquemas de codificacion

Un esquema de codificacion especifica los codigos que tanto un computador o terminal pueden mostrar  y recibir.  
Se utilizan para interpretar los datos en simbolos significativos desde una terminal o maquina Host.  
Diferentes esquemas de codificacion:

- unico byte.
- multiples bytes.
- cantitdad de bits para la codificacion variable.
- cantidad de bits para la codificacion fijo.

## Ejemplos de codigos

- Codigo morse

Telegrafo electrico y optico dos señales de distinta duracion. (dot and dash)

- Codigo BAUDOT

Longuitud fija de 5 bits. Utilizado en telex/teletipo. Codifica solo las letras mayusculas, opera en forma contextual.

- Codigo BCDIC (`B`inary `C`oded `D`ecimal `I`nterchange `C`ode)

Longuitud fija de 6 bits. Utilizado por muchos sistemas de la firma IBM. Codifica solo letras mayuscula.

- Codigo EBCDIC (`E`xtended `B`inary `C`oded `D`ecimal `I`nterchange `C`ode)

Surgido en 1964 con el sistema IBM S360. Longuitud de 8 bits. Utilizado en algunos sistemas mainframe.

- Codigo ASCII (`A`merican `S`tandard `C`ode for `I`formation `I`nterchange)

Se utiliza para la representacion de los caracteres de texto (alfanumericos) del alfabeto ingles, los signos de puntuacion y algunos comandos.  
Propuesto en 1963 y finalizo en 1968.  
Esquema de longuitud fija.  
ASCII original. Longuitud de codigo de 7 bits o sea 128 caracteres, se hizo estandar en los EEUU.  
ASCII extendido(EASCII).Ampliacion para caracteres internacionales, con una longuitud de 8 bits.  
Muy usuado actualmente.

- Codigo ANSI (`A`merican `N`ational `S`tandards `I`nterchange)

Ultimas normas sobre el ASCII establecida a traves ISO-14962-1997.  
ANSI X3.64(Tambien denominado ECMA-48)  
Definido en 1991, se utiliza para la representacion de los caracteres de texto(alfanumericos) del alfabeto ingles internacionalizado, los signos de puntuacion, algunos comandos, mover el cursosr y cambiar colores frente/fondo.  
Esquema de longuitud fija.  
Longuitud de codigo. 8 bits.  
Muy usuado actualmente. (Windows y otros SO.)

- Codigo UNICODE

Norma de codificacion de caracteres que puede representar todos los caracteres utilizados por los computadores.

Norma establecida por Apple y Xerox en 1988

En 1991 se establece un comite con la participacion de Adobe, Aldus, Apple, IBM, Microsoft, Sun, Xerox, entre otros... y establecen la norma Unicode.  

Longuitud fija de 16bits. UTF-16.  

> Existen codificaciones de 8bits UTF-8 y 32 Bits UTF-32.

La version 2.0 representa hasta 38885 caracteres.  

UCS-2 (`U`niversal `C`haracter `S`et 2 byte form). Es un codigo de 2 bytes con formato de longuitud fija.  

UTF-8(`U`niversal character set `T`ransformation `F`ormat). Es multibyte, con un formato de longuitud variable.

Tanto el UCS-2 como el UTF-8 codifican el mismo repertorio de caracteres tanto en unicode 1.1 o unicode 2.0  

El unicode 2.0 codificado como UTF-8 incluye el ASCII/ANSI utilizando la codificacion en un unico byte.
