## TUPLES

la clase System.Tuple provee un tipo para representar una colección key-value. Este es utilizado cuando se requiere una determinada estructura de datos, pero no se quiere crear un tipo separado para esto.

```c#
public Tuple<string int> getInfo()
{
    return new Tuple<string,int>("oscar",23);
}
```

Posteriormente para acceder se refencia con Item1 y Item2

### Problema de tuplas

* se debe acceder  a la propiedades con un patrón ItemX
* Se tiene el limite máximo de 8 propiedades
* Tuple es un tipo referenciado

## VALUE TUPLE 

C# introdujo la estrucutra ValueTuple 

* se puede asociar el nombre de los elementos de una tupla, se tiene un nivel de diseño y validación en tiempo de compilación del código.
* Se cuenta con la flexibilidad de acceder a todos lo elementos de la tupla o solo a una parte(_), 
* Value Tuple son tipos y no herencia o otra caracteristica, esto significa que ValueTuple tiene un mejor rendiemiento.


Referencia

[Microsoft Developer](https://blogs.msdn.microsoft.com/mazhou/2017/05/26/c-7-series-part-1-value-tuples/)

