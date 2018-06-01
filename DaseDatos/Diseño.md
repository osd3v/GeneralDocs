## Métodologia para diseñar una Base de Datos

### 1.- Identificar el problema del mundo real

Identificar el problema del cliente, y requerimiento de almacenamiento de información. 

### 2.- Recolectar información del problema

Levantamiento de la información. Se debe documentar los requerimientos, con la finalidad de realizar los diseños y contrucción. Se sugiere un patrón o prototipo para mejorar el flujo de trabajo de la aplicación, ya que con este prototipo se entenderá los procesos que pueden ser complejos de plasmar. 

### 3.- Crear el Modelo conceptual (respresenta el problema como se percibe del mundo real).

Utilizando el Modelo Entidad relacional (M-E/R), se debe entender los conceptos de entidad, relación, atributo y dominio. 

Entidad : objeto real o abstracto.
Atributo : Caracteristicas de las entidades
Relación: conexiones
Dominio: rango de valores posibles de los atributos

### 4.- Modelo lógico

Un modelo relacional tiene uno o muchos esquemas relacionados, y a este conjunto de esquemas se le conoce como "esquema relacional" de base de datos. 

Transformar M-E/R a esquema relacional

### 5.- Normalizar

-1ra Forma Normal, Eliminación de grupos repetitivos
-2da Forma Normal, Existir dependencia funcional completa (DFC) , es decir que un dato no clave(atributo simple) depende de un dato clave (identificador).
-3ra Forma Normal, No debe existir dependecia funcional transitoria (DFT), es decir, que dato clave no puede depender de otro dato que tampoco sea clave.

### 6.- Crear el Modelo Físico (DDL)

Se crea el Modelo Físico con un DBMS

### 7.- Uso del componente DML

Lenguaje de manipulación de datos

