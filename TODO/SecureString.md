## SecureString

**CADENAS MÁS SEGURAS**

las cadenas standar nunca fueron una solución segura para almacenar información sensible como contraseñas. 

Problemas de utilizar cadenas:

* No esta referenciado, por lo tanto en garbage collector puede moverlo y dejar multiples copias en la memoria
* No esta encriptado, cualquiera que pueda leer el proceso de la memoria tiene la posibilidad de ver el valor de la cadena. Además, si la manipulación o intercambio de proceso se realiza en el disco, el contenido no encriptado el contenido de la cadena esta guardada en una archivo. 
* No es mutable, cuando se debe modificar la cadena, se debe tener todas las versiones en la memoria. No es una alternativa efectiva para eliminarse una vez se haya terminado de utilizar.

Anteriormente la solución recomendada era utilizar un arreglo de bytes. 

SecureString esta encriptado(DPAPI) y solo es desencriptado cuando se accede a su valor. El GC no mueve la cadena escriptada en la memoria, y no se necesita preocuparte de tener multiples copias de la cadena en diferentes direcciones. Adicionalmente cuenta con la caracteristica de bloquearlo como de solo lectura evitando que sea modificado.  Implementa la interface IDisposable, cuando se termina de utilizar una instancia de la clase, se puede cerrar cada instancia directamente o indirectamente. 

###Operaciones para modificar los datos de la cadena 

1. AppendChar()
2. InsertAt()
3. RemoveAt()
4. SetAt()
5. MakeReadOnly()

OBS: el momento de las destrucción de objetos por el GC es arbitrario

Dispose: es un método que indica la diponibilización de los recursos de memoria que tenia en reserva. No garantiza la inmediata eliminación.

Una instancia de la clase System.String es inmutable. No es posible indicar cuando se elimine la instancia. Las operaciones para modificar una instancia existente crean una copia  para realizar las manipulaciones.  

## Tipos Inmutables

Un objeto es inmutable si no cambia de estado una vez este creado. La principal razon de su uso es la programación concurrente. 

