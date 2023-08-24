# Sistemas de numeracion

Exiten disintos sistemas de numeracion, algunos persisten como los romanos, los chinos tiene una forma particular de agrupar los numeros.

## Sitemas no posicionales

En estos, el valor del simbolo no depende de la posicion que este ocupe dentro del nro. Como el sistema de numeracion romano.

## Sitemas posicionales

### Teorema fundamental de la Numeración

el valor del simbolo depende de la posicion que este ocupe dentro del nro. Como el sistema decimal.

Para el nro 221

el nro esta en base 10, la posicion signfica una potencia de la base multiplica al digito.

El digito que vale una unidad(de der a izq, la 1ra posicion), que se encuentra en la pocision 1 entonces la base, que es 10, esta elevada a la potencia 0.  
En la segunda posicion, la base se encuentra elevada a la potencia 1.  
En la tercera posicion, la base, se encuentra elevada a la potencia 2.

> 221 = 2 x 10^2 + 2 x 10^1 + 1 x 10^0

Los dígitos varían entre b símbolos [0 y b-1]. Valores posibles de los diez dígitos en base 10 : [0,1,2,3,4,5,6,7,8,9]

Nº(b)= *`dn bn +… d2 b2 + d1 b1 + d0 b0`+ d-1 b-1 + d-2 b-2 +d-3 b-3…+ d-k b-k*

>En color es la parte entera, en blanco la parte fraccionaria

*nota:* en una fraccion cuando en el numerador se encuentra una potencia negativa, es lo mismo que pase dividiendo al denominador con la potencia cambiada de signo.

*ej:* 2 x 10^-1 --> 2 / 10^1

### Ejemplos de bases usadas en informatica

- BASE 2 (binaria) b= 2 d= [0,1]
- BASE 8 (octal) b= 8 d= [0,1,2,3,4,5,6,7]
- BASE 10 (decimal) b=10 d= [0,1,2,3,4,5,6,7,8,9]
- BASE 16 (hexadecimal) b=16 d= [0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F]

En este último caso los símbolos faltantes de los dígitos de la numeración arábiga se reemplazan
con las primeras letras del alfabeto para cubrir los números decimales 10,11,12,13,14 y 15  

>*La potencia es la cantidad de digitos que necesito para representar una cantidad*

### Sitema de numeracion Decimal

i es la posición respecto a la coma o punto.  
La primera posición a la derecha de la coma i=-1.  
La primera posición a la izquierda de la coma i=0.

El nro `123,456` en decimal puede expesarse, mediante descomposicion en terminos, como:

> 1x10^2 + 2x10^1 + 3x10^0 + 4x10^-1 + 5x10^-2 + 6x10^-3

### Sistema Trinario

- Base 3
- Símbolos: [0, 1, 2 ]

*trampa de parcial*: pide cambiar un nro de base 16 a decimal, ej: 1111, el error comun es poner F, pero eso no es base 16, es base 2 en hex.

### Sistema Binario

- Base 2
- Símbolos: [0, 1]

### Sistema Octal

- Base 8
- Símbolos: [0 1 2 3 4 5 6 7]

### Sistema Hexadecimal

- Base 16
- Símbolos: [0 1 2 3 4 5 6 7 8 9 A B C D E F]

## Conversion de sistemas numericos

### Decimal a Binario

Parte entera: metodo de divisiones sucesivas por 2  
Parte fraccionaria: metodo de multiplicaciones sucesivas por 2

*nota:* si tengo un nro binario negativo, `sin codificacion`, se representa de la misma manera que cualquier nro, es decir un menos por delante.

De la sucesion de divisiones de la parte entera, para saber el nro binario que da, se lee desde el ultimo resultado hasta el primer resto y se escribe en ese orden.

La multiplicacion sucesiva se detiene cuando:

- da exacto
- cuando se repite un resultado(significa que es periodico)
- puede ser un numero irracional.(ej. raiz de 2)

con 4 digitos alcanza, excepto que se trabaje en codificacion de punto flotante, cuando la fraccion tiene que representar una cantidad de bits.

### Decimal a Octal

Parte Entera, Método de las divisiones sucesivas por 8.
Parte Fraccionaria, Método de las multiplicaciones sucesivas por 8.

### Octal a Decimal

Se aplican los pesos correspondientes al sistema octal.  
O sea se aplica el Teorema fundamental de la Numeración.

### Octal a Binario

#### Tabla BCO - Binari Coded Octal

esta el grafico en los apuntos, voy a agregar una imagen aca mas adelante.

Por cada símbolo octal se pone su equivalente en binario

se usan tres digitos de binario, por uno octal.

### Octal a Hexadecimal

- Hay que llevar a cabo un paso intermedio; es decir, pasar el número a decimal o binario y éste, por ultimo, a hexadecimal.

- En enteros no hay problema con pasar de hex a decimal y despues pasar el decimal a binario.
Pero si es un nro con fraccion va a dar error, en ese caso, pasa el nro 37 a binario escribiendo el equivalente octal de cada digito y agrupando ese resultado de a 4 digitos y reamplaza el digito hex como corresponde sumando ceros segun dicte la coma

### Hexadecimal a Decimal

- Se desarolla el polinomio equivalente, Teorema fundamental de la numeracion.

### Hexadecimal a Octal

- Hay que llevar a cabo un paso intermedio; es decir, pasar el número a decimal o binario y éste, por ultimo, a octal.

## Resumen

- `Cualquier sistema` para convertirlo a `decimal` --> Teorema fundamental de la numeracion.
- `Octal` a `Decimal` y Viceversa --> `Paso intermedio a Binario`.
- `Hexadecimal` u `octal` a `binario` --> Se toma cada símbolo se convierte a `binario` y se toman todos los  bits como si fuera un solo número.
- `Hexadecimal` a `Octal` o viceversa --> `paso intermedio a binario` y despues a la base que corresponda. En octal se pasa a binario con la tabla BCO
