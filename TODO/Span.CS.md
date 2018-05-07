## Introduccion Span<T>



Para el escenario donde se exponga una rutina para trabajar in situ sobre los dato de la memoria. Es probable que exponga un método que utilize toda una matriz y proporcione una operaciones para el T[]. Esto es correcto si la la rutina utilizará toda las matriz, sin embargo que se utiliza cuando se desea operar parcialmente. Es este caso es probable que exponga una sobrecarga que tome un desfase y un recuento.

Ahora, cual es el camino cuando se desea admitir dato en memoria que no estan en la matriz, sino que proceden de código nativo, residen en la pila o solo tiene un puntero y una longitud.

Entonces como implementar un método para operar sobre una región arbitraria de la memoria y , que aun asi, funciona igual de bien con matrices completar o subconjuntos de las matrices, asi como con matrices administradas y punteros no administrados.

No se debe obligar al autor a realizar asignaciones ni copias y debe funcionar igual con entradas de tipo T[] y T*

## Span<T>

System.Span<T> es un nuevo tipo de valor en .NET que permite la representación de regiones contiguas de memoria arbitraria, independientemente si dicha memoria esta asociada a un objeto administrado, la proporciona código nativo a tráves de la interoperabilidad o se encuentra en la pila. Todo esto sin dejar de proporcionar el acceso seguro con caracteristicas de rendimiento , como la de las matrices.



Cuando se envuelve un arreglo con Span<T> esta puede apuntar a cualquier subrango con un inicio y longitud arbitrario.

Referencia

[Referencia Documentación Github](https://github.com/dotnet/corefxlab/blob/master/docs/specs/span.md)

[Referencia Microsoft Magazine](https://msdn.microsoft.com/es-es/magazine/mt814808)











