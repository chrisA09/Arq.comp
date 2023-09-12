# Conceptos de electricidad

## Electricidad

*Electronica*: parte de la fisica que estudia los cambios y los movimientos de los electrones libres y la accion de las fuerzas electromagneticas y los utiliza en aparatos que reciben y transmiten informacion.

*Partes del atomo:*

- Electrones: poseen carga electrica negativa.
- Protones: poseen carga electrica positiva.
- Neutrones: poseen carga electrica neutra.

las cargas electricas opuestas se atraen  
los electrones orbitan alrededor del nucleo.

> La electricidad se manifiesta cuando por algun mecanismo o proceso los electrones son liberados del atomo.

### Corriente electrica

- Los electrones son obligados a separarse de su nucleo
- La fuerza que los obliga a separarse es el campo electrico
- Los electrones libres viajan de atomo en atomo atraves del material --> ese flujo de electrones se denomina corriente electrica

> La corriente electrica es un proceso dinamico

### Conductores

- Permiten la circulacion de los electrones libremente
- Electrones levemente retenidos por sus nucleos
- Estos electrone pueden facilmente ser liberados de los atomos cuando se le aplica una diferencia de potencial
- La fuerza de retencion quelos nuecleos realizan sobre los electrones se denomina "resistencia electrica"

> cuantos menor oposicion a liberar electrones -> menor resistencia

Materiales:  

- oro
- plata
- cobre
- aluminio

### Aislantes

- no permiten la libre circulacion de electrones
- electrones fuertemente retenidos por sus nucleos
- la resistencia electrica es muy elevada

Materiales:

- plastico
- vidrio
- aceites
- ceramica certificada
- vacio

## Semiconductores

Permiten que el flujo de electrones pueda ser controlado con precision

A fines de 1940 se comenzo a usar el transistor ("transfer resistor"), con esto se dio inicio a la era de la "electronica en estado solido", reemplazando a la valvula de vacio siendo mas eficiente y volumenes significativamente menores

### Tipos

Componentes `pasivos`:  
resistor  
capacitor  
inductor  

Componentes `activos`:  
valvula de vacio(casi obsoleta)

### circuitos integrados

Nace de la tecnica para construir circuitos con mas de un componente en solo dispositivo de estado solido

Estos circuitos tiene capacidades desde una simple funcion logica de pocos transistores a computadores completos

### unidades de medicion de la electricidad

- Voltaje:  
Fuerza o tension causada porla separacion entre electrones y protones  
Unidad de media: volt [V]

- Corriebte electrica:  
el libre flijo de electrones en un circuito electrico  
Unidad de media: ampere [A]

- Resistencia:  
impedimento u oposicion al flujo de electrones  
Unidad de media: [Ω]

### Relacion entre voltaje, corriente y resistencia

Las tres magnitudes fisicas estan relacionadas enter si por medio de la ley de ohm

> Ley de Ohm
>
> I = V / R

la corriente es directamente proporcional al potencial electrico e inversamente proporcional a su resistencia

### Circuito electrico

Es todo camino cerrado por donde pueden circular los electrones.  
Para que estos circulen se necesita una diferencia de potencial y un conductor que cierre el circuito

- Potencia electrica instantanea(P):  
"velocidad" con la que se transforma la energia  
Unidad de media: watt [W]

> P = V x I

- Potencia enegia/calor intercambiada (P):  
la energia E se mide en joule, T es tiempo  
Unidad de media: watt [W]

> P = E / t

- Frecuencia(F):  
es medida en hertz(hz) o ciclos por segundo
Unidad de media: hertz [Hz]

- Periodo(T):  
es el tiempo que requiere una señal para realizar un ciclo
Unidad de media: segundos [s]

> F = 1 / T
>
> La frecuencia equivale a la inversa del periodo

## Señales

### Tipos de señales

- Señal analogica: sonidal pura.
- Señal digital: señal cuadrada.

#### Computador electronico

`computador analogico`: opera con valores y funciones continuas.  
`computador digital`: opera con digitos, valores discretos.  
`computador digital binario`: opera dos digitos asociados a 0 y 1.  
`computador hibrido`: opera con partes digitales y partes analogicas.

#### Modulacion

Es el conjunto de tecnicas para transportar informacion sobre una onda portadora, tipicamente una onda senoidal.

> demodulacion es el proceso contrario

##### tipos de modulacion

- modulacion en amplitud
- modulacion en frecuencia
- modulacion en fase
- otras.

#### Comunicacion Serie

cada conjunto de señales se envia alternativamente por un solo par de conductores, total dos conductores(1 canal señal/retorno)

#### Comunicacion Paralelo

cada conjunto de señales se envia en un solo instante y se necesita un conductor por cada señal, o sea para este caso 8(conductores de señales) mas el retorno, total de nueve conductores(canales de 8 señales/retorno)

#### Tipos de comunicacion

- Simplex: los datos fluyen del emisor al receptor solamente y nunca en sentido contrario.  
no se espera reaccion alguna de los datos enviados, utiliza un solo canal.

- Half duplex: los datos fluyen entre ambos pero solo en un sentido a la vez. En cada extremo debe haber un transmisor-receptor. Se utiliza un canal

- Full duplex: los datos fluyen entre ambos simultaneamente. Se obtiene el mayor indice de eficacia en la utilizacion del medio, utiliza dos canales simultaneos.
