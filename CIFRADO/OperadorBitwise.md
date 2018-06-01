## Operadores a nivel de bits

Existen escenarios donde conocer el funcionamiento de estos operadores permite mejorar el rendimiento de las aplicaciones o crear estructuras más complejas.

Una operación bit a bit, opera sobre números binarios a nivel de bits individuales. Es una acción primitiva sustancialmente más rapida que las que se llevan a cabo sobre el valor real de los operandos.

Los bitwise son operadores de 32 bits en javascript. Lo que significa que los números se rellenan con ceros a la izquierda, los cuales pueden despreciarse porque no tiene un significado o valor.

Lista de operadores:

| Operador | Representación | Descripción                                                  |
| -------- | -------------- | ------------------------------------------------------------ |
| &(AND)   | a & b          | Devuelve 1 si ambos operandos son 1                          |
| \| (OR)  | a \| b         | Devuelve 1 donde uno o ambos operandos son 1                 |
| ^ (XOR)  | a ^ b          | Devuelve 1 donde un operando, pero no ambos, es 1            |
| ~ (NOT)  | ~ a            | Invierte el valor del operando                               |
| <<       | a << b         | Desplaza a la izquierda un número especificado de bits       |
| >>       | a >> b         | Desplaza a la derecha un número especificado de bits. Este operador presenva el signo. |
| >>>      | a >>> b        | Desplaza la derecha un número especificado de bits descartando los bits desplazados y sustituyéndolos por ceros. Rellena de ceros a la derecha |

OPERADOR BIT A BIT **AND**

| a    | b    | a & b |
| ---- | ---- | ----- |
| 0    | 0    | 0     |
| 0    | 1    | 0     |
| 1    | 0    | 0     |
| 1    | 1    | 1     |

OPERADOR BIT A BIT **OR**

| a    | b    | a \| b |
| ---- | ---- | ------ |
| 0    | 0    | 0      |
| 0    | 1    | 1      |
| 1    | 0    | 1      |
| 1    | 1    | 1      |

OPERADOR EXCLUSIVE OR **(XOR)**

| a    | b    | a ^ b |
| ---- | ---- | ----- |
| 0    | 0    | 0     |
| 0    | 1    | 1     |
| 1    | 0    | 1     |
| 1    | 1    | 0     |

OPERADOR DE NEGACIÓN **NOT**

| a    | ~ a  |
| ---- | ---- |
| 0    | 1    |
| 1    | 0    |

DESPLAZAMIENTO LÓGICO DE BITS

El desplazamiento lógico se usa para mover bits hacie la izquiera o derecha para colocarlos en la posición adecuada. El primer operando representa el binario que queremos modificar, mientras que el segundo indica las posiciones a desplazar.

| Desplazamiento a la izquierda | Desplazamiento a la derecha |
| ----------------------------- | --------------------------- |
| 00011100<<1 = 00111000        | 00011100>>1 = 00001110      |
| 00011100<<2 = 01110000        | 00011100>>2 = 00000111      |

En el desplazamiento a la izquierda, el bit más significativo(más a la izquierda) se pierde y se le asigna un 0 al menos significativo(el de la derecha). En los desplazamiento a la derecha ocurre lo contrario.

Tener en cuenta que los desplazamientos no son rotaciones, lo bits que sales por la izquierda se pierden mientras que los que entran por la derecha son rellenados con ceros. Este tipo de desplazamientos se denominan lógicos a diferencia de los cíclicos o rotacionales.

### LOS FLAGS

Identificar _flags_ en las aplicaciones sin implementar estructuras de flujo complejas o declaración de operaciones innecesarias.

Establecer flags:

let FLAG_A=parseInt('0001',2);
let FLAG_B=parseInt('0010',2);
let FLAG_C=parseInt('0100',2);
let FLAG_D=parseInt('1000',2);

| 1    | 1    | 1    | 1    | 1    | 1    | 1    | 1    | 1    | 1    |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| 512  | 256  | 128  | 64   | 32   | 16   | 8    | 4    | 2    | 1    |

numero.toString(2); -> Convertir un número en su valor respresentación en bits.
parseInt('binario',2); -> Convertr un cadena binaria dada en su valor decimal real.

Con este patrón ya identificado, crear un flujo que identificar los flags es más sencillo al actuar a nivel de bits.

Con esta estructura de control podemos preguntar por varios flags a la vez con muchas facilidad. Se recomienda crear previamente una máscara que indique explicitamente los flags que se requieren.

```javascript
let usrFlags=FLAG_A | FLAG_B; //Agrupar o combinar varios flags (análogo a la suma)
if(usrFlags & FLAG_A)
{
   //sentencias
}
```

### MEJORAR EL RENDIMIENTO

### Curiosidad

Obtener parte entera de un número con coma flotante utilizando una comparación OR a 0, o el operador XOR con el 0.
Este es un Trucando se puede obtener con la funcioón Math.floor().

